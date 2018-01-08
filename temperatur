
#include <stdio.h>
#include <stdlib.h>

void CtoKF(float t)  /*celsii*/
{
	printf("%.2f F\n", t*1.8 + 32);
	printf("%.2f K\n\n", t + 273.15);
}

void FtoCK(float t)  /*farengeit*/
{
	printf("%.2f C\n", (t - 32) / 1.8);
	printf("%.2f K\n\n", t + 459.67);
}

void KtoCF(float t)  /*kelvin*/
{
	printf("%.2f C\n", t - 273.15);
	printf("%.2f F\n\n", t - 459.67);
}

void iError() /*error*/
{
	printf("Usage sample:\n");
	printf("(programm's path) t tChat\n");
	printf("Where 't' for numeric data, 'tChar' for tempeture scale (C,K,F).\n");
}

int main(int argc, char* argv[])
{
float t; /*temperature*/
char tChar;/*hkala*/

if (argc<2)	/*no arguments*/
iError();
else {
	 if (sscanf(argv[1], "%f", &t) == 1) /*1 argument*/
		{
		if (argc == 2) tChar = 'L'; /*2 argument*/
		else
		if (argc == 3) tChar = argv[2][0];
		   switch (tChar)
			{
			case 'C':
			case 'c':
				{ /*the number entered and C*/
				if (t + 273.15 >= 0)
					{
					CtoKF(t);
					}
				else printf("Error - K<0\n");
				break;
				}

			case 'F':
			case 'f':
				{ /*the number entered and F*/
				if (t + 459.67 >= 0)
					{
					FtoCK(t);
					}
				else printf("Error - K<0\n");
				break;
				}

			case  'K':
			case  'k':
				{ /*the number entered and K*/
				if (t >= 0)
					{
					KtoCF(t);
					}
				else printf("Error - K<0\n");
				break;
				}

				default:
				{ 
				printf("%.2f C:\n", t);
				if (t + 273.15 >= 0)
					{
					CtoKF(t);
					}
				else printf("Error - K<0\n");
				printf("%.2f F:\n", t);
				if (t + 459.67 >= 0)
					{
					FtoCK(t);
					}
				else printf("Error - K<0\n");
				printf("%.2f K:\n", t);
				if (t >= 0)
					{
					KtoCF(t);
					}
				else printf("Error - K<0\n");
				break;
				}

			}
		}
	 else
	 iError();
	 }
return 0;
}
