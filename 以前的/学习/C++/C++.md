# 基础
#### 整型                        内存

1. 短整型 short                 2
2. 整形 int                            4
3. 长整型 long                     4
4. 长长整型 loglong            8

**主要区别是作战内存大小不一样**

如何计算当前变量的占用内存?
*sizeof* 关键字
```c++
#include <iostream>
using namespace std;
//整型大小比较
int main(){
	cout << sizeof(short) <<endl;

	cout << sizeof(int) << endl;

	cout << sizeof(log) << endl;

	cout << sizeof(loglog) << endl;

	return 0;
}
sizeof(short) <= sizeof(int) < sizeof(log) < sizeof(loglog)
```

### 实型（浮点型）
| 数据类型   | 占用空间  | 有效数字范围     |
| ------ | ----- | ---------- |
| float  | 4byte | 7位有效数字     |
| double | 8byte | 15-16位有效数字 |
```C++

#include <iostream>
using namespace std;
//整型大小比较
int main(){
	float f1 = 3.14f
	cout << f1 << endl;
	double d1 = 3.14d
	cout << d1 << endl;
	return 0;
}
```

### 字符型
语法: char ch  - 'a';
内存:字符型变量只占用一个字节
原理：将字符转换为编码存入
创建：
```c++
#include <iostream>  
using namespace std;  
int main(){  
    //创建字符型变量  
    char ch = 'a';  
    cout << ch  << endl;  
    //内存大小  
    cout << sizeof(ch) << endl;  
    //常见错误   
//char ch2 = "b";, 创建字符型变量要用单引号  
    //a -- 97  
    //A -- 65    //char ch2 - 'abced'    
    cout << int(ch) << endl;  
}
```














### 字符串型
两种风格：
1. c风格字符串
	char str[] = "hello world";
2. c++风格字符串
	 string str2 = "hello world"
```c++
	#include <iostream>  
	using namespace std;  
	#include <string>  
	  
	int main(){  
	    string str2 = "hello world";  
	    cout << str2 << endl;  
	    return 0;  
	}
```
### 布尔类型
true -- 真
false -- 假
内存：只占用一个内存
### 数据的输入

## 运算符
+， -， *， /
```c++
  
int main(){  
    //整数  
    int a = 10;  
    int b = 20; //除数 不能为 0    cout << a % b << endl;  
    //小数不能做取模运算  
    return 0;  
  
}
```
### 前置递增，后置递增
```C++
#include <iostream>  
using namespace std;  
#include <string>  
  
int main(){  
    //前置递增  
    int a = 10;  
    int a1 = ++a * 10;  
    cout << "a=="<< a << endl;  
    cout << "a1=="<< a1 << endl;  
    //后置递增  
    int b = 20;  
    int b1 = b++*10;  
    cout << "b == " << b <<endl;  
    cout << "b1 == " << b1 <<endl;  
    return 0;  
  
}
```
·前置递增先对变量进行++再计算表达式
·后置递增先对变量进行计算表达式再++
**作业：**
前后置递减
```c++
#include <iostream>  
using namespace std;  
#include <string>  
  
int main(){  
    //前置递减 
    int a = 10;  
    int a1 = --a * 10;  
    cout << "a=="<< a << endl; //9  
    cout << "a1=="<< a1 << endl; //90  
    //后置递减  
    int b = 20;  
    int b1 = b--*10;  
    cout << "b == " << b <<endl; // 19  
    cout << "b1 == " << b1 <<endl;// 200  
  
    return 0;  
  
}
```


### 赋值运算符
![[Pasted image 20240427100836.png]]
```c++
#include <iostream>  
using namespace std;  
#include <string>  
  
int main(){  
    int a = 10;  
    a = 100;  
    cout << "a = " << a << endl;  
		  
    a = 10;  
    a *= 2;  
    cout << "a = " << a << endl;  
  
    a = 10;  
    a /= 2;  
    cout << "a = " << a << endl;  
    }
```
比较运算法
```C++
#include<iostream>
using namespace str;
int main(){
	//比较运算符
	// == 
	int a = 10;
	int b = 20;
	cout << (a == b) <<endl; //返回0，表示假
	// !=, >=, <=
}
```
### 逻辑运算符
![[Pasted image 20240427101917.png|]]
```c++
int main(){  
   int a = 10;  
    int b = 0;  
   //再C++中，除0外都是真  
   cout << !a << endl;  
   cout << (a && b) << endl;  
   cout << (a || b) << endl;  
   return 0;  
}
```
## 程序流程选择
·顺序结构
·选择结构
·循环结构
### 选择结构
单个if
```c++
int main(){  
    int score = 0;  
    cout << "请输入一个分数"<< endl;  
    cin >> score;  
    cout << "您输入的分数是："<< score << endl;  
    if (score > 600)  
    {  
        cout << "您能考上一本"<<endl;  
    }  
    return 0;  
}
```

增添else
```c++
int main(){  
    int score = 0;  
    cout << "请输入一个分数"<< endl;  
    cin >> score;  
    cout << "您输入的分数是："<< score << endl;  
    if (score > 600)  
    {  
        cout << "您能考上一本"<<endl;  
    }  
    else  
    {  
        cout << "未考上一本大学" << endl;  
    }  
    return 0;  
}
```
多个if
```c++
int main(){  
    int score = 0;  
    cout << "请输入一个分数"<< endl;  
    cin >> score;  
    cout << "您输入的分数是："<< score << endl;  
    if (score > 600)  
    {  
        cout << "您能考上一本"<<endl;  
    }  
    else if (score > 500)  
    {  
        cout << "您能考上二本大学" << endl;  
    }  
    else if (score > 400)  
    {  
        cout << "您能考上三本大学" << endl;  
    }  
    else  
    {  
        cout << "未考上一本大学" << endl;  
    }  
    return 0;  
}
```
嵌套if与语句
```c++
int main(){  
    int num1 = 0;  
    int num2 = 0;  
    int num3 = 0;  
  
    cout << "请输入小猪A的体重" << endl;  
    cin >> num1;  
  
    cout << "请输入小猪B的体重" << endl;  
    cin >> num2;  
  
    cout << "请输入小猪C的体重" << endl;  
    cin >> num3;  
    if (num1 > num2) {  
        if (num1 > num3) {  
            cout << "小猪A最重" << endl;  
        } else {  
            cout << "小猪C最重" << endl;  
        }  
    }  
    else {  
        if (num2 > num3) {  
            cout << "小猪B最重" << endl;  
        } else {  
            cout << "小猪C最重" << endl;  
        }  
    }  
    return 0;  
}

```
### 三目 运算符
创建三个变量a，b，c，将a和b作比较，将变量大的赋值给c
 ```c++
 int main(){  
    int a = 10;  
    int b = 20;  
    int c = 0;  
    //如果a > b 则返回a，否则返回b  
    c = a > b ? a : b;  
    cout << "c = " << c << endl;  
    //继续赋值捏】  
    (a > b ? a : b) = 100;  
  
    cout << "a = " << a << endl;  
    cout << "b = " << b<< endl;  
    cout << "c = " << c << endl;  
    return 0;  
}
```
(a > b ? a : b)表示如果a > b,则返回a否则返回b也可以继续赋值给当前返回的值 (a > b ? a : b) = 100; 
### switch语句
 ```c++
 int main(){  
    int score = 0;  
    cout << "请输入你的数字" << endl;  
    cin >>  score;  
    cout << "您输出的分数是：" <<score <<  endl;  
    switch (score) {  
        case 10:  
            cout << "经典" << endl;  
            break;  
        case 9:  
            cout << "也是经典" << endl;  
            break;  
        case 8:  
            cout << "还行" << endl;  
            break;  
        case 7:  
            cout << "也还行" << endl;  
            break;  
        default:  
            cout << "都是烂片" << endl;  
            break;  
    }  
    return 0;  
}
```

### 循环语句
```c++
int main(){  
    int num = 0;  
    //while()中写入循环条件  
    while(num <10){  
        cout << num <<endl;  
        num ++;  
    }  
    return 0;  
}
```
| 在执行循环的时候，注意循环的条件，也要防止死循环.
作业：猜数字大小
```c++
int main(){  
   int num = rand()%100 + 1;  
   int num1 = 0;  
   while(1){  
       cout << "请输入你的数字" <<endl;  
       cin >> num1;  
       if (num1 > num){  
           cout << "您输入的数字大了，请小一点" << endl;  
       }  
       else if (num1 < num){  
           cout << "您输入的数字太小了，请大一点" <<endl;  
       }  
       else{  
           cout << "恭喜你输入的数字正确" << endl;  
           break;  
       }  
   }  
   return 0;  
}
```

**do while 循环**
先执行一次do内的内容，再循环
水仙花
```c++
int main(){  
    int num =100;  
  
    do  
    {  
        int a = 0;  
        int b = 0;  
        int c = 0;  
  
        a = num % 10;  
        b = num /10 % 10;  
        c = num /100 %10;  
        if (a*a*a +b*b*b +c*c*c == num)  
        {  
            cout << num <<endl;  
        }  
        num++;  
    }while (num < 1000);  
    return 0;  
}
```
**for  循环**
```c++
int main(){  
    for (int i = 0; i <10; i++)  
    {  
        cout <<i <<endl;  
    }  
    return 0;  
}
```
 **嵌套循环**
 ```c++
 int main(){  
    //外层循环  
    for (int i = 0; i < 10; i++)  
    {   //内层循环  
        for (int j = 0; j < 10; j++)  
        {  
            cout << "*" ;  
        }  
        cout << endl;  
    }  
    return 0;  
}****
```
9*9乘法表
```c++
int main(){  
    for (int i = 1; i < 10; i++)  
    {  
        for (int j = 1;j <= i; j++)  
        {  
            cout << j << "*" <<i<< "="<< j*i<< " ";  
        }  
        cout << endl;  
  
    }  
    return 0;  
}
```
### 跳转语句
·break 跳出本次循环
```c++
int main(){
	for (int i = 0;i < 10;i++)
	{
		for (int j = 0; j < i;j++)
		{
			if (j == 5)
			{
			 break
			}
		}
	}
}
```
·continue  跳过本次循环中未执行的语句 
```c++
int main(){  
    for (int i = 0; i<100;i++)  
    {//如果是技术就输出  
        if (i % 2 == 0)  
        {  
            continue;  
        }  
        cout << i <<endl;  
    }  
    system("pause");  
    return 0;  
}
```
```
```
**goto语句**
执行goto语句，先打标记，在执行过程中会跳转到打标记的地方
## 数组
### 数组定义
	1.数组特点：
		放在一块连续的内存空间中。数组中的每个元素都是相同数据类型(整形，浮点型等)
	2.创建数组
		·数据类型 + 数组名[数组长度];	
		·数据类型 + 数组名[数组长度] = {value1,value2,value3};	
		·数据类型 + 数组名[] = {value1,value2,value3};	
		
```c++
int main(){  
    int arr[5] = {10,20,30,40l,50};  
    for ( int i = 0;i < 5; i++)  
    {  
        cout << arr[i] << " " ;  
  
    }  
    cout << endl;  
    return 0;  
}
```
	3.一维数组名称的用途：1统计整个数字在内存中的长度

						![[Pasted image 20240429110747.png|250]]

						2可以获取数组在内存中的首地址

						![[Pasted image 20240429111738.png]]


数组的逆置
冒泡排序 
有两点注意
	1.循环的次数是元素个数减一
	2.每次循环两两交换，交换次数是元素个数减去当前循环的次数减一
```c++
int main(){  
    int a[9] = {4,2,8,0,5,7,1,3,9};  
    cout << "排序前： "<< endl;  
    for (int i = 0;i < 9; i++)  
    {  
        cout << a[i] << endl;  
    }  
//循环次数  
    for (int i = 0 ; i < sizeof(a)/sizeof(a[0])-2; i++)  
    {//每次对比次数  
        for (int j = 0;j < sizeof(a)/sizeof(a[0])-2-i;j++)  
        {  
            if (a[j] > a[j+1])  
            {  
                int temp = a[j];  
                a[j] = a[j+1];  
                a[j+1] = temp;  
  
            }  
        }  
    }  
    cout << "排序前： "<< endl;  
    for (int i = 0;i < 9; i++)  
    {  
        cout << a[i] << endl;  
    }  
    return 0;  
}
```
### 二维数组
```c++
int main(){  
    int arr1[2][3] =  
    {  
            {1,2,3},  
            {4,5,6}  
    };  
    int arr2[2][3] = {1,2,3,4,5,6};  
    int arr3[][3] = {1,2,3,4,5,6};  
    }
```
二维数组的几种表示方式
## 函数
函数的基本定义
```c++
int add (int num1,int num2)  
{  
    //函数体语句  
    int sum = num1 + num2;  
    return sum;  
    //return表达式  
}
//函数的调用

int main(){
	int a = 10;
int b = 20;

int c = add(a, b);
cout << "c = " << c <<endl;

return 0;
}






```
函数的声明：
确保函数存在
int 函数名(形参)

**函数的份文件**
1. 创建.h后缀名的头文件
2. 创建.cpp后缀名的源文件
3. 在头文件中写函数的声明
4. 在源文件中写函数的定义
## 指针
### 指针基础
指针就是个地址
如何去定义个指针
```c++
int main(){  
    //1.定义指针  
    int a = 10;  
    int *p;  
    p = &a;  
    cout << "a的地址" << &a << endl;  
    cout << "指针p为" << p << endl;  
    //2.使用指针  
    cout << "p = " << *p <<endl;  
    return 0;  
}
```
指针的内存空间
```c
int main(){  
    //1.定义指针  
    int a = 10;  
    int * p = &a;  
    cout << "sizeof (int *) = " << sizeof(int *) << endl;  
    cout << "sizeof (int *) = " << sizeof(float *) << endl;  
    cout << "sizeof (int *) = " << sizeof(double *) << endl;  
    cout << "sizeof (int *) = " << sizeof(char *) << endl;  
    return 0;  
}
```
空指针
```c++
int main(){  
    int *p = NULL;  
    *p = 100;  
    cout << *p <<endl;  
    return 0;  
}
```
不可访问

野指针
```c
int main(){  
    int *p = (int *)0x1100;  
    cout << *p <<endl;  
    return 0;  
}
```
超出范围


### const修饰指针
常量指针
const int * p = &a
特点：指针指向的值不可以改，指针的指向可以改
指针常量
int *  const p2  =10&a;
特点： 指针的指向不可以改，指针指向的值可以改
const int const * p = &a;
```c++
int main(){  
    int a = 10;  
    int b = 10;  
    //1.常量指针  
    const int *p = &a;  
    p  = &b;  
    //2.指针常量  
    int * const  p2 = &a;  
    * p2 = 20;  
    //3、既修饰指针有修饰常量  
    const int * const p3 = &a;  
//    *p3 = 100;  
//    p3 = &b;  
  
  
}
```
### 指针和数组
```c++
int main(){  
    int arr[5] = {1,2,3,4,5};  
    int *p = arr;  
//    cout << "数组中第一个元素的位置：" << *p <<endl;  
//    p++;  
//    cout << "数组中第二个元素的位置：" << *p <<endl;  
    for (int i = 0;i < 5;i++)  
    {  
        cout << "数组中第"<< i +1<< "个元素的地址" << *p << endl;  
        p++;  
    }  
    return 0;  
}
```
### 值传递和地址传递
地址传递可以改变参数
```c++
void swap1(int a , int b)  
{  
    int temp = a;  
    a = b;  
    b = temp;  
  
  
}  
void swap2(int *p1, int * p2)  
{  
    int temp = *p1;  
    *p1 = *p2;  
    *p2 = temp;  
  
}  
  
int main(){  
    int a = 10;  
    int b =20;  
    swap1(a,b);  
    cout << "a = " << a << endl;  
    cout << "b = " << b << endl;  
    swap2(&a,&b);  
    cout << "a = " << a << endl;  
    cout << "b = " << b << endl;  
    return 0;  
}
```
## 结构体
定义：结构体属于用户自定义的数据类型，一些列类型集合组成的类型
关键字： struct

定义结构体时的关键字是struct，不可以省略，创建结构体变量事，struct可以省略
```c++
struct student  
{   //姓名  
    string name;  
    //年级  
    int age;  
    //分数  
    int score;  
};  
  
int main(){  
    struct student s1;  
    s1.name = "张三";  
    s1.age = 18;  
    s1.score = 100;  
  
    cout << "姓名：" << s1.name << "年龄：" << s1.age << "分数:" << s1.score << endl;  
  
    return 0;  
}****
```
### 结构体数组
创建的结构体如果数量多了怎么办
直接在int main() 中改
```c++
int main(){  
    struct Student stuArrary[3] =  
            {  
                    {"张三",18,100},  
                    {"李四",28,99},  
                    {"王五",38,66}  
            };  
    stuArrary[2].name = "赵六";  
    for (int i = 0;i<3;i++)  
    {  
        cout <<"姓名：" << stuArrary[i].name  
        <<"年龄：" << stuArrary[i].age  
        <<"分数" << stuArrary[i].score<<endl;  
    }  
    return 0;  
}
```
### 结构体指针
· 创建结构体变量
·通过指针指向结构体变量
· 通过指针访问结构体变量中的数据
```c++
int main(){  
    Student  s ={"张三",18, 100};  
    Student *p = &s;  
    cout << "姓名："<< p->name << "年龄：" << p->age << "分数：" << p->score<< endl;  
    return 0;  
  
  
  
}
```
### 结构体嵌套结构体
·先创建需要被嵌套的结构体，再将创建的结构体放入前提哦啊的结构体中
```c++
struct Student  
{   //姓名  
    string name;  
    //年级  
    int age;  
    //分数  
    int score;  
};  
struct teacher  
{  
    string name;  
    int id;  
    struct Student std;  
  
};  
  
int main(){  
    teacher t;  
    t.name = "老王";  
    t.id = 007;  
    t.std.name = "小三";  
    t.std.age = 18;  
    t.std.score = 100;  
    cout << t.name << t.id << t.std.name << t.std.age <<t.std.score <<endl;  
    return 0;  
  
}
```
### 结构体做函数参数
·值传递只改变形参不改变实参
· 地址传递可以改变实参
### const在结构体中的使用
·使用指针来村存储信息，内存小，利用const修饰指针可以让实参不发生变化。
```c++
struct Student  
{   //姓名  
    string name;  
    //年级  
    int age;  
    //分数  
    int score;  
};  
struct teacher  
{  
    string name;  
    int id;  
    struct Student std;  
  
};  
//1.值传递；  
void printStudent1(const Student *s)  
{  
//    s->age = 100;  
    cout << "子函数中打印 姓名：" << s->name <<"年龄" << s->age << "分数"<< s->score <<endl;  
}  
//2.地址传递；  
void printStudent2(struct Student *p)  
{  
    cout << "子函数中打印 姓名：" << p->name <<"年龄" << p->age << "分数"<< p->score <<endl;  
  
}  
int main(){  
    //创建结构体  
    struct Student s ={"张三", 15,90};  
  
    printStudent1(&s);
```
## 通讯录管理

# 进阶
### 内存分区模型
![[Pasted image 20240506095905.png]]


	在程序编译后，生成了exe可执行程序，未执行该程序前分为两个区域
		代码区：
		存放CPU执行的机器指令
		代码区特点：1️⃣共享的2️⃣只读的
		全局区：
		全局变量和静态变量存放在此，全局区包含了常量区
		1️⃣该区域的数据在程序结束后由操作系统释放
	三种变量：
		1️⃣全局变量
			在函数体外
		2️⃣局部变量
			在函数体内
		3️⃣常量变量
			1.字符串常量
			cout << "字符串常量" << "hello world" << endl;
			2.const修饰变量
				const修饰的全局变量，const修饰的局部变量。

![[Pasted image 20240506101804.png]]
	
			栈区
			🈲不要返回局部变量的地址
			堆区
			在程序运行时由程序员管理内存决定是否释放
		new操作
		int *func()  
		{  
		    int *p = new int(10);  
		    return p;  
		}
		

## 引用
给变量起别名
数据类型 &变量 = 数据
```c++
int main(){  
    int a = 10;  
    int &b = a;  
  
    cout << "a = " <<a <<  endl;  
    cout << "b = " << b << endl;  
  
     b = 100;  
  
    cout << "a = " << a << endl;  
    cout << "b = " << b << endl;  
}
```
1️⃣引用必须初始化
2️⃣引用初始化后，不可以更改😩
### 引用做参数
```c++
void myswap03(int &a, int &b)  
{  
    int temp = a;  
    a = b;  
    b = temp;  
}
int main(){  
    int a = 10;  
    int b = 20;  
  
//    myswap01(a,b);  
//    myswap02(&a, &b);  
    myswap03(a, b);  
    cout << "a = " <<a <<  endl;  
    cout << "b = "<< b << endl;  
}
```
### 引用做返回
```c++
int& test01()  
{  
    static int a = 10;  
    return a;  
}  
  
int main() {  
    int &ref2 = test01();  
    cout << "ref2 = " << ref2 << endl;  
    cout << "ref2 = " << ref2 << endl;  
  
    test01() = 100;  
    cout << "ref2 = " << ref2 << endl;  
    cout << "ref2 = " << ref2 << endl;  
  
}
```
### 引用的本质  
### 常量引用
```c++
void showValue(const int& v)  
{  
    cout << v << endl;  
}  
	  
int main(){  
    const int& ref = 10;  
  
    cout << "ref = " << ref << endl;  
    int a = 10;  
    showValue(a);  
  
    cout << "a = " << a << endl;  
}
```

--- 
常量引用：
const int& ref, 不能修改指针值，只能修修改指针指向。
函数定义的形参也要用const修饰
## 函数提高
### 函数默认参数
	函数默认参数 func（int a, int b = 10, int c =20）
	声明和实现只能有一个有参数

```c++
int func(int a , int b );  
  
int func(int a = 20, int b = 10)  
{  
    return a+ b;  
}  
int main(){  
//    cout << func(10) << endl;  
    cout << func() << endl;  
  
}
```
### 函数占位参数
语法： 返回值类型 函数名 （数据类型）{}
在调用函数时也需要穿如此相同数据类型的元素
```c++
void func(int a, int)  
{  
    cout << "this is a func" << endl;  
}  
int main(){  
//    cout << func(10) << endl;  
    func(10,1);  
  
}
```
## 函数重载
### 概念
函数名可以相同，提高复用性
条件：
·同一个作用域下
· 函数名称相同
· 函数参数类型不同，或者个数不同，顺序不同
**注意**
函数的返回值不能作为函数重载的条件，只能用void定义函数。
```C++
void func()  
{  
    cout << "调用1" << endl;  
}  
void func(int a)  
{  
    cout << "调用(int a)2" << endl;  
}  
void func(int a, double b)  
{  
    cout << "调用(int a, double b)2" << endl;  
}  
int main(){  
    func();  
    func(10);  
    func(10,3.12);  
}

```
### 函数重载的注意事项
1.引用作为函数重载的参数
```C++
void func(const int& a)  
{  
    cout << "func(const int& a)" << endl;  
}  
  
void func(int& a)  
{  
    cout << "func(int& a)" << endl;  
}  
  
int main(){  
    int a = 10;  
    func(a);  
    func(10);  
}
```
可以用常量修饰表示不同的参数
const int &a
int &a =10;
相当于创建一个临时变量:
int temp = 10;
	const int &a = temp;
2.函数重载碰到默认参数
在调用函数时添加默认参数的数据
## 类和对象

```c
C++面向对象的三大特性：封装，继承，多态
1.封装
	封装的意义：
	·将属性和行为作为一个整体
	·类在设计封装
	//访问权限
	//三种
	共有 public 成员 类内可以访问，类外可以访问
	保护 protected 成员 类内可以访问 类外不可以访问，儿子可以访问父类中的保护内容
	私有 private 成员 类内可以访问 类外不可以访问， 儿子不可以访问父亲的私有内容
	struct 和 private的区别是一个可以访问类外一个不可以访问类外

class Person  
{  
public:  
  
    void setname(string name)  
    {  
        m_Name = name;  
    }  
    string getname()  
    {  
        return m_Name;  
    }  
  
    int getage()  
    {  
        return m_Age;  
    }  
  
    void setidol(string idol)  
    {  
        m_Idol = idol;  
    }  
private:  
    //私有访问  
    string m_Name; //可读可写  
    int m_Age = 18; //只读  
    string m_Idol; //只写  
};  
  
int main(){  
    Person p1;  
    p1.setname("张三");  
    cout << "设置的名字是" << p1.getname() << endl;  
    cout << p1.getage() << endl;  
  
  
}
```
上述代码表示了在私有访问时各种变量的可读可写性，可读get，可写set
``

1.[[立方体的面积和体积]]


### 对象的初始化和清理
![[Pasted image 20240510093259.png]]

#### 构造函数的分类和调用
![[Pasted image 20240510100118.png|400]]
[[test01]]
#### 拷贝构造函数
![[Pasted image 20240510140645.png]]
 
#### 深拷贝与浅拷贝
浅拷贝是简单的赋值拷贝操作。深拷贝是在堆区重新申请空间,进行拷贝操作.
利用指针
#### 初始化列表
```python
public:  
    Person(string name, string pName):m_Phone(pName), m_Name(name)
```
#### 对象成员
#### 静态成员
· 静态成员变量
	所有对象共享一份数据
	在编译阶段分配内存
	类内声明，类外初始化
· 静态成员函数
	所有对象共享一个函数
	静态成员只能访问静成员变量
共有属性和私有属性，私有属性静态成员变量和函数都不能访问
```C++
class Phone  
{  
public:  
    Phone(string name)  
    {        m_PhoneName = name;  
        cout << "Phone构造" << endl;  
    }  
    ~Phone()  
    {  
        cout << "Phone析构" << endl;  
    }  
  
    string m_PhoneName;  
};  
class Person  
{  
public:  
    Person(string name, string pName):m_Phone(pName), m_Name(name)  
    {  
        cout << "Person构造" << endl;  
    }  
    ~Person()  
    {  
        cout << "Person沟西" << endl;  
    }  
  
    void playGame()  
    {  
        cout << m_Name << "使用" << m_Phone.m_PhoneName << endl;  
    }  
    Phone m_Phone;  
    string m_Name;  
  
};  
  
void test01()  
{  
    Person p("张三", "苹果MAX");  
    p.playGame();  
  
};  
  
int main(){  
    test01();  
  
    return 0;  
}
```
### 对象模型和this指针
非静态成员变量 属于类的对象
 静态成员变量 不属于类的对象 
 每个成员函数内都有个this指针
·this指针
	1.当格式不规范可以用this指针来区别
	2.可以返回this指针，但要解引用
```c++
class Person  
{  
public:  
    Person(int age)  
    {  
        this->age = age;  
    }  
    Person& PersonAddAge(Person &p)  
    {  
        this->age += p.age;  
        return *this;  
    }  
  
    int age;  
};  
//int Person::m_B = 0;
}  
void test02(){  
    Person p1(10);  
  
    Person p2(10);  
  
    p2.PersonAddAge(p1).PersonAddAge(p1).PersonAddAge(p1);  
  
    cout << "p2的年龄为："<< p2.age << endl;  
}  
int main(){  
    test02();  
}
```
#### 空指针访问成员函数
```c++
public:  
    void printPerson()  
    {  
        cout << "this is a person" << endl;  
    }  
    void showPerson()  
    {  
        if (this == NULL)  
        {  
            return;  
        }  
        cout <<"age = " << this->m_Age << endl;  
    }  
    int m_Age;  
  
};  
void test01()  
{  
    Person * p = NULL;  
  
    p->printPerson();  
  
    p->showPerson();  
};  
int main(){  
    test01();  
}
```
当类中只定义了成员变量，用空指针想要返回一个成员变量是错误的，指针本身就为空，所指向的成员变量也是个空，所以我们会用一个if语句来判断指针。
#### const修饰成员函数
1.常函数
·在成员函数后加一个const，其中的属性不能被修改（指针变为const Person * const this）
·如果要修改成员属性可以加关键词mutable
```c++
class Person  
{  
public:  
    void showPerson()  
    {  
        this->m_Age = 100;  
    }  
    int m_Age; 
    
      void showPerson1() const
    {  
        this->m_Bge = 100;  
    }  
     mutable int m_Bge;
};
```
2.常对象
在声明对象前加一个const成该对象为常函数
常对象只能调用常函数，但可以修改静态变量的值，只需在成员属性前加上static
### 友元
友元的三种方法
1. 全局函数做友元；
1. 类做友元；
2. 成员函数做友元；

什么是友元：可以让一个函数或者类访问另一个类中的私有成员
关键字为friend
**全局函数做友元**
```c++
class Buliding  
{  
    friend void goodgay(Buliding *buliding);  
public:  
    Buliding()  
    {  
        m_SittingRoom = "客厅";  
        m_BedRoom = "卧室";  
  
    }  
public:  
    string m_SittingRoom;  
private:  
    string m_BedRoom;  
};  
//全局函数  
void goodgay(Buliding *buliding)  
{  
    cout << "好基友全局函数访问" <<buliding->m_SittingRoom << endl;  
    cout << "好基友全局函数访问" <<buliding->m_BedRoom << endl;  
}  
void test01()  
{  
    Buliding buliding;  
    goodgay(& buliding);  
};  
int main(){  
    test01();  
}
  
```c++
class Building;  
class GoodGay  
{  
public:  
    GoodGay();  
    void visit();  
  
    Building * building;  
};  
  
class Building  
{  
public:  
    friend class GoodGay;  
    Building();  
public:  
    string m_SittingRoom;  
private:  
    string m_BedRoom;  
};  
  
Building::Building()  
{  
    m_SittingRoom = "客厅";  
    m_BedRoom = "卧室";  
}  
  
GoodGay::GoodGay()  
{  
    building = new Building;  
}  
void GoodGay::visit()  
{  
    cout << "好基友类正字啊访问" <<building->m_BedRoom << endl;  
}  
void test01()  
{  
    GoodGay gg;  
    gg.visit();  
}
```
在成员函数内作友元
```c++
class Building;  
class GoodGay  
{  
public:  
    GoodGay();  
  
    void visit();  
    void visit2();  
  
    Building * building;  
};  
class Building  
{  
    friend void GoodGay::visit();  
public:  
    Building()  
    {  
        m_SittingRoom = "客厅";  
        m_BedRoom = "卧室";  
    }  
public:  
    string m_SittingRoom;  
private:  
    string m_BedRoom;  
};  
  
  
GoodGay::GoodGay()  
{  
    building =  new Building;  
}  
void GoodGay::visit()  
{  
    cout << "visit函数访问：" <<building->m_SittingRoom<< endl;  
    cout << "visit函数访问：" <<building->m_BedRoom<< endl;  
}  
  
void GoodGay::visit2()  
{  
    cout << "visit2函数访问：" <<building->m_SittingRoom<< endl;  
}  
void test01()  
{  
     GoodGay gg;  
    gg.visit();  
    gg.visit2();  
}  
int main(){  
    test01();  
}
```
### 运算符重载
#### 加号运算符重载
+

```c++
class Person  
{  
public:  
    Person(){};  
    Person(int a, int b)  
    {  
        this->m_A = a;  
        this->m_B = b;  
    }  
    Person operator+(const Person &p)  
    {  
        Person temp;  
        temp.m_A = this->m_A + p.m_A;  
        temp.m_B = this->m_B + p.m_B;  
        return temp;  
    }  
  
public:  
    int m_A;  
    int m_B;  
};
```
	定义一个operator +（指针地址）,将指针的值和当前this指针指向的属性进行加法的操作存到temp里
#### 左移运算符重载
<<
当输入
$cout <<p << endl;$ 时若只输出前半部分，该如何操作
```c++
ostream& operator<<(ostream &count, Person & p)  
{  
    cout << "m_A = "<< p.m_A << " m_B = " << p.m_B;  
    return count;  
}
```
利用operator(cout的引用， p的引用)


#### 递增运算符重载
++
* 前置++
	先加
* 后置++
	后加
```c++
int a = 10;
前置++
cout << ++a << endl; //11
cout << a << endl;  //11
cout << a++ << endl; //10
cout <, a << endl; // 11
```


#### 赋值运算符重载
=
在p2 = p1时，会将p1的值传递给p2，但此时两者指向同一个内存，在析构函数中释放该内存时，p1会释放一次，p2也释放一次，这就造成了重复释放（p1，p2在释放内存时是独立进行的，互相并不影响）
![[Pasted image 20240529091257.png]]
利用深拷贝来重新申请一块新的区间，若有多个相同的赋值对象，运用链式编程思想，返回解引用对象。
```c++
class Person  
{  
public:  
    Person(int age)  
    {  
        m_Age = new int (age);  
    }  
    ~Person()  
    {  
        if (m_Age != NULL)  
        {  
            delete m_Age;  
            m_Age = NULL;  
        }  
    }  
    Person& operator=(Person &p)  
    {  
        if (m_Age != NULL)  
        {  
            delete m_Age;  
            m_Age = NULL;  
        }  
        //深拷贝  
        m_Age = new int(*p.m_Age);  
        return *this;  
    }  
    int *m_Age;  
};
```
#### 关系运算符重载
想要判断p1 == p2，也就是该数据类型中的所有成员属性都相同，在类中添加bool函数来返回true 或者false
```c++
bool operator==(Person &p)  
{  
    if (this->m_Age == p.m_Age && this->m_Name == p.m_Name)  
    {  
        return true;  
    }  
    else  
    {  
        return false;  
    }  
}
```

#### 函数调用运算符重载
()
```c++
class MyString  
{  
public:  
    void operator()(string text)  
    {  
        cout << text << endl;  
    }  
};  
void test01()  
{  
    MyString myString;  
    myString("hello world");  
}  
class MyAdd  
{  
public:  
    int operator()(int num1, int num2)  
    {  
        return num1 + num2;  
    }  
};  
void test02()  
{  
    MyAdd myAdd;  
    int res = myAdd(10,10);  
    cout << res << endl;  
} 
```
## 继承
语法：class A ：public B；
A类称为子类或派生类
B类称为父类或基类

A可以继承B中public的属性
```c++
class BasePage  
{  
public:  
    void top()  
    {  
        cout << "this is top" << endl;  
    }  
    void footer()  
    {  
        cout << "this is footer" << endl;  
    }  
    void left()  
    {  
        cout << "this is left" << endl;  
    }  
  
};
```
### 继承方式
![[Pasted image 20240530142210.png]]
在继承的时候子类都不可以访问父类中private的部分
在测试时
·共有继承不变
·保护继承，其中公有部分变为保护部分，不可以修改
·私有继承，其中公有和保护部分都不可以被访问
子类的内存也包含父类所继承过来的
### 析构顺序
![[Pasted image 20240530153118.png]]
运行结果为
![[Pasted image 20240530153202.png]]
表明构造子类时先构造父类
### 继承同名函数处理方式
在coding过程中，如果子类和父类出现了同名的成员，test中是调用子类的还是父类。
·父类和子类在构造后若要访问子类同名函数，直接访问，因为子类成员是在父类成员之后构造完成的
·若要访问父类的同名函数，加上弗雷德作用域即可
成员分为成员属性和成员函数。都是一样的访问方式
在成员前加上作用域

对于静态成员也是一样
静态成员
类内声明，内外初始化，
访问静态成员有两种方式：
·通过对象访问
·通过类访问
Son::func() //通过Son访问func函数
Son::Base::func() //通过Son访问Base作用下的func，
两个：：不同
![[Pasted image 20240530171038.png]]
## 多态
去完成某个行为时，不同对象会做出不同的状态
![[Pasted image 20240530184724.png]]
### 纯虚函数和抽象类
在多态中，通常父类虚函数的实现是毫无意义的，主要是调用子类重写的内容，因此可以将虚函数改为纯虚函数

	语法 `vitrual 返回值类型 函数名 （参数列表）= 0`
包含纯虚函数的类也称为抽象类

特点：
·无法实例化对象
· 子类必须重写抽象类中的纯虚函数，否则也属于抽象类
### 1文件的读写
文件操作：
文件类型1️⃣文本文件2️⃣二进制文件
流对象
1. ofstream写操作
2. ifstream读操作
3. fstream读写操作
#### 写文件
 包含头文件#include  < fstream >
  在创建的函数体中创建流对象 : ofstream 对象名
指定方式打开写内容 关闭文件
### 读文本文件

创建流对象
按指定方式打开文件
	1.判断文件是否存在
	2.若存在，读取文件
	3.关闭文件
```c++
void test()  
{  
    ifstream ifs;  
    ifs.open("text.txt", ios::in);  
    if (!ifs.is_open())  
    {  
    cout << "文件打开无效" << endl;  
    return;  
    }  
    //读文件第一种  
//    string buf;  
//    while (getline(ifs,buf))  
//    {  
//        cout << buf << endl;  
//    }  
    char c;  
    while ((c = ifs.get()) != EOF) // end of file;  
    {  
        cout <<  c;  
    }  
}  
int main(){  
    test();  
}
```
#### 读写二进制文件
二进制的方式创建流对象==ifstream ifs("person.txt",ios::in | ios::binary);==
读文件
==ifs.read((char *)&p, sizeof(p));==
用二进制创建写文件的流对象
==ofstream ofs(" person.txt",ios::out|ios::binary);//二进制文件对象==
```c++
class Person  
{  
public:  
    char m_Name[64];  
    int m_Age;  
};  
  
void test01()  
{  
    ofstream ofs(" person.txt",ios::out|ios::binary);//二进制文件对象  
//    ofs.open("person.txt", ios::out| ios::binary);  
    Person p = {"张三", 18};  
    ofs.write((const char *)&p, sizeof(p));  
    ofs.close();  
}  
void test2()  
{  
    ifstream ifs("person.txt",ios::in | ios::binary);  
    if (!ifs.is_open())  
    {  
        cout << "文件打开失败" << endl;  
    }  
    Person p;  
    ifs.read((char *)&p, sizeof(p));  
    cout << "姓名 ；"<< p.m_Name <<"年龄 :" << p.m_Age<<endl;  
  
  
}
```
``
# c++提高
## 模板
	语法：template<typename T>
	函数声明或定义
```c++
template<typename T>
void swapnum(T& a, T & b)
{
	temp = a;
	a = b;
	b = temp;
}
void test()
{
	int a = 10;
	int b = 20;
	//利用模板自动推导类型
	swapnum(a,b);
	//显示指定类型
	myswap<int>(a, b);
	cout << "a = " << a << endl;
	cout << "b = " << b << endl;

}
```
## 模板实例：排序
```c++
template<class T>  
void bubbleSort(T&a, T&b)  
{  
    T temp = a;  
    a = b;  
    b= temp;  
}  
//selectort  
template<class T>  
void selectSort(T arr[], int len)  
{  
    for (int i = 0; i < len; i++)  
    {  
        int max = i;  
        for (int j = i + 1; j< len;j ++)  
        {  
            if (arr[max] < arr[j])  
            {  
                max = j;  
            }  
        }  
        if (max != i)  
        {  
            bubbleSort(arr[max], arr[i]);  
        }  
    }  
}  
template <class T>  
void printArray(T arr[], int len)  
{  
    for (int i = 0;i < len; i++ )  
    {  
        cout << arr[i] << " ";  
  
    }  
    cout << endl;  
}  
void test01()  
{  
    char charArr[] = "bdasd";  
    int num = sizeof(charArr) / sizeof(char);  
    selectSort(charArr,num);  
    printArray(charArr ,num);  
}  
void test02()  
{  
    int Arr[] = {2,4,45,6,4,1};  
    int num = sizeof(Arr) / sizeof(Arr[0]);  
    selectSort(Arr,num);  
    printArray(Arr, num);  
}

```
## 普通函数与模版函数
使用普通函数可随时发生自动类型转换
调用模板函数时，利用自动类型推导，不会发生隐式类型转换，需要用显示指定类型
```c++
void test()  
{  
    int a = 10;  
    int b = 20;  
    char c = 'A';  
    cout << myAdd01(a, b) << endl;  
    ==cout << myAdd01<int>(a, c) << endl;==  
    cout << myAdd02(a, b);  
}

```
### 调用规则
```c++
  
void myPrint(int a ,int b)  
{  
    cout << "普通函数在调用" << endl;  
}  
template <class T>  
T myPrint(T a , T b)  
{  
    cout << "模板函数在调用" << endl;  
}  
template <class T>  
T myPrint(T a , T b,T c)  
{  
    cout << "模板函数在调用" << endl;  
}  
void test()  
{  
    int a;  
    int b;  
  
//    myPrint<>(a, b);  
    myPrint(a, b ,100);  
}

```
```c++
class Person  
{  
public:  
    Person(string name, int age)  
    {  
        m_Name = name;  
        m_Age = age;  
    }  
    string m_Name;  
    int m_Age;  
};  
template<class T>  
bool myCompare(T a, T b)  
{  
    if (a == b)  
    {  
        return true;  
    }  
    else  
    {  
        return false;  
    }  
}  
template<> bool myCompare(Person &p1, Person &p2)  
{  
    if (p1.m_Name == p2.m_Name && p1.m_Age == p2.m_Age)  
    {  
        return true;  
    }  
    else  
    {  
        return false;  
    }  
}  
  
void test01()  
{  
    int a = 10;  
    int b = 20;  
  
    bool ret = myCompare(a, b);  
    if (ret)  
    {  
        cout << "a == b" << endl;  
    }  
    else  
    {  
        cout << "a != b" << endl;  
    }  
}
```
## 类模板
	语法：template<NameType> <>中表示类名中要传入的参数

```c++
template<class NameType, class AgeType>  
class Person  
{  
public:  
    Person(NameType name, AgeType age)  
    {  
        this->m_Name = name;  
        this->m_Age = age;  
    }  
    void showPerson()  
    {  
    cout << "Name : " << this->m_Name << "Age : " << this->m_Age << endl;  
    }  
public:  
    NameType m_Name;  
    AgeType m_Age;  
};
```
上面是一个Person类中有Name和Age属性的类模板
在调用时
```C++
void test()  
{  
    Person<string, int>person("Tom", 13);  
    person.showPerson();  
}
```
·类模板只能用显示指定类型方式：没有隐式方式，参数类型必须自己定义
·类模板中的模板参数可以有默认参数

	类模板中的成员函数并不是一开始就创建的，只有在调用后才会创建。
### 类模板对象做函数参数
三种
1.传入指定参数 传入对象模板
2.参数模板化 template<class T1, class T2>
3.整个类模板化 template< class T>

```c++
//1
void printPerson(Person<string, int> &p)  
{  
    p.showPerson();  
}
//2
template<class T1, class T2>  
void pintPerson2(Person<T1,T2> &p)  
{  
    p.showPerson();  
    cout << "T1的类型是" << typeid(T1).name() << endl;  
    cout << "T1的类型是" << typeid(T1).name() << endl;  
}
//3
template<class T>  
void printPerson(T &p)  
{  
   p.showPerson();  
}

```
### 类模板与继承
当类模板继承的父类是模板时，要指出父类模板的类型
```c++
template<class T>  
class Base  
{  
    T m;  
};  
  
class Son :public Base<int>  
{  
  
};
```
想要更改父类模板的类型，继承的子类也必须是一个模板
```c++
template<class T1, class T2>  
class Son2 : Base<T2>  
{  
public:  
    Son2()  
    {  
        cout << typeid(T1).name() << endl;  
        cout << typeid(T2).name() << endl;  
    }  
};
```
### 类模板成员函数类外实现
```c++
//构造函数  类外实现  
template<class T1, class T2>  
Person<T1, T2>::Person(T1 name, T2 Age)  
{  
   m_Name =name;  
   m_Age = Age;  
}  
  
//成员函数 类外实现  
template<class T1, class T2>  
void Person<T1, T2>::showPerson(){  
    cout << "姓名" << this->m_Name << "年龄" << this->m_Age << endl;  
}
```
###  类模板和友元
·类模板配合友元函数的类内和类外实现
类内实现：
## STl
### 基本概念
为了提高代码的复用性
·standard template library标准模板库
·从广义上氛围容器container 算法algorithm 迭代iterater
六大组件：容易，算法，迭代器，仿函数，适配器，空间适配器
![[Pasted image 20240604231252.png]]

1. 容器：
	1. 将运用最广泛的一些数据库结构实现出来
	2. 有序列式容器和关联式容器
		1. 序列是容器：强调值的排序，序列式容器中的每个元素均有固定的位置
		2. 关联式容器：二叉树结构，各元素之间没有严格的物理上的顺序关系
2. 算法：
	1. 问题的解法
	2. 分为质变算法（拷贝，替换,删除）和非质变算法查找，计数，遍历
		1.  是否会更改区间内的元素内容。
3. 迭代器：
	1. 通过迭代器算法才能运用到容器上
	2. 每个容器都有专属的迭代器

## 容器算法迭代器
### vector
	·容器：vector
	·算法：fo_each
		·迭代器：vector<int>::iterator
```c++
void test01()  
{  
    vector<int> v;  
    v.push_back(10);  
    v.push_back(20);  
    v.push_back(30);  
    v.push_back(40);  
    //第一种遍历  
//    for (vector<int>::iterator it  = v.begin();it != v.end();it++)  
//    {  
//        cout << *it << endl;  
//    }  
    //第二种方法  
//    for_each(v.begin(),v.end(), MyPrint);  
    //第三种方法  
    vector<int>::iterator pBegin = v.begin();  
    vector<int>::iterator pEnd = v.end();  
    while (pBegin != pEnd)  
    {  
        cout << *pBegin << endl;  
        pBegin++;  
    }  
}
```
#### vector存放自定义数据类型
存放类的数据
```C++
void test01()  
{  
    vector<Person>v;  
  
    Person p1("aaa",10);  
    Person p2("bbb",20);  
    Person p3("ccc",30);  
    v.push_back(p1);  
    v.push_back(p2);  
    v.push_back(p3);  
    //遍历  
    for(vector<Person>::iterator it = v.begin();it != v.end();it ++)  
    {  
        cout << "姓名" << (*it).m_Name << "年龄： " << (*it).m_Age <<endl;  
  
    }  
  
}
```
存放指针数据
```c++
void test02()  
{  
    vector<Person*>v;  
  
    Person p1("aaa",10);  
    Person p2("bbb",20);  
    Person p3("ccc",30);  
    v.push_back(&p1);  
    v.push_back(&p2);  
    v.push_back(&p3);  
    for (vector<Person*>::iterator it = v.begin();it != v.end();it ++)  
    {  
        cout << "姓名："<<(*it)->m_Name << "年龄：" << (*it)->m_Age << endl;  
    }  
}
```

#### 容器的嵌套

```c++
void test01()  
{  
    vector<vector<int>>v;  
    vector<int> v1;  
    vector<int> v2;  
    vector<int> v3;  
    vector<int> v4;  
  
    for (int i = 0;i<4; i++)  
    {  
        v1.push_back(i+1);  
        v2.push_back(i+2);  
        v3.push_back(i+3);  
        v4.push_back(i+4);  
    }  
  
    v.push_back(v1);  
    v.push_back(v2);  
    v.push_back(v3);  
    v.push_back(v4);  
  
    for (vector<vector<int>>::iterator it = v.begin();it->begin() != it->end(); it++)  
    {  
        for (vector<int>::iterator vit = (*it).begin(); vit != (*it).end(); vit++)  
        {  
            cout << *vit <<" ";  
  
        }  
        cout << endl;  
    }  
}
```
#### 构造函数和赋值
```c++
void test01()  
{  
    vector<int>v;  
    for (int i =0;i < 10;i++)  
    {  
        v.push_back(i);  
    }  
  
    printVector(v);  
  
    vector<int> v2;  
    v2 = v;  
    printVector(v2);  
}  
int main(){  
     test01();  
 }


```
#### 容量和大小
·容量：能存储的最大元素的值
·大小：存储的元素的值
容量永远大于等于大小
```c++
void test01()  
{  
    vector<int>v1;  
    for (int i =0;i < 10; i++)  
    {  
        v1.push_back(i);  
    }  
    printVector(v1);  
  
    if (v1.empty())  
    {  
        cout <<  "v1为空" << endl;  
    }  
    else  
    {  
        cout << "v1不为空 " << endl;  
        cout << "v1的容量为：" << v1.capacity() << endl;  
        cout << "v的大小为:"<< v1.size() << endl;  
    }  
    v1.resize(24);  
    cout << "-------" << endl;  
    cout << "v1的容量为：" << v1.capacity() << endl;  
    cout << "v的大小为:"<< v1.size() << endl;  
}
```
```c++
void test01()  
{  
    vector<int>v1;  
  
    for (int i =0;i < 10; i++)  
    {  
        v1.push_back(i);  
    }  
  
    //[]赋值  
    for (int i = 0;i < v1.size();i++)  
    {  
        cout << v1[i] << " ";  
  
    }  
    cout << endl;  
    //at赋值  
    for (int i = 0;i < v1.size();i++)  
    {  
        cout << v1.at(i) << " ";  
    }  
    cout << endl;  
  
    cout << "v1的最后一个元素：" << v1.back() << endl;  
    cout << "v1的第一个元素是: " << v1.front() << endl;  
}

```
#### vector预留空间
	reserve(int len;) //容器预留len个元素长度，预留位置不初始化，元素不可访问

```c++
void test01()  
{  
    vector<int> v1;  
  
    v1.reserve(1000);  
  
    int num = 0;  
    int *p = NULL;  
    for (int i = 0; i < 10000;i++)  
    {  
        v1.push_back(i);  
        if ( p != &v1[0])  
        {  
            p = &v1[0];  
            num ++;  
        }  
    }  
  
    cout << "num :" << num << endl;  
}
```
每次开辟新的内存v1的第一个元素都会不同
### string
![[Pasted image 20240605151724.png]]
```c++
//stirng 赋值
void test01()  
{  
    string str1;  
    str1 = "hello word";  
    cout << "str1 = " << str1 <<endl;  
  
    string str2;  
    str2 = str1;  
    cout << "str2 = " << str2 <<endl;  
  
    string str3;  
    str3 = ' ';  
    cout << "str3 = " << str3 << endl;  
  
    string str4;  
    str4.assign(str1);  
    cout << "str4 = " << str4 << endl;  
  
    string str5;  
    str5.assign(str1, 6);  
    cout << "str5 = " << str5 << endl;  
  
    string str6;  
    str6.assign(6,'a');  
}
```
![[Pasted image 20240605154810.png]]
```c++
//字符串拼接
 void test01()  
{  
     string str1;  
     str1 = "I";  
     str1 += " Love";  
     cout << "str1 = " << str1 << endl;  
  
     string str2;  
     str2 = str1;  
     str2 +=" ";  
     cout << "str2 = " << str2 << endl;  
  
     string str3;  
     str3 = str1;  
     str3 += str2;  
     cout << "str3 ="<< str3 << endl;  
  
     string str4;  
     str4.append(str1);  
     cout << "str4 = " << str4 << endl;  
  
     string str5;  
     str5.append("sdadad",2);  
     cout << "str5 = " << str5<<endl;  
  
     string str6;  
     str6.append(str3,0,4);  
     cout << "str6 = "<< str6 << endl;  
}
//查找与拼接
void test01()  
{  
    //1.查找  
    //find  
    string str1 = "abcdefgde";  
    int pos = str1.find("fe");  
    if (pos == -1)  
    {  
        cout << "没有找到该值" << endl;  
    }  
    else  
    {  
        cout << "pos =" << pos << endl;  
  
    }  
    //rfind  
    pos = str1.rfind("de");  
    cout << "pos = " << pos << endl;  
  
    //2.替换  
    string str2 = "abcdksal";  
    str2.replace(2,3,"1234"); //pos:替换起始位置，n1：替换的个数  
    cout << "str2 = " << str2 << endl;  
}

//比较
void test()
{
	string str1 = "Hello";
	string str2 = "hello";

	str1.compare(str2) //返回int数据，用ASCII码判断，通常来判断字符串是否相等
	}

//字符串存取
利用str.at(i)可访问单个字符
void test01()  
{  
    string str1 = "asdasd";  
    str1[1] = '1';  
    cout << "str1 = " << str1 << endl;  
  
    for (int i = 0;i < size(str1);i ++ )  
    {  
        cout << str1.at(i) << " ";  
          
    }  
    cout << endl;  
      
}
//插入和删除
void test01()  
{  
    //插入  
    string str = "hello";  
    str.insert(1,"1111");  
    cout << str << endl;  
    //删除  
  
    str.erase(1,4);  
    cout << str << endl;  
}
//截取字串
void test01()  
{  
    string email = "zhangsan@sina.com";  
      
    int pos = email.find("@");  
      string userName = email.substr(0,pos);  
    cout << userName << endl;  
  
}

```
### deque
#### 构造方法
	·deque<T>
	·deque(beg, end)
	·deque(n, elem)
	·deque(const deque &deq)
```c++
void test01()  
{  
    deque<int> d1;  
    for (int i  = 0; i < 10;i++)  
    {  
        d1.push_back(i);  
    }  
    printDeque(d1);  
  
    deque<int> d2(d1.begin(),d1.end());  
    printDeque(d2);  
  
    deque<int> d3(10, 1000);  
    printDeque(d3);  
  
    deque<int> d4(d1);  
    printDeque(d4);  
  
}
```
#### 赋值
	assign
		#区间
		#n个value		
	operator
#### 插入删除
和vector相类似，但区别是可以在头部front添加元素
### 学员成绩打分实战
```c++
void createPerson(vector<Person> &(v))  
{  
    string nameSeed = "ABCDE";  
    for (int i = 0; i <5;i++)  
    {  
        string name = "选手";  
        name += nameSeed[i];  
        int score = 0;  
        Person p(name, score);  
        v.push_back(p);  
    }  
}  
  
void createScore(vector<Person>(&v))  
{  
    for (vector<Person>::iterator it = v.begin();it != v.end();it++)  
    {  
        deque<int>d;  
        for (int i = 0;i < 10;i++)  
        {  
            int score = rand() %78 + 23; //23 ~ 100  
            d.push_back(score);  
        }  
    //test  
//        cout <<"选手"<<  (*it).m_Name << "的打分情况是";  
//        for (deque<int>::iterator dit = d.begin();dit != d.end();dit ++)  
//        {  
//            cout << *dit << " ";  
//        }  
//        cout <<endl;  
  
        sort(d.begin(), d.end());  
        d.pop_back();  
        d.pop_front();  
  
        int sum = 0;  
        for (deque<int>::iterator dit = d.begin();dit != d.end();dit ++)  
        {  
           sum += *dit;  
        }  
        int avg = sum / 10;  
        (*it).m_Score = avg;  
    }  
  
}  
  
void showScore(vector<Person>(&v))  
{  
    for (vector<Person>::iterator it = v.begin();it != v.end();it++ )  
    {  
        cout <<(*it).m_Name <<": "<< (*it).m_Score<< endl;  
    }  
}
```
### stack
	1.top
	2.pop
	3.empty
	4.size

### 链表
由数据域和指针域，结点组成
优点：
·可以对任意位置进行快速的插入或删除，和数组相比，数组还需将元素往前或往后移动来插入或删除元素
·采用动态存储分配，不会造成内存浪费和溢出
![[Pasted image 20240611203100.png]]
 缺点：需要找到相应的指针域来找元素，遍历速度慢，空间与额外耗费大

#### 构造方法
	
	1.list<int>L1;
	2.lsit<int>L2(L1.begin(), L2.end())
	3.list<int>L3(10, 1000)
	4.
#### 赋值和交换
	赋值
		list<int>L1;
		L2 = L1;
	交换
		L2.swap(L1)

### set容器
#### 构造和赋值
	set<int> st;
		st.insert(10);
		st.insert(20);
		st.insert(30);
	set<int> st2(st.begin(), st.end())
	set<int> st3(st);
~~
#### 查找和统计
```c++
void test01()  
{  
    set<int>s;  
  
    s.insert(10);  
    s.insert(20);  
    s.insert(30);  
    s.insert(40);  
  
    set<int>::iterator pos = s.find(30);  
    if (pos != s.end())  
    {  
        cout << "z找到了元素" << *pos << endl;  
    }  
    else  
    {  
        cout << "未找到元素 " << *pos << endl;  
    }  
  
    int num = s.count(30);  
    cout << "num = "  << num <<endl;  
}
```
#### set和multiset
 multiset中的元素可以重复

#### 对组pair的创建
```c++
void test01()  
{  
    pair<string, int>p("Tom", 20);  
  
    cout<< "姓名" << p.first << " 年龄" << p.second << endl;  
}
```
对组中的两个数据都能访问，用first，second来访问
#### set容器排序
```c++
class MyCompare  
{  
public:  
    bool operator()(int v1, int v2)  
    {  
        return v1 > v2;  
    }  
};  
  
void test01() {  
    set<int, MyCompare>s1;  
  
    s1.insert(10);  
    s1.insert(20);  
    s1.insert(30);  
    s1.insert(40);  
  
    for (set<int, MyCompare>::iterator it = s1.begin(); it != s1.end(); it++)  
    {  
        cout << (*it) << " ";  
    }  
    cout << endl;  
  
}
```
对指定类名排序
```c++
class comparePerson  
{  
public:  
    bool operator()(const Person&p1, const Person&p2) const  
    {  
        return p1.m_Age < p2.m_Age;  
    }  
};  
  
void test01()  
{  
    set<Person,comparePerson>s;  
  
    Person p1("Alice", 25);  
    Person p2("Bob", 30);  
    Person p3("Charlie", 20);  
    Person p4("David", 25);  
    Person p5("Eve", 30);  
  
    s.insert(p1);  
    s.insert(p2);  
    s.insert(p3);  
    s.insert(p4);  
    s.insert(p5);  
  
    for (set<Person,comparePerson>::iterator it = s.begin(); it != s.end();it++)  
    {  
        cout << "姓名" << (*it).m_Name << " 年龄" << (*it).m_Age;  
    }  
  
}
```
### map容器
跟字典差不多
·map中所有元素都是pair,pair中的第一个元素为key，第二个元素为value
·元素会根据键值自动匹配，与插入的顺序无关
multimap中的key值可以重复，map不允许容器中有重复的key值

	构造方法：
		直接构造
		拷贝构造
	赋值
		直接复制

#### 大小和互换
	size -- 统计大小
	empty 判断是否为空
	swap 交换容器
#### 插入和删除

## 函数对象
### **函数对象概念**
·重载函数调用操作符的类，其对象称为函数对象
·函数兑现使用重载的()时，行为类似函数调用，也叫仿函数

函数对象(仿函数)是一个类，不是一个函数

**函数对象使用**
特点：
·函数对象在使用时，可以像普通函数那样调用，可以有参数，可以有返回值
·函数对象超出普通函数的概念，函数对象可以有自己的状态
·函数对象可以作为参数传递
```c++
class MyAdd  
{  
public:  
    int operator()(int n1, int n2)  
    {  
        return n1 + n2;  
    }  
};  
void test01()  
{  
    MyAdd add;  
    cout<<add(10,20) << endl;  
  
}  
//2函数对象有自己的状态  
class MyPrint  
{  
public:  
    MyPrint()  
    {  
        this->count = 0;  
    }  
    void operator()(string test)  
    {  
        cout << test << endl;  
        this->count++;  
    }  
    int count;  
};  
  
void test02()  
{  
    MyPrint print;  
    print("test");  
    print("test");  
    print("test");  
    print("test");  
    print("test");  
  
    cout << print.count << endl;  
  
}
```


### 谓词
 ·返回bool类型的仿函数称为谓词
 有一元谓词和二元谓词区别是operator接受多少个参数  