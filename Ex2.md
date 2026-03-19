# Ex.No:2
# Ex.Name: Write A CPP program to Demonstrate on the object delegation (use integer data)
## Date:
## Aim:
To write a C++ program to demonstrate object delegation, where one class delegates a task to another class using integer data.


## Algorithm:
STEP 1: Start the program.

STEP 2: Create a class Calculator to perform arithmetic operations.

STEP 3: Declare a private integer data member in Calculator.

STEP 4: Define a public method in Calculator to read an integer value.

STEP 5: Define a method in Calculator to double the value (or perform any operation).

STEP 6: Create another class Delegator which contains an object of Calculator as a member.

STEP 7: In Delegator, define a method to delegate the operation to the Calculator object.

STEP 8: Call the method of Calculator through the Delegator object to perform the operation.

STEP 9: Display the result of the operation.

STEP 10: End the program.




## Program:
```'
#include <iostream>
using namespace std;

class A
{
    string value;

public:
    A(string val) : value(val) {}

    string getValue() const
    {
        return value;
    }
};

class B
{
    A objA; 

public:
    B(string val) : objA(val) {}

    string getValue() const
    {
        return objA.getValue();
    }
};

int main() 
{
    string a;
    cin >> a; 
    B objB(a);

    cout << objB.getValue() << endl; 

    return 0;
}

```


## Output:
<img width="469" height="265" alt="519125073-9e4440e6-906a-4c60-ba7f-7a22fdaebd88" src="https://github.com/user-attachments/assets/88d5ee99-83d8-498b-a0c9-b677f3f0285b" />



## Result:
Thus, the program successfully demonstrates object delegation, where one class delegates tasks to another class using integer data.
