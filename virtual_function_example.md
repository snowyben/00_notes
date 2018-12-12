# FatFoo notes
## For Copy
1. ①②③④⑤⑥⑦⑧⑨⑩⑪⑪⑫⑬⑭⑮⑯⑰⑱⑲⑳

## URL
1. I *get* 10 times more traffic from [Google][] than from
[Yahoo][] or [MSN][]. `printf()`

[google]: http://google.com/        "Google"
[yahoo]:  http://search.yahoo.com/  "Yahoo Search"
[msn]:    http://search.msn.com/    "MSN Search"

## Cite
1. >abc
2. >abcdef

```c++
#include <iostream>
#include <string>
using namespace std;
//声明基类Student
class Student
{
public:
Student(int, string,float);  //声明构造函数
void display( );//声明输出函数
protected:  //受保护成员，派生类可以访问
int num;
string name;
float score;
};
//Student类成员函数的实现
Student::Student(int n, string nam,float s)//定义构造函数
{
num=n;
name=nam;
score=s;
}
void Student::display( )//定义输出函数
{
cout<<"num:"<<num<<"\nname:"<<name<<"\nscore:"<<score<<"\n\n";
}
//声明公用派生类Graduate
class Graduate:public Student
{
public:
Graduate(int, string, float, float);//声明构造函数
void display( );//声明输出函数
private:float pay;
};
// Graduate类成员函数的实现
void Graduate::display( )//定义输出函数
{
cout<<"num:"<<num<<"\nname:"<<name<<"\nscore:"<<score<<"\npay="<<pay<<endl;
}
Graduate::Graduate(int n, string nam,float s,float p):Student(n,nam,s),pay(p){}
//主函数
int main()
{
Student stud1(1001,"Li",87.5);//定义Student类对象stud1
Graduate grad1(2001,"Wang",98.5,563.5);//定义Graduate类对象grad1
Student *pt=&stud1;//定义指向基类对象的指针变量pt
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
