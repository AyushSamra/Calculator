#include<iostream>
#include<cmath>
using namespace std;
void display(){
    cout<<"Press + for addition operation."<<endl;
    cout<<"Press - for subtraction operation."<<endl;
    cout<<"Press * for multiplication operation."<<endl;
    cout<<"Press / for Division operation."<<endl;
    cout<<"Press e for exponent operation."<<endl;
    cout<<"Press r for square root  operation."<<endl;
    cout<<"Press % for percentage operation."<<endl;
    cout<<"Press c for clear all operation."<<endl;
}
void input(double a,char ch,double b,double &r){
cout<<"Enter the value of a: "<<endl;
cin>>a;
cout<<"Enter the value of ch: "<<endl;
cin>>ch;
cout<<"Enter the value of b: "<<endl;
cin>>b;
    switch (ch)
    {
    case '+':
   
     r=a+b;
     break;   
    case '-':
    
     r=a-b;
    break;    
    case '*':
     r=a*b;
    break;
    
    case '/':
    
     r=a/b;
        break;
    default:
    cout<<"Wrong operation: "<<endl;
    }
    cout<<"The value of "<<a<<" "<<ch<<" "<<b<<" is "<<r<<endl;
    cout<<"You are left with 9 no. of attempts!!!"<<endl;
}

int main(){
double a;double b;double r;int count=0;
char ch2;
char ch;
cout<<"\t\t\t\t *****SIMPLE CALCULATOR*******\t\t\t\t"<<endl;
cout<<"\t\t\t YOU CAN PERFORM ONLY 10 OEPRATIONS IN ONE GO: \t\t"<<endl;
display();
input(a,ch,b,r);

    for(int i=9;i>0;i--){
       
        ++count;
    cout<<"Do you want to perform further calculations (Y/N): "<<endl;
    cin>>ch2;

    if(ch2=='Y'){
        cout<<"Enter the new operation you want to perform with result: "<<r<<endl;
        cin>>ch2;
    cout<<"Enter the new value of a: "<<endl;
    cin>>a;
        switch (ch2)
        {
    case '+':
   
     r=r+a;
     break;   
    case '-':
    
     r=r-a;
    break;    
    case '*':
     r=r*a;
    break;
    
    case '/':
    
     r=r/a;
        break;
    default:
    cout<<"Wrong operation: "<<endl;
    }
    cout<<"The new result of operation is "<<r<<endl;
    int left=(i)-count;
    cout<<"You are left with "<<left<<" no. of attempts"<<endl;
    --count;
    }
    else if(ch2!='N'){
        cout<<"You have to type only (Y-N)!!!"<<endl;
        break;
    }
 else{
    cout<<"Your final answer is "<<r<<endl;
    break;
 }
    }

return 0;
}