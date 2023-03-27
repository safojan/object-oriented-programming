#  Virtual Functions in C++


## What are virtual Functions in c++ ?
-in simple words
Virtual function is a member function.
decleared in base class /parent class.
is redefined (overridden) by the drived/child class.
When you refer to a derived class object using a pointer or a reference to the base class, you can call a virtual function for that object and
execute the derived class’s version of the function

```
#include<iostream>
using namespace std;
  
class base {
public:
    virtual void print()
    {
        cout << "print base class\n";
    }
  
    void show()
    {
        cout << "show base class\n";
    }
};
  
class derived : public base {
public:
    void print()
    {
        cout << "print derived class\n";
    }
  
    void show()
    {
        cout << "show derived class\n";
    }
};
  
int main()
{
    base *bptr;
    derived d;
    bptr = &d;
  
    // Virtual function, binded at runtime
    bptr->print();
  
    // Non-virtual function, binded at compile time
    bptr->show();
    
    return 0;
}













```


