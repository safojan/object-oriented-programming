# Virtual Functions in C++

## What are virtual Functions in c++ ?

- In simple words
  Virtual function is a member function
  decleared in base class /parent class
  is redefined (overridden) by the drived/child class
  When you refer to a derived class object using a pointer or a reference to the base class, you can call a virtual function for that object and
  execute the derived class�s version of the function

oh the last point is a difficult one let understand it with a
simple code.

lets we have a class called animal 🐉 .

```
class animal{
	public:
	void sound(){
		cout<<"a  "<<endl;
	}
}
```

now we have a derived class dog 🐶

```
class Dog : public Animal {
public:
    void makeSound() override {
        std::cout << "The dog barks." << std::endl;
    }
};

```

in the main we have

```
 int main() {
    Dog dog;
    Animal* animalPtr = &dog;
    animalPtr->makeSound(); // calls Dog's version of makeSound()
    return 0;
}

```

The Dog class overrides the makeSound() function from Animal using the override keyword. This version of the
function prints a message saying that the dog barks.

`In the main() function, a Dog object is created. A pointer of type Animal\* is created and assigned the address of the Dog object using the & operator. Then, the makeSound() function is called on the animalPtr pointer. Since makeSound() is virtual and animalPtr points to a Dog object, the Dog version of makeSound() is executed,
which prints the message saying that the dog barks.
