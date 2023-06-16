# 1. 程序的基本结构
```c
#include <iostream>
using namespace std;  // 命名 std 命名空间

int main(){
      int a = 5;
      cout << 'a 的值为' << a << endl;
      return 0;
}
```

# 2. 数据类型
## 2.1 基本数据类型
```cpp
#include <iostream>
using namespace std;

int main(){
    cout << sizeof(bool) << endl;        //1byte
    cout << sizeof(char) << endl;        //1byte
    cout << sizeof(int)  << endl;        //4byte
    cout << sizeof(short int) << endl;   //2byte
    cout << sizeof(long int) << endl;    //8byte
    cout << sizeof(fload) << endl;       //4byte
    cout << sizeof(double) << endl;      //8byte
    cout << sizeof(long double) << endl; //16byte
    cout << sizeof(wchar_t) << endl;     //4byte
    return 0;
}
```
## 2.2 struct 结构体
```cpp
#include <iostream>
using namespace std;
struct student{
    int num;       //学号
    char name[20]; //姓名
    char sex;      //性别
    int age;       //年龄
};

int main(){
    student stu = {0001, "Linda", 'F', 19}; // 初始化 变量赋值
    cout << stu.name << endl;
    return 0;
}
```
## 2.3 enum 枚举
```cpp
#include <iostream>
using namespace std;
int main(){
    enum color {red, green, blue} c;
    
    enum color {red, green, blue};
    enum color c=blue;
    
    enum color {red, green=5, bule} c;
    c = blue  // c=6 red=0
    return 0;
}
```
# 3. 变量
## 3.1 变量的类型
```cpp
#include <iostream>
using namespace std;
int main(){
    // 指针
    int a =20;
    int *p;
    p = &a;
    
    // 数组
    double balence[5] = {1000.0, 1.0, 2.3, 3.4, 4.5};
    double balence[] = {1000.0, 1.0, 2.3, 3.4, 4.5};
    
    // 引用  任何时候系统都不会对引用进行初始化，必须在创建时初始化  函数传参加引用返回的参数是函数处理后的
    int i = 5;
    int& r=i;
    
    return 0;
}
```

## 3.2 变量的声明
```cpp
#include <iostream>
using namespace std;
extern int a;
int main(){
    int a = 10;
    return 0;
}
```
## 3.3 变量的使用
```cpp
#include <iostream>
using namespace std;
int main(){
    int a = 10;  // a 左值 指向内存位置的表达式 可以出现在“=”左边  10 右值 存储在内存地址的数值，只能出现在“=”右边
    return 0;
}
```
# 4. 常量 
```cpp
#include <iostream>
using namespace std;
#define num 10
const int LENGTH = 20;

int main(){
    return 0;
}
```
 c++ 宏定义 边际效应 https://blog.csdn.net/AngelDg/article/details/120143877



