# CPP MODULE 3 :
# 3a :
# PROGRAM STATEMENT :
write a c++ program to read 3 student details(regno,name & gender ) in one class and display the 
above details in another class using inheritance?
# ALGORITHM :
1. Define an array employees of DisplayEmployee objects for storing details of multiple employees.
2. Use a loop to call setDetails() for each employee, reading employee number, name, and gender.
3. Display a header message, "Student Details are".
4. Use a loop to call showDetails() for each employee, printing the details.
5. Return from main() to terminate the program.
# PROGRAM :
NAME  : DILIP KUMAR R
REG NO : 212222040037
```
#include <iostream>
using namespace std;
class Employee
{
protected:
 int empno;
 string empname;
 string empgender;
public:
 void setDetails() 
 {
 cin >> empno >> empname >> empgender;
 }
};
class DisplayEmployee : public Employee 
{
public:
 void showDetails()
 {
 cout << empno << " " << empname << " " << empgender << endl;
 }
};
int main()
{
 const int numEmployees = 3; 
 DisplayEmployee employees[numEmployees];

 for (int i = 0; i < numEmployees; ++i) 
 {
 employees[i].setDetails();
 }
 
 cout << "Student Detaile are" << endl;
 
 for (int i = 0; i < numEmployees; ++i)
 {
 employees[i].showDetails();
 }
 return 0;
}}
```
# OUTPUT :
 ![image](https://github.com/user-attachments/assets/4ba9447b-0aa8-4846-bcf6-6a7b775d5861)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 3b :
# PROGRAM STATEMENT :
Write a program to implement protected member with integer values?
# ALGORITHM :
1. Define a base class with a protected member variable to store an integer value.
2. Declare a public function in the base class to set and get the value of the protected member.
3. Define a derived class that inherits the base class and accesses the protected member.
4. In the main function, create an object of the derived class and use its function to access the protected 
member.
5. Display the integer value and end the program.
# PROGRAM :
```
#include <iostream>
using namespace std;
class Base 
{
protected:
 int num; 
public:
 void setNum(int n)
 {
 num = n;
 }
};
class Derived : public Base
{
public:
 void displayNum()
 {
 cout << "The value of num is: " << num << endl;
 }
};
int main()
{
 Derived obj;
 int input;
 cin >> input;
 obj.setNum(input);
 obj.displayNum();
 return 0;
}
```
# OUTPUT :
 ![image](https://github.com/user-attachments/assets/98516d98-0abc-4bc6-b19d-864c4351e7fa)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 3c :
# PROGRAM STATEMENT :
write a c++ program to check loan eligibility based on age and income using 
multiple inheritance(age greater then 20 and less than 46) and income greater then 20000 is eligible 
for loan)
# ALGORITHM :
1. Read the age and income from the user.
2. Use setAge() and setIncome() methods to store the age and income of the applicant.
3. Use the checkEligibility() method to determine loan eligibility based on age and income
4. If the age is between 21 and 45 (inclusive) and income is above 20,000, print "Eligible for Loan"
5. Otherwise, print "Not Eligible for Loan".
# PROGRAM :
```
 #include <iostream>
using namespace std;
class Age 
{
protected:
 int age;
public:
 void setAge(int a)
 {
 age = a;
 }
};
class Income
{
protected:
 int income;
public:
 void setIncome(int inc) 
 {
 income = inc;
 }
};

class LoanEligibility : public Age, public Income
{
public:
 void checkEligibility() 
 {
 if (age > 20 && age < 46 && income > 20000)
 {
 cout << "Eligible for Loan" << endl;
 }
 else 
 {
 cout << "Not Eligible for Loan" << endl;
 }
 }
};
int main() 
{
 LoanEligibility applicant;
 int age, income;
 cin >> age;
 cin >> income;
 applicant.setAge(age);
 applicant.setIncome(income);
 applicant.checkEligibility();
 return 0;
}
```
# OUTPUT :
 ![image](https://github.com/user-attachments/assets/07e91c56-e65e-49da-a8d7-a8dc0df14b66)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.

# 3d :
# PROGRAM STATEMENT :
Write a C++ program to pass a character to the parameterized constructor of the base class through 
derived class .
# ALGORITHM :
1. Define a base class with a parameterized constructor that accepts a float.
2. Define a derived class that calls the base class constructor using an initializer list to pass the float to 
the base class constructor.
3. In the main function, create an object of the derived class and pass a character to the derived class 
constructor.
4. The derived class constructor will forward the float to the base class constructor.
5. Display the float in the base class constructor and end the program.
# PROGRAM :
```
#include <iostream>
using namespace std;
class Base
{
private:
 float pwd;
public:
 Base(float p)
 {
 pwd = p; 
 cout << " The value passed to the base class is " << pwd << endl;
 }
};
class Derived : public Base 
{
public:
 Derived(float p) : Base(p)
 {
 cout << "The value " << p << " is passed through the derived class constructor" << endl;
 }
};
int main() 
{
 float a;
 cin>>a;
 Derived obj(a);
 return 0;
}
```
# OUTPUT :
 ![image](https://github.com/user-attachments/assets/eab89cbe-7354-4bb4-b52b-ea5c4d87a476)

# RESULT :
Thus, The program is verified and executed successfully.The outputs match the expected 
results, confirming its correctness.
