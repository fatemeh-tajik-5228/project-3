# project-3
#include <iostream> 
using namespace std ;
//vast va rasand //ejtema eshterak matris ha
int main () {
	int n , m ;
	cout << "satr matris ra vared kon" << "\n" ;
	cin >> n ;
	cout << "sotom matris ra vared kon" << "\n" ;
	cin >> m ;
	
	int A[n][m] ;
	cout << "matris rabeteh A ra vared kon(0 or 1)" << "\n" ;
	for(int i=0 ; i<n ; i++) {
		cout << "satr" << i+1 << ": \n" ;
		for(int j=0 ; j<m ; j++) {
			cin >> A[i][j] ;
		}
		cout << "\n" ;
	}
	int B[n][m] ;
	cout << "matris rabeteh B ra vared kon(0 or 1)" << "\n" ;
	for(int i=0 ; i<n ; i++) {
		cout << "satr" << i+1 << ": \n" ;
		for(int j=0 ; j<m ; j++) {
			cin >> B[i][j] ;
		}
		cout << "\n" ;
	}
	
	int result ;
	string a ;
	cout << "(Or) or (And) \n" ;
	cin >> a ;
	for(int i=0 ; i<n ; i++) {
		for(int j=0 ; j<m ; j++) {
			if(a == "Or") result = A[i][j] || B[i][j] ;
			else if(a == "And") result = A[i][j] && B[i][j] ;
			else {
				cout << "na motabar" ;
				return 1 ;
			} 
			cout << result << "\t" ;
		}
		cout << "\n" ;
	}
	return 0 ;
}
