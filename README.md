# multiset
tìm số lớn nhất trong cửa số ( 3 chữ số) tăng dần
#include <iostream>
#include <iomanip>
#include <string>
#include <cstring>
#include <string.h>
#include <set>
using namespace std;

main(){
int a[10];
for(int &x : a){
	cin>>x;
}
multiset <int > khoi;
for (int i=0 ; i<3;i++){
	khoi.insert(a[i]);
}
for ( int i=3;i<10;i++){
	cout<<*khoi.rbegin();
	khoi.erase(a[i-3]);
	khoi.insert(a[i]);
}
cout<<*khoi.rbegin();
	return 0;
}
