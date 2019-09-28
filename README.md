# program
#include <iostream>
#include <string>
#include <bits/stdc++.h> 

using namespace std; 

void encode(string s,int k){ 

    string newS; 
    for(int i=0; i<s.length(); ++i) 
    { 
        int encode;

        int val = int(s[i]); 

        int dup = k; 

        if(val + k > 122){ 

            k -= (122-val); 
            k = k % 26; 
            newS += char(96 + k); 
        } 
        else

            newS += char(val + k); 

        k = dup; 
    } 

    cout<<newS; 
} 

int main(){

  string str; int k;

  cout<<"Enter a string: ";

  cin>>str;

  cout<< " Enter the value of k: ";

cin>>k;

encode(str, k);

    return 0; 
} 
