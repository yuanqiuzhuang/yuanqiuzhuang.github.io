---
title: Github pages + Hexo搭建个人博客
date: 2016-12-26 18:59:25
tags: [github,hexo]
categories: 教程
---
``` c++
#include <iostream>
#include <string>
using namespace std;
int main(){
	int n;
	cin>>n;
	while(n--){
		string s1,s2="";
		cin>>s1;
		for(int i=0;i<s1.length();i++){
			switch(s1[i]){
				case '0':s2+="0000";break;
				case '1':s2+="0001";break;
				case '2':s2+="0010";break;
				case '3':s2+="0011";break;
				case '4':s2+="0100";break;
				case '5':s2+="0101";break;
				case '6':s2+="0110";break;
				case '7':s2+="0111";break;
				case '8':s2+="1000";break;
				case '9':s2+="1001";break;
				case 'A':s2+="1010";break;
				case 'B':s2+="1011";break;
				case 'C':s2+="1100";break;
				case 'D':s2+="1101";break;
				case 'E':s2+="1110";break;
				case 'F':s2+="1111";break;
				default:break;
			}
		}
		int len=s2.length();
		if(len%3==1) s2="00"+s2;
		else if(len%3==2) s2="0"+s2;
		int flag=0;
		for(int i=0;i<=s2.length()-3;i=i+3){
			int r=4*(s2[i]-'0')+2*(s2[i+1]-'0')+s2[i+2]-'0';
			if(r) flag=1;
			if(flag) cout<<r;
		}
		cout<<endl; 
	}
	return 0;
} 

```

> 哈哈哈哈哈