<!-- # Generate--Otp -->
<!-- Generate Otp using C++ -->

#include<bits/stdc++.h>
using namespace std;

<!-- Main logic for generating the otp -->
string generateOtp(int len){
  string str ="abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789";
  int n =str.length();
  string Otp;
  
  for(int i=0; i<len ;i++){
    Otp.push_back(str[rand() % n]);
  }
  return Otp;
}

int main(){
  srand(time(NULL));
  int len =6;
  string ans =generateOtp(len);
  cout<<ans;

}
