# Ex.No:4
# Ex.Name: Write a CPP program to show how the override works using virtual functions and how it works without the virtual concept.
## Date:
## Aim:
To write a C++ program showing how function overriding works with virtual functions (runtime polymorphism) and how it behaves without virtual functions (compile-time binding).

## Algorithm:
STEP 1: Start the program.

STEP 2: Create a base class Base.

STEP 3: Declare a member function show() in the base class.

STEP 4: Create a derived class Derived that inherits publicly from Base.

STEP 5: Override the show() function in the derived class.

STEP 6: In the first case, make the show() function in the base class virtual to demonstrate runtime polymorphism.

STEP 7: In the second case, remove the virtual keyword to demonstrate compile-time binding.

STEP 8: In the main() function, create a base class pointer pointing to a derived class object.

STEP 9: Call the show() function using the base class pointer in both cases.

STEP 10: Observe the difference in output between using virtual and non-virtual functions.




## Program:
```
#include <iostream>
using namespace std;

class base
{
public:
    virtual void print(string str)
    {
        cout << str << " Base Class overridden" << endl;
    }

    void show(string str) 
    {
        cout << str << " Base Class Not overridden" << endl;
    }
};

class derived : public base 
{
public:
    void print(string str) override 
    {
        cout << str << " Derived Class Overridding" << endl;
    }

    void show(string str) 
    {
        cout << str << " Derived Class Not Overridding" << endl;
    }
};

int main()
{
    string str;
    cin >> str;

    base *p = new derived;

    p->print(str);

    p->show(str);


    return 0;
}
```


## Output:
<img width="937" height="310" alt="519126583-3594eba3-ddea-4e32-bfb4-3f7fd9c1b035" src="https://github.com/user-attachments/assets/d9083912-8c0b-4172-ad6b-7b7a3fd2fdd6" />



## Result:
With virtual function: The derived class function is called (runtime polymorphism).

Without virtual function: The base class function is called (compile-time binding).
