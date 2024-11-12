# C++_codes
Just to store codes.
<br>
Author - Mahesh Yarra
?


**//C++ code which converts given decimal number to its corresponding binary number **

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

//**Prime number detector**

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


//**code which checks the numbers whether it is a power of 2 or not.**

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



//**code which can tell the no of notes required of 100, 50, 20, 10, 1 for a given amount**

#include<iostream>
using namespace std;
int main (){
    int r;
    cout<<"Enter the amount"<<endl;
    cin>>r;
    int a, b, c, d, e;
    a = r/100;
    r = r-a*100;
    b=r/50;
    r=r-b*50;
    c=r/20;
    r=r-20*c;
    d=r/10;
    r=r-10*d;
    e=r;
    cout<<"100 rs notes: "<<a<<", 50 notes: "<<b<<", 20 notes: "<<c<<" ,10 notes: "<<d<<" , 1 notes: "<<e<<endl;
   
   }


//CODE which finds the index of the element in a rotated sorted array

#include<iostream>
using namespace std;
int findposition(int arr[], int n, int key) {
    int s =0;
    int e = n-1;
    int mid = s + (e-s)/2;
    while ( s<=e){
         mid = s + (e-s)/2;
         if ( arr[mid]== key){
            return mid;
         }
         if ( arr[mid]>= arr[s]){
            if ( arr[s]<=key && key <= arr[mid]){
                e= mid;
            }
            else {
                s= mid +1;
            }
         }
         else {
            if ( arr[mid]<key && key <=arr[e]){
                s = mid+1;
            }
            else {
                e = mid;
            }
         }
    }
 return -1;}

 int main (){
    int arr[8]={6,7,8,1,2,3,4,5};
    int ans = findposition(arr, 8, 5);
    cout<<ans<<endl;
 }//output 7


