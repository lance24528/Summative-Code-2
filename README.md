// Summative-Code-2

#include <string>   
#include <iostream>
#include <math.h>
using namespace std;

void factorial(long double number) {

	long double n = number, factorial = 1, i;
	for (i = 1; i <= n; i++) {
		factorial = factorial * i;
	}
	cout << "\nFactorial of " << n << " is " << factorial << "\n" << endl;
	
}
void mtable(long double number) {

	long double table = 10;
	do 
	{
		cout << table << " x " << number << " = " << table * number << endl;
		table--;
	} while (table !=0);
}
void exponent(long double number) {

	long double pow1 = 10;
	while (pow1 != 4)
	{
		
		cout << "\n" << number << " raised to the power of " << pow1 << " = " << pow(number, pow1) << endl;
		pow1--;
	}
}
int main()
{
	long double number; string fname;
	cout << "Enter full name: " << endl;
	getline(cin, fname);
	cout << "\n" << fname;
	cout << "\n\nEnter a number: ";
	cin >> number;
	while (number < 1)
	{
		cin >> number;
		cin.clear();
		cin.ignore(1000, '\n');
		cout << "Input a valid number: " << endl;
	}
		factorial(number);
		mtable(number);
		exponent(number);

		return 0;
}

