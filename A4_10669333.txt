#include <iostream>
#include <math.h>

using namespace std;

int GCD(int p, int q)
//The GCD of any two numbers refers to the largest umber that divides them without leaving a remainder

{
    int rem = p%q;
    while(rem != 0)
    {
        p = q;
        q = rem;
        rem = p%q;
    }
    return q;
}
int main()
{
    cout << "Enter any two numbers to find their GCD"<<endl<<endl;
    int p,q;
    cin>>p>>q;
    cout <<"The GCD of "<<p<<" and "<<q<<" is "<<GCD(p,q);

    return 0;
}
