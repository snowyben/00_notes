# Virtual Function Testcode

For polymorphism feature in C++. If we write a virtual function in the following style equaling to zero, it will be a pure virtual function: 
1. > The base class is not allowed to be instantiated;
2. > The pure virtual function must be implemented.
```c++
    ...//in base class
    void display()=0;
    ...
```



## Test code 1

```c++
#include <iostream>
#include <string>
using namespace std;
//base Student
class Student
{
    public:
    Student(int, string,float);  
    void display();
    protected:  //derived class can access
    int num;
    string name;
    float score;
};

Student::Student(int n, string nam,float s)
{
    num=n;
    name=nam;
    score=s;
}
void Student::display()
{
    cout<<"num:"<<num<<"\nname:"<<name<<"\nscore:"<<score<<"\n\n";
}

class Graduate:public Student
{
    public:
    Graduate(int, string, float, float);
    void display();
    private:float pay;
};

void Graduate::display()
{
    cout<<"num:"<<num<<"\nname:"<<name<<"\nscore:"<<score<<"\npay="<<pay<<endl;
}
Graduate::Graduate(int n, string nam,float s,float p):Student(n,nam,s),pay(p){}

int main()
{
    Student stud1(1001,"Li",87.5);
    Graduate grad1(2001,"Wang",98.5,563.5);
    Student *pt=&stud1;
    pt->display();
    pt=&grad1;
    pt->display();
    return 0;
}
```
## Output 1
```
num:1001
name:Li
score:87.5

num:2001
name:Wang
score:98.5
```
## Test code 2
```c++
    ...// in base class
    virtual void display(); 
    ...
```
## Output 2
```
num:1001
name:Li
score:87.5

num:2001
name:Wang
score:98.5
pay=1200
```


----------------------

[FATFOO](https://github.com/snowyben/00_notes)

<div class="footer">
&copy; 2018 FatFoo Corporation
</div>
