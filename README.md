# program
#include <iostream>
#include <string>
#include <bits/stdc++.h> 

using namespace std; 

void replace(string s,int k){ 

    string S; 
    for(int i=0; i<s.length(); ++i) 
    {

        int val = int(s[i]); 

        int dup = k; 

        if(val + k > 122){ 

            k =k- (122-val); 
            k = k % 26; 
            S =S+ char(96 + k); 
        } 
        else

            S =S+ char(val + k); 

        k = dup; 
    } 

    cout<<S; 
} 

int main(){

  string str; int k;

  cout<<"Enter a string: ";

  cin>>str;

  cout<< " Enter the value of k: ";

cin>>k;

replace(str, k);

    return 0; 
} 
