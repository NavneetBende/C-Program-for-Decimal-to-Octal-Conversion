# C-Program-for-Decimal-to-Octal-Conversion

Program for Decimal to Octal conversion in C++
We are going. to understand how to code Decimal to Octal Conversion in C++ and different ways of coding Decimal to Octal in C++

The C++ program to convert decimal to octal number accepts a decimal number from the user. This number is further converted to its equivalent octal number after following a series of steps. The following section gives an algorithm for this conversion. It is then followed by a C++ program.

Decimal to Octal in C++
While loop in C
Methods discussed
Using an array to store the comparable octal value
Using int variable to store comparable octal value
Method 1
C++ Program to Convert Decimal to Octal new
C++ Code:-
Run
#include<iostream>
using namespace std;

void convertOctal(int num)
{
    // creating an array to store octal equivalent
    int octalArray[32];
 
    // using i to store octal bit at given array position
    int i = 0;
    while (num > 0) {
 
        // resultant remainder is stored at given array position
        octalArray[i] = num % 8;
        num = num / 8;
        i++;
    }
 
    // printing octal array in reverse order
    for (int j = i - 1; j >= 0; j--)
        cout << octalArray[j];
}
 
int main()
{
    int n = 148;
    convertOctal(n);
    return 0;
}
Output
224
Related Pages
Hexadecimal to Decimal conversion

Decimal to Binary conversion

Decimal to Octal Conversion

Decimal to Hexadecimal Conversion

Binary to Octal conversion

Octal to Binary conversion

Method 2
Decimal to Octal Conversion in C++
C++ Code:-
Run
#include<iostream>
using namespace std;

void convertOctal(int num)
{
    int octal = 0;
    int rem, i = 1;
    
    while(num!=0)
    {
        rem = num % 8;
        num /= 8;
        octal += rem * i;
        
        // moving to next position ex: units -> tens
        i *= 10;
    }
    cout << octal;
}
 
int main()
{
    int decimal_num = 221;
    convertOctal(decimal_num);
    return 0;
}
Output
335
