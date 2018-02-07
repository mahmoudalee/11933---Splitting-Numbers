# 11933---Splitting-Numbers

#include <iostream>
using namespace std;

int main()
{
	int n;
	while (cin >> n && n)
	{
		bool flag = 1;
		int a = 0, b = 0;
		for (int i = 0; i < log2((double)n) + 1; i++)
		{
			if (n & (1 << i))
			{
				if (flag)
				{
					a |= 1 << i;
					flag = 0;
				}
				else
				{
					b |= 1 << i;
					flag = 1;
				}
			}
		}
		cout << a << " " << b << endl;
	}	                                         
    return 0;
}
