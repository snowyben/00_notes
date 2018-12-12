# Virtual Function Testcode

```c++
#include <iostream>
#include <string>
using namespace std;
//base Student
class Student
{
public:
Student(int, string,float);  
void display( );
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
void Student::display( )
{
cout<<"num:"<<num<<"\nname:"<<name<<"\nscore:"<<score<<"\n\n";
}
//声明公用派生类Graduate
class Graduate:public Student
{
public:
Graduate(int, string, float, float);
void display( );
private:float pay;
};
// Graduate类成员函数的实现
void Graduate::display( )
{
cout<<"num:"<<num<<"\nname:"<<name<<"\nscore:"<<score<<"\npay="<<pay<<endl;
}
Graduate::Graduate(int n, string nam,float s,float p):Student(n,nam,s),pay(p){}
//主函数
int main()
{
Student stud1(1001,"Li",87.5);
Graduate grad1(2001,"Wang",98.5,563.5);
Student *pt=&stud1;
pt->display( );
pt=&grad1;
pt->display( );
return 0;
}
```

----------------------

[FATFOO](https://github.com/snowyben/00_notes)

<div class="footer">
&copy; 2018 FatFoo Corporation
</div>
