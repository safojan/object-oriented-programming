# Operator Overloading

In c++ we overload operators to do operations on user defined class aka class and their objects.

like we can add two integers in c++ using + now we need to find some tachnique by using it we can add two user defined data types like structures and objects

```
int a;
float b,sum;
sum=a+b;
```

Here, variables “a” and “b” are of types “int” and “float”, which are built-in data types. Hence the addition operator ‘+’ can easily add the contents of “a” and “b”. This is because the addition operator “+” is predefined to add variables of built-in data type only.

now examine this code

```
class Num{
int a;
string b;

};

int main(){
Num a,b,c;

c=a+b;

    return 0;
}

```

this code will give an error because + operator is not defined for the data type/class ,means the compiler is confused ,what to do ! so the solution is operator overloading.to do so we do operator overloading.

```
class Num{
int a;
string b;
public:
Num operator+(Num const& other){
Num result;
res.a=a+other.a;
return a;

}

};

int main(){
Num a,b,c;

c=a+b;

    return 0;
}

```
