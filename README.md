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


//code which checks the numbers whether it is a power of 2 or not.

#include <iostream>
using namespace std;
#include <cmath> //To use log function

int main (){
    int n ;
    cout<<"enter the number"<<endl;
    cin>>n;
     double p;
    int m;
    p=log2(n);   //if p is an integer then output is true otherwise false
    m=p;    // p(double)- pcan be rational but m (int) - m will be an integer
    if (p==m){
        cout<<"true"<<endl;
    }else if (p!=m){
        cout<<"false"<<endl;
    }
    return 0;}

