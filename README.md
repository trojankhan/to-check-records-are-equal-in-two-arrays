#include<iostream>
#include<fstream>
using namespace std;

void no()
{
	int x, y;
	cin >> x >> y;
	ofstream fout;
	fout.open("num.txt", ios::out);
	fout << x << endl;
	fout << y << endl;
	fout.close();
}

void read()
{
	int x = 0;
	int y = 0;
	ifstream fin;
	fin.open("num.txt", ios::in);
	fin >> x;
	fin>> y;
	if (x == y)
	{
		cout << "numbers are equal" << endl;
	}
	else
	{
		cout << "numbers are not equal" << endl;
	}
	fin.close();
}
int main()
{
	no();
	read();
	system("pause");
	return 0;
}

