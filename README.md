# UncommonHack-2018

Code Without Audio
#include <iostream>
#include <cstdlib>
#include <string>
using namespace std;

//converts Farenheit to Hervens
class FartoHer
{
private:
	double hervens, farenheit;
public:
	FartoHer();
	FartoHer(double);
	double setfarenheit();
	double getfarenheit();
	double getHervens();
	void fhdisplay();
};

FartoHer::FartoHer()
{
	farenheit = -457.67;
	//-420 is too cold. Man needs second jacket.
	if (farenheit <= 420)
		cout << "EH. Too cold.\n";
}

FartoHer::FartoHer(double farenheit)
{
	this->farenheit = farenheit;
}
//function sets farenheit in class
double FartoHer::setfarenheit()
{
	return this->farenheit = farenheit;
}
//function makes farenheit accessible from class
double FartoHer::getfarenheit()
{
	return farenheit;
}
//function finds hervens
double FartoHer::getHervens()
{
	hervens = farenheit + 420;
	return (hervens);
}
void FartoHer::fhdisplay()
{
	cout << "\nHere's your temperature in Hervens: " << getHervens() << ". You're welcome.\n\n";
}

void BSDegreeCalculator()
{
	double BS;
	BS = ((rand() % 5) + 1) * 84;
	cout << BS << endl << endl;

	if (BS == 84)
		cout << "MANS NOT HOT";
	if (BS == 168)
		cout << "Man won't take off his jacket.";
	if (BS == 252)
		cout << "Skrrat, skidi-kat-kat mans not hot.";
	if (BS == 336)
		cout << "At this degrees, you smoke trees. Skidiki-pap-pap. Mans still not hot.";
	if (BS == 420)
		cout << "The girl told me, \"Take off your jacket\" I said, \"Babes, man's not hot\"";

}

int main()
{
	double farenheit;
	int num, fam, BS;
	string answer;

	cout << "This absolutely amazingly seamless and technologically advanced program\n";
	cout << "does exactly what you've needed since day one. We spent a total of three\n";
	cout << "years designing this program for your benefit. As with any great power \n";
	cout << "comes great responsibility, we hope that you take care to use this program\n";
	cout << "to enhance society.\n\n\n";

	cout << "Please enter some random temperature in farenheit por favor.\n";
	cin >> farenheit;
	FartoHer A(farenheit);
	A.fhdisplay();

	cout << "Now you might want to convert hervens to josies. Do you? Type 'y' for yes or 'n' for no: ";
	cin >> answer;
	cout << "\n\nIt really didn't matter what you typed because the only code written is this message.\n\n";
	cout << "The temperature is 21 degrees Josie (super hot). \n\nWanna know it in Big Shaqs? \nType '1' for yes and '2' for no:";
	cin >> fam;
	if (fam == 1)
	{
		cout << "The answer to your querie is: ";
		BSDegreeCalculator();
	}
	if (fam == 2)
	{
		cout << "Are you sure about this? '1' for yes or '2' for no";
		cin >> num;
		if (num == 1)
			cout << "LOL TOO BAD! Here's your temperature in Big Shaqs: ";
		if (num == 2)
			cout << "Young grasshopper has learned their lesson. Good job. Here's your temperature in Big Shaqs: ";
		BSDegreeCalculator();
	}
	else 
	{
		cout << "Bet you didn't actually expect your answer to matter. \n\n I mean.. it didn't really. Here's the temperature in Big Shaqs: ";
		BSDegreeCalculator();
	}



	system("pause");
	return 0;
}
