#include <iostream>
#include <iomanip>
using namespace std;


int calculateoverduedays(int returnDate,int borrowingDate) {
	int allowedDays=14;
	int actualDays=returnDate-borrowingDate;
	int overdueDays;

	if(actualDays>allowedDays) {
		overdueDays=actualDays-allowedDays;
	} else
		overdueDays=0;

	return overdueDays;

}


int borrowBook(int availableQuantity) {

	if(availableQuantity>0) {
		cout<< "Book is available for borrowing."<<endl;
		availableQuantity=availableQuantity-1;
		cout<<"Updated stock: "<< availableQuantity<< endl;
		cout<<"Borrow Successful"<<endl;
	} else
		cout<< "Borrow Failed: Book Out of Stock"<<endl;
	return availableQuantity;

}
int returnBook(int availableQuantity) {
	availableQuantity=availableQuantity+1;
	cout<<"Return Successful"<<endl;
	return availableQuantity;
}


int main() {
	string memberID,BookID,transactionType;
	int borrowingDate,returnDate,availableQuantity,overdueDays;
	double fineperDay,overduefine;

	cout <<fixed <<setprecision(2);

	cout <<"Enter member ID: ";
	cin >>memberID;
	cout << "Enter Book ID: ";
	cin >> BookID;
	cout <<"Enter transaction type (Borrow/Return): ";
	cin >>transactionType;
	cout <<"Enter borrow date: ";
	cin >> borrowingDate;
	cout <<"Enter return date: ";
	cin >>returnDate;
	cout <<"Enter fine per day: ";
	cin >>fineperDay;
	cout << "Enter available quantity: ";
	cin >>availableQuantity;

	overduefine=0.00;


	if (transactionType=="Borrow") {
		availableQuantity=borrowBook(availableQuantity);
	} else if (transactionType=="Return") {
		availableQuantity=returnBook(availableQuantity);
		overdueDays=calculateoverduedays(returnDate,borrowingDate);
		overduefine = overdueDays*fineperDay;
	} else {
		cout <<"Invalid transaction type."<<endl;
	}
	cout <<"Updated Book Quantity: "<<availableQuantity<<endl;
	cout <<"Overdue Fine: RM" << overduefine<<endl;



	return 0;
}
