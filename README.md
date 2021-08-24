# ObjectOrientedProgramming
C++ programs 

Each lab has some questions given for practice 

Codes in each file : 

LAB 1

1.Write a Program To pass an entire array to a function.Print all the elements and Return the largest element

2.Write a Program To pass a student name,roll no and average marks as function array and print all the details in user defined function

3.Write a Program To create a function that calculate rate of interest and return the value to the calling function


LAB 2

1.Write a program to overload the function area to compute area of rectangle, circle and square

2. Write a program to allocate n spaces dynamically to allocate for integers. Enter values and find the sum and average. The value of n is enter by user from keyboard.


LAB 3

1.Write a program  in c++to create a class to show the use of static and non static data members and member functions.

2.Write a program in C++to create a class to show overloading of member functions where make one member function as online and another as non online.

3.Write a program to create a class student  having roll, and 5 subject marks. Input and display the details of two students along with average mark.


LAB 4

1. WAP to swap private data member of two classes. [The classes have no relation with each other].

2.Create two classes which stores distance in feet, inches and meter, centimeter format respectively. Write a function which compares distance in object of these classes and displays the larger one.

3.Create a class with an integer data member. Include functions for input and output in class. Count the number of times each function is called and display it.

4.Create a class which stores name, roll number and total marks for a student. Input data for n students. Find the average marks scored by n students, store it as a data member of the class and display it using a function which may be called without object.

5.Create a class which stores name, author and price of a book. Store information for n number of books. Display information of all the books in a given price range using friend function.


LAB 5

1.Create a class complex which stores real and imaginary part of a complex number.Include all types of constructors and destructor. The destructor should display a message about the destructor being invoked. Create objects using different constructors and display them. 

2. Create a class which stores time in hh:mm format. Include all the constructors. The parameterized constructor should initialize the minute value to zero, if it is not 
provided. 

3. Create a class which stores a string and its length as data members. Include all the constructors. Include a member function to join two strings and display the concatenated string. 

4. WAP to demonstrate the order of call of constructors and destructors for a class. 

5. WAP to count number of objects created from a class using concept of static data members and static member function.


LAB 6

1..Create a class distance which stores a distance in feet and inches. Input 2 distance values in objects, add them, store the resultant distance in and object and display it. 
[Write the above program in two ways. a) store the resultant distance in the calling object:C3.add(C1,C2) b) return the resultant object C3=C1.add(C2)]

2.Write a program in C++ to derive a class “grade” from student which has four subject marks, name and roll number of a student.The “student” class stores the section,age of the student as its private member. Input the details for two students and print all the details with average mark.( The derived class is to be derived in private mode)

LAB 7

1.Write a program to create a class students having average marks as it's data member.Create two object and add user defined values entered by user from keyboard and add to both the object separately and display them by overloading binary plus operator and display them.

2.Write a program to create a class students having average marks as it's data member.Create two object and add user defined values entered by user from keyboard and add to both the object separately and display them by overloading binary plus operator and display them.Perform using friend function 

3.  .Write a program to create a class students having average marks as it's data member.Add these properties of one object to another object by using member and friend function and display them

4. Write a program to create a class students having average marks as it's data member. Overload binary plus operator to add two objects and store results to another object using member and friend function

LAB 8

1. WAP to overload following operators for class distance, which stores the 
distance in feet and inches. 
a)Overload Binary + to add two objects (D3=D1+D2) 
b)Add an object to an integer, where the integer should be added to the inches value ( D2=4+D1) 
c)Overload Unary - to show the new sign of values. 
Link : https://onlinegdb.com/HyD9_EPDD

2. Create a class to store an integer array. Overload insertion and 
extraction operator to input and display the array elements. 
Link : https://onlinegdb.com/rkIWtEvPP

3. Create a class which a complex number. Add two objects and display the resultant object.Overload the ++ (post and pre) operator for the class. 
Link : https://onlinegdb.com/BytGtEvvP

4. Create a class which allocates the memory for a string through 
dynamic constructor. Overload the binary + to concatenate two strings 
and display it. 
Link : https://onlinegdb.com/rkTmYVPDD
 
5.WAP to add two objects of time class. Overload the operator ‘==’ to compare two objects and display whether they are equal or not. Overload the assignment operator to assign one 
property to another and display the time. 
Link : https://onlinegdb.com/SypNtNvvw

6.WAP to add two objects of distance class. Overload the 
operator > to compare two objects and return the object with 
larger time value and display it. Overload the == operator to 
compare and display whether two given objects contain same 
distance value. 
Link : https://onlinegdb.com/rJ4IY4DvP

** Lab 9 **

Q1.WAP to display content of a file using character output function.

ANS 1:

#include<iostream>
#include<string.h>
#include<fstream>
#include<stdlib.h>
using namespace std;
 
int main()
{
        
        char s[100], fname[100];
        ofstream out;
        out.open("abc.txt");
 
        cout<<"Enter any data:: ";
        cin>>fname;
        out<<fname;
        out.close();
        ifstream in;
 
        in.open("abc.txt");
 
        if(!in)
        {
                cout<<"\nError in opening file..!!\n";
 
                exit(0);
        }
 
        cout<<"\n";
 
        while(in.eof()==0)
    {
        in>>s;
        cout<<s<<" ";
    }
 
        cout<<"\n";
        in.close();
 
return 0;
 
}






















Q2. WAP to copy contents of one file to another.

ANS 2:

#include<iostream>
#include<fstream>

using namespace std;
int main()
{

	fstream if1;
	fstream of1;
	char ch;
	if1.open("abc.txt",ios::in);
	of1.open("ctext.txt");
	while(!if1.eof())
	{
		if1>>ch;
		of1<<ch;
		cout<<ch<<" ";
	}
	cout<<"File copied successfully..!!";
	if1.close();
	of1.close();
	return 0;
}








Q3. WAP to write 10 strings into a file and display them from file.

ANS 3:
#include <iostream>
#include <fstream>
using namespace std ;
int main(void)
{
    ofstream out ;
    char data[100] ;
    string s="a.txt" ;
    string c ;
    int z=10 ;
    for(int i=0;i<z;i++)
    {
      out.open(s) ;
      cout<<"enter content\t";
      cin>>c;
      out<<c ;
      s[0]++ ;
      out.close() ;
    }
    s="a.txt" ;
for(int i=0;i<z;i++)
  {
    ifstream in;
       in.open(s);
       in>>data ;
       cout<<data<<"\t";
       in.close() ;
       s[0]++ ;
  }

    return 0 ;
}

Q4. WAP to display content of a file in reverse order.

ANS 4: 

#include<fstream>
#include<string.h>
#include<stdio.h>
#include<iostream>
using namespace std;
void Create()
{	std::fstream fil;
	fil.open ("Student.txt",ios::app);
	char ch,S[80];
	cout<<"Enter line : ";
	cin.getline(S,sizeof(S));
	fil<<S<<endl;
}
void Display()
{	fstream fil;
	fil.open("Student.txt",ios::in);
	char S[80];
	while(!fil.eof())
	{      fil.getline(S,80);
		cout<<S<<endl;
	}
}
void Rline()
{
	fstream fil;
	fil.open("Student.txt",ios::in);
	char W[80];
	while(!fil.eof())
	{   fil.getline(W,80);
		for (int i=strlen(W)-1;i>=0;i--)
		    cout<<W[i];
		    cout<<"\n";
	}
}
int main()
{	
    Create();
    Create();
    Display();
    Rline();
    return 0;
}





























Q5. WAP to count following in a given file:

a.No.of characters
b.No.of words 
c.No.of lines
d..No.of uppercase letters,lowercase letters, digits and special symbols.

ANS 5:

#include<iostream>
#include<fstream>
using namespace std;
int main()
{
     int noc=0,now=1,nol=1,uc=0,lc=0,sc=0,d=0;
     char fname[30];
     char ch;
     ofstream out;
        out.open("abc.txt");
        cout<<"Enter any data:: ";
        cin.getline(fname,30);
        out<<fname;
        out.close();
        ifstream fin;
        fin.open("abc.txt");
        fin.seekg(0,ios::beg);
     while(fin)
     {    fin.get(ch);
          if(ch!=' ' && ch!='\n')
               noc++;
          if(ch==' ')
               now++;
          if(ch=='\n')
          {
               nol++;
               now++;
          }
          if(ch>=65&&ch<=90)
		   uc++;
	      else if(ch>=48&&ch<=57)
		   d++;
		  else if(ch>=97&&ch<=122)
		   lc++;
		  else
		   sc++;
     }
     cout<<"\n Total No. of Characters  : "<<noc;
     cout<<"\n Total No. of Words       : "<<now;
     cout<<"\n Total No. of Lines       : "<<nol;
     cout<<"\n Total No. of Uppercase letters       : "<<uc;
     cout<<"\n Total No. of Lowercase Letters       : "<<lc;
     cout<<"\n Total No. of Digits       : "<<d;
     cout<<"\n Total No. of Special Characters       : "<<sc;
     fin.close();
     return 0;
}

























Q6.WAP to read and write objects to a file,using read and write functions.


ANS 6:

//C++ program to write and read object using read and write function.
#include <iostream>
#include <fstream>
 
using namespace std;
 
//class student to read and write student details
class student
{
    private:
        char name[30];
        int age;
    public:
        void getData(void)
        { cout<<"Enter name:"; cin.getline(name,30);
          cout<<"Enter age:"; cin>>age;
        }
 
        void showData(void)
        {
        cout<<"Name:"<<name<<",Age:"<<age<<endl;
        }
};
 
int main()
{
    student s;
     
    ofstream file;
 
    //open file in write mode
    file.open("aaa.txt",ios::out);
    if(!file)
    {
      cout<<"Error in creating file.."<<endl;
      return 0;
    }
    cout<<"\nFile created successfully."<<endl;
 
    //write into file
    s.getData();    //read from user
    file.write((char*)&s,sizeof(s));    //write into file
 
    file.close();   //close the file
    cout<<"\nFile saved and closed succesfully."<<endl;
 
    //re open file in input mode and read data
    //open file1
    ifstream file1;
    //again open file in read mode
    file1.open("aaa.txt",ios::in);
    if(!file1){
        cout<<"Error in opening file..";
        return 0;
    }
    //read data from file
    file1.read((char*)&s,sizeof(s));
 
    //display data on monitor
    s.showData();
    //close the file
    file1.close();
     
    return 0;
}
