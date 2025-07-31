```c++
#include <iostream>  
using namespace std;  
#include <string>  
class Person  
{  
public:  
    //无参数构造  
    Person()  
    {  
        cout << "Person 的无参构造函数被调用" << endl;  
    }  
    //有参构造  
    Person(int a)  
    {  
        age = a;  
        cout << "Person 的有参构造函数被调用" << endl;  
  
    }  
    //拷贝构造函数  
    Person(const Person &p)  
    {  
        age = p.age;  
        cout << "Person 的拷贝构造函数调用" << endl;  
    }  
    ~Person()  
    {  
        cout << "Person 的析构函数被调用" << endl;  
    }  
    int age;  
  
};  
  
void test01()  
{  
    //1.括号法  
//    Person p1;//默认构造函数调用  
//    Person p2(10);//有参构造函数  
//    Person p3(p2);//拷贝构造函数  
//    cout << "p2的年龄是" << p2.age <<endl;  
    //2.显示法  
//    Person p2 = Person(10);  
//    Person p3 = Person(p2);  
    //3.隐式转换法  
//    Person p4 = 10;  
//    Persoqqwn P5 = p4;  
}  
int main(){  
    test01();  
}
```