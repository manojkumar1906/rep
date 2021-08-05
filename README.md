#include <iostream>
using namespace std;
#define akka long long
bool bet(akka x[], akka y[])
{
    if ((x[0]>=y[0] && x[1]>=y[1] && x[2]>y[2])||(x[0]>=y[0] && x[1]>y[1] && x[2]>=y[2])||(x[0]>y[0] && x[1]>=y[1] && x[2]>=y[2]))
    {
        return true;
    }
    return false;
}
int main()
{
    akka t;
    cin>>t;
    while (t--)
    {
        akka a[3],b[3],c[3];
        cin>>a[0]>>a[1]>>a[2];
        cin>>b[0]>>b[1]>>b[2];
        cin>>c[0]>>c[1]>>c[2];
        if ((bet(a,b) || bet(b,a)) && (bet(b,c) || bet(c,b)) && (bet(c,a) || bet(a,c)))
        {
            cout<<"yes"<<endl;
        }
        else
        {
            cout<<"no"<<endl;
        }
    }
    return 0;
}
