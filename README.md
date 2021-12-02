// Data-Structure-Tower-Of-Hanoi-


#include<bits/stdc++.h>
using namespace std;


void towerOfHanoi(int n,char source,char intermediate,char destination)//3  A   C   B
{
    if(n == 1)
    {
        cout<<"Move disk 1 sources "<<source<<" to destination "<<destination<<endl;
        return;
    }

    towerOfHanoi(n-1,source,destination,intermediate);//2 a b c   1 a b c

    cout<<"Move disk "<<n<<" From source "<<source<<" to destination "<<destination<<endl;

    towerOfHanoi(n-1, intermediate, source,destination);
}


int main()
{
    int n;
    cin>>n;

    char source = 'A';
    char intermediate = 'B';
    char destination = 'C';

    towerOfHanoi(n,source,intermediate,destination);//3 A C B

    return 0;
}
