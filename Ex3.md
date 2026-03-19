# Ex.No:3
# Ex.Name: Write a CPP program to override the print() function in the base class with the print() function in the child class using the concept of virtual functions.
## Date:
## Aim:
To write a C++ program to override the print() function in the base class with the print() function in the derived class using virtual functions.


## Algorithm:
STEP 1: Start the program.

STEP 2: Create a base class named Base.

STEP 3: Declare a virtual function print() in the base class.

STEP 4: In the base class, define the print() function to display a base class message.

STEP 5: Create a derived class Derived that inherits publicly from Base.

STEP 6: Override the print() function in the derived class to display a derived class message.

STEP 7: In the main() function, create a base class pointer pointing to a derived class object.

STEP 8: Call the print() function using the base class pointer.

STEP 9: Observe that the derived class function is invoked because of virtual function mechanism.

STEP 10: End the program.





## Program:
```
#include<iostream>
using namespace std;
 
class base 
{
    public:
    string a;
    virtual void print()
    {
        cin>>a;
        cout<<a<<endl;
    }
};
 
class derived:public base
{
    public:
    string a;
    void print()
    {
        cin>>a;
        cout<<a<<endl;
    }
};
 
int main()
{
    base *bptr;
    derived dobj;
    bptr = &dobj;
    bptr->print();
    // Virtual function, binded at runtime
   
    return 0;
}
```



## Output:
<img width="617" height="239" alt="519125906-8b3c9073-5f8a-4bdd-99b0-16759dbcb24d" src="https://github.com/user-attachments/assets/9b41018d-1df1-45f7-9154-444f8fb4bd4f" />



## Result:
Thus, the program successfully demonstrates function overriding using virtual functions, where the derived class version of print() is called through a base class pointer.
