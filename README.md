//# ROCK-PAPER-SCISSORS-C++-
//This is a code for game of rock paper scissors in c++ programming language.

#include<iostream>
#include<cmath>
#include <cstdlib> 
#include <ctime> 
#include<stdlib.h>
#include<cstring>
using namespace std;
int main()
 {
	srand(time(0));
	string a;
	cout<<"ENTER YOUR NAME : ";
	cin>>a;
	cout<<"**********WELCOME TO ROCK PAPER SCISSORS  "<<a<<"*********"<<endl;
	int n;
	cout<<a<<"  PLEASE ENTER NUMBER OF ROUNDS YOU WANT TO PLAY : \n";
	cin>>n;
	
     char t1;   //p or s
    int t2;
    char t3;
    int cw=0,pw=0,d=0;     // cw=computerwins , pw= player wins , d=draw
	
	for(int i=1; i<=n; i++){
		cout<<"ENTER R FOR ROCK - P FOR PAPER - S FOR SCISSORS :\n";
		cout<<"ENTER YOUR CHOICE "<<a<<endl;
		cin>>t1;
		
		t2=rand()%3;
		if(t2==0){
			t3='R';
		}
		if(t2==1){
			t3='P';
		}
		if(t2==2){
			t3='S';
		}
		
		cout<<a<<" YOU ENTERED "<<t1<<" AND COMPUTER CHOSE "<<t3<<endl;
        
		if(t1=='R' && t2==0){
			cout<<"GAME IS A DRAW :";
			d++;
		}
			if(t1=='P' && t2==0){
			cout<<a<<" WINS:";
			pw++;
		}	
			if(t1=='S' && t2==0){
			cout<<"COMPUTER WINS:";
			cw++;
		}
			if(t1=='R' && t2==1){
			cout<<"COMPUTER WINS:";
			cw++;
		}	
			if(t1=='P' && t2==1){
			cout<<"GAME IS A DRAW :";
			d++;
		}	
			if(t1=='S' && t2==1){
			cout<<a<<" WINS:";
			pw++;
		}
		if(t1=='R' && t2==2){
			cout<<a<<" WINS:";
			pw++;
		}
		if(t1=='P' && t2==2){
				cout<<"COMPUTER WINS:";
			cw++;
		}
		if(t1=='S' && t2==2){
		cout<<"GAME IS A DRAW :";
		d++;
		}
	}
	
	cout<<endl<<endl<<"                         **RESULTS**     \n";
	cout<<a<<" WON "<<pw<<" TIMES. \n";
	cout<<"COMPUTER WON "<<cw<<" TIMES. \n";
	cout<<"THE GAME WAS DRAW "<<d<<" TIMES. \n";
	
return 0;	
}


  
