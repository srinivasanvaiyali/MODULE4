# Ex.No:5
# Ex.Name: Write a CPP program to override the print() function in the base class with the print() function in the child class using the concept of virtual functions.
## Date:
## Aim:
To write a C++ program to demonstrate the concept of virtual functions in multi-level inheritance, where each class overrides the function get_ram_space().

## Algorithm:
STEP 1: Start the program.

STEP 2: Create the base class PC.

STEP 3: Declare a virtual function get_ram_space() in the PC class.

STEP 4: Create a derived class PC_XT that inherits publicly from PC.

STEP 5: Override the get_ram_space() function in PC_XT.

STEP 6: Create another derived class PC_AT that inherits publicly from PC_XT.

STEP 7: Override the get_ram_space() function in PC_AT.

STEP 8: In the main() function, create base class pointers pointing to objects of each derived class.

STEP 9: Call get_ram_space() using base class pointers to demonstrate runtime polymorphism.

STEP 10: End the program.




## Program:
```
#include <iostream>
using namespace std;

class PC 
{
public:
    virtual void get_ram_space() 
    {
        cout << "PC has 4 GB RAM Space" << endl;
    }
};

class PC_XT : public PC 
{
public:
    void get_ram_space() override
    {
        cout << "PC_XT has 16 GB RAM Space" << endl;
    }
};

class PC_AT : public PC_XT
{
public:
    void get_ram_space() override 
    {
        cout << "PC_AT has 1 TB RAM Space" << endl;
    }
};

int main()
{
    PC *pcPtr;
    PC_AT at;
    
    pcPtr = &at;
    pcPtr->get_ram_space();  
}
```


## Output:
<img width="783" height="180" alt="519127775-6e2d2498-59ec-466c-9e11-af7004a01d93" src="https://github.com/user-attachments/assets/a6f530af-b5c2-41e4-8d69-02c37845f91f" />



## Result:
The program successfully demonstrates virtual functions in multi-level inheritance, where the correct overridden function in the derived class is invoked at runtime through a base class pointer.
