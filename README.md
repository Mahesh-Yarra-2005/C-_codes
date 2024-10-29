# C++_codes
Just to store codes.
<br>
Author - Mahesh Yarra
?
//C++ code which converts given decimal number to its corresponding binary number 

#include <iostream>
using namespace std;
int main(){
    int n;
    cout<<"enter the value of n"<<endl;
    cin>>n;
    int ans=0;
    int i=0;
    while(n!=0){
        int bit =n&1;
        ans=(bit*pow(10, i))+ans;
        n=n>>1;
        i++;
    }
cout<<ans;
    return 0;
}

//Prime number detector

#include <iostream>
using namespace std;
int main (){
    int n;
    cout<<"enter the value of n"<<endl;
    cin>>n;
    int i=2;
    bool isprime=1;
    while(i<n){
        if(n%i==0){
            isprime=0;
            break;
        }
        i++;
    }
    if(isprime==0){
        cout<<"n is not a prime number"<<endl;
    }
    if (isprime==1){
        cout<<"n is a prime number"<<endl;
    }
    return 0;
}
