# Flag


#include<iostream>
#include<iomanip>
using namespace std;
int main()
{
	srand(unsigned(time(0))); int n = rand() % 12 + 9; n = 2 * n + 1;
	char** array = new char* [n];
	for (int i = 0; i < n; i++)
	{
		array[i] = new char[n];
	}
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			array[i][j]=' ';
		}
	}
	//------------------------------------
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			if (i==0||j==0||j==n-1||i==n-1||(i == j+1)|| (i -1 + j == n - 1) ||(i+1+j==n-1)||(i==j-1)||(i+2==(n-i-1))|| (i -2 == (n - i - 1)) || (j - 2 == (n - j - 1)) || (j+2 == (n - j - 1)))
			{
				array[i][j] = '*';
			}
			
		}
	}
	//------------------------------------
	for (int i = 0; i < n; i++)
	{
		for (int j = 0; j < n; j++)
		{
			cout << setw(4) << array[i][j];
		}cout << endl;
	}
	//------------------------------------
	for (int i = 0; i < n; i++)
	{
		delete array[i];
	} delete[] array; array = nullptr;
}
