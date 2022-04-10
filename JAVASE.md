Java入门

# 1.Java的概述

> Java是由sun公司在1995年研发推出，后在2009年被Oracle公司收购。
>
> Java之父是：詹姆森·高斯林。
>
> Java是一门高级编程语言：语言风格接近人类的自然语言，写程序简单易懂。
>
> Java的流行度很高，商用占用率很高。
>
> java有一个很重要的特性：可移植性（跨平台）。
>
> Java什么都可以干，但是最被市场认可的是企业级开发：如京东淘宝这样的互联网系统。

### Java的技术体系分为

> javaSE：标准版，Java技术的核心和基础
>
> javaEE：企业版，大型互联网企业级解决方案，充分被市场认可
>
> javaME：小型版，移动应用的解决方案，没有被市场认可

### java的重要特点

**java语言是==面向对象==的（oop）**

**java语言是健壮的。java的强类型机制，异常处理，垃圾的自动收集等是java程序健壮性的重要保证**。

**java语言是==跨平台性==的。**

> 即一个编译好的class文件可以在多个系统下运行，这种特性称为跨平台。

**java语言是解释型的**

> 解释型语言还有，JavaScript，java，PHP。编译型语言，c，c++
>
> 区别是：解释型语言，编译后的代码不能被机器执行，需要解释器来执行。编译型语言，编译后的的代码，可以直接被机器执行

# 2.Java的产品

**JDK：Java的开发工具包，必须安装它才可以使用java**

> 去Oracle官网下载，安装在没有空格和中文的路径
>
> 学习使用的jdk推荐最新版本，企业可能用的老版本jdk8，因为稳定性高
>
> LST：长期支持的版本：jdk8、jdk11、jdk17

### JDK中最常用的两个软件

> javac：编译程序
>
> java：之星程序

# 3.开发第一个Java程序

### 编写代码

> 代码编写规范，建议使用全英文名称，首字幕大写，后缀一定是.java

```java
//class后面的名字要和文件名字一样
public class HelloWorld{
    public static void main(String[] args){
        System.out.print("HelloWorld");//打印HelloWorld
    }
}
```

### 执行代码

**在使用命名窗编写代码时，要让代码运行起来还要以下两步**

```cmd
javac HelloWorld.java
```

> 这是先编译脚本文件，运行后会得到一个HelloWorld.class的文件

```cmd
java HelloWorld
```

> 运行这个代码，就会输出结果了，代码就跑起来了

# java的基础语法

# 第一阶段



## 1.注释

- **什么是注释**

  > 注释是写在代码中对对代码进行解释的说明的文字，方便自己和其他人查看，以便理解程序

```java
//这个是单行注释，注释内容只能写一行
```

```java
/*
多行注释
可以注释多行
*/
```

```java
/**
文档注释
文档注释的内容可以提及到一个程序的说明文档中去
*/
```

- **注释的特点**

  > 注释不会影响到程序的执行

## 2.字面量

- **计算机是用来处理数据的，字面量就是告诉程序员：数据在程序中的书写格式**

| 常用数据 | 现时中的写法 | 程序中的写法 | 说明                                   |
| :------- | :----------- | :----------- | :------------------------------------- |
| 整数     | 666，-888    | 666，-888    | 写法一致                               |
| 小数     | 5.55，-8.88  | 5.55，-8.88  | 写法一致                               |
| 字符     | A，你，0     | 'A','你','0' | 程序中必须使用单引号，有且仅能一个字符 |
| 字符串   | 牛马程序员   | "牛马程序员" | 程序中必须使用单引号，内容可有可无     |
| 布尔值   | 真，假       | true，false  | 只有两个值，true代表真，false代表假    |
| 空值     |              | 值是：null   | 一个特殊的值，空值                     |

```java
public class Literal {
    public static void main(String[] args) {
        //整数
        System.out.println(444);

        //小数
        System.out.println(88.85);

        //字符
        System.out.println('0');
        System.out.println('A');
        System.out.println('你');
        //字符里面只能有一个字符，多了就会报错
//        System.out.println('niuma');
        System.out.println(' ');//空字符
        //特殊的字符：\n代表了换行，\t代表了是一个tab缩进
        System.out.println('n');
        //pdrintln后面的ln本身就代表了一个换行，所有这里会换两行
        System.out.println('\n');
        System.out.println('p');
        System.out.println('\t');

        //字符串
        System.out.println("HelloWorld");
        System.out.println("");
        System.out.println("   ");
        System.out.println("H");

        //布尔值
        System.out.println(true);
        System.out.println(false);

    }
}

```

## 3.变量

**变量就是用来存储一个数据的内存区域（可以理解成盒子）且里面存储的数据可以变化**

### **3.1 变量的定义格式**

**数据类型 变量名称 = 初始值;**

> 数据类型就是强制盒子中存储数据的形式
>
> 变量名称就是却名字，首字母建议小写，且取得名字要有意义
>
> 初始值就是存储的初始数据

```java
int a = 5;
```

```java
public class variableDome1 {
    public static void main(String[] args) {
        //数据类型 变量名称 = 初始值;
        double monye = 6.0;
        System.out.println(monye);

        //增加（从=右往左看）
        monye = monye + 4.0;
        System.out.println(monye);
    }
}
```

### **3.2 变量的注意事项**

> 变量要先声明在使用，不然报错
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220214180420766.png)

> 变量声明后，不能存储其他类型的数据
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220214180610586.png)

> 变量的有效范围是从定义开始到"}"截止，且在同一个范围内不能定义两个同名的变量
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220214181337486.png)

> 变量定义的时候j可以没有初始值，但是在使用的时候不必须给初始值
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220214181612737.png)

### **3.3 程序中+号的使用**

> 当左右两边都是数字类型时，则作加法运算
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220215153204618.png)

> 当左右两边有一方为字符串时，则做拼接运算
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220215153811742.png)

> 运算顺序是从左到右

### **3.4 数据类型**

每一种数据都定义了明确的数据类型，在内存中分配了不同大小的内存空间（字节）.

数据类型又分为基本数据类型和引用数据类型

基本数据类型有：

**数值型**：

> 整数类型，存放整数（byte[1],short[2],int[4],long[8]）
>
> 浮点（小数）类型（float[4],double[8]）

**字符型（char[2]）存放单个字符**

**布尔型（boolean[1]）存放true和false**

引用数据类型：

**类（class）**

**接口（interface）**

**数组（[]）**

#### **3.4.1 整形**

java程序中变量常声明为int型，除非不足以表示大数才用long

```java
public class variableDome3 {
    public static void main(String[] args) {
        //java的整型常量默认为int类型，声明long类型常量须在后加“l”或“L”
        int a1 = 40;
//        int a2 = 5L;//报错，不能这样
        long a2 = 4L;
    }
}
```



#### 3.4.2 **浮点类型**

关于浮点数在机器中存放形式的简单说明==浮点数=符号位+指数位+尾数位==

尾数部位可能丢失，造成精度损失（小数都是近似值）

> java的浮点型常量默认为double类型，声明long类型常量须在后加“f”或“F”
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220215192537891.png)

```java
public class Float {
    public static void main(String[] args) {
        //java的浮点型常量默认为double类型，声明long类型常量须在后加“f”或“F”
        float num= 1.3F;
        double num1 = 1.2;
        double num2 = 2.5F;
    }
}
```

浮点型常量有两种表达形式

> 十进制表达式：如：5.12    2.53     .25（必须有小数点）
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220215194039425.png)

> 科学计数法形势：如：5.12e2[5.12乘以10的2次方]    5.12E-2[5.12除以10的2次方]
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220215194127825.png)

> 在通常情况下我们使用double类型，因为double类型比float类型精度更准确
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220215194658369.png)

> 浮点数使用时的一个陷阱
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220215195319353.png)

**得到一个重要的使用点：==当我们对运算结果是小数的进行相等的判断时，要小心==**

```java
//这样是错误的写法，这样得不到我们想要的结果
if (num5 == num6){
    System.out.println("相等");
}else{
    System.out.println("不相等");
}

//正确的应该是两个数值的差值的绝对值，在某个精度范围内来判断
//先来看一下差值的绝对值
 System.out.println(Math.abs(num5-num6));
                    
if(Math.abs(num5-num6)<=0.0001){
    System.out.println("差值非常小，在我的规定精度内，认为相等");
}else{
    System.out.println("不相等");
}

```

**如果是直接查询得到的小数或者是直接赋值，是可以判断相等的**

**ps：上面用到了一个Math.abs这个是Java的API文档中的一个类**

> JavaAPI文档
>
> API（Application Programming Interface，应用程序编程接口）是java提供的基本编程接口（java提供的类，还有相关的方法）
>
> [中文在线文档](https://www.matools.com)

#### **3.4.3 字符类型**

字符类型可以表示单个字符，字符类型值char，char是两个字节(可以存放汉字)

多个字符使用字符串String

```java
public class Char {
    public static void main(String[] args) {
        //char 字符类型的基本使用
        char c1 = '1';
        char c2 = '牛';
        char c3 = '\n';
        char c4 = 50;//说明：字符类型可以直接存放一个数字

        System.out.println(c1);
        System.out.println(c2);
        System.out.println(c3);
        System.out.println(c4);//当char的值为数字输出时，它会输出该数字对应表示的字符=》编码的
    }
}

```

**字符常量是用==单引号('')==括起来的==单个字符==**

在java中，char的本质是一个整数，在默认输出时是输出他在[unicode码](https://tool.chinaz.com/Tools/Unicode.aspx)中对应的字符。

要想要输出他对映的字符可以使用==(int)字符==这个方法来输出

char类型是可以进行运算的，相当于一个整数，因为他都有对应的unicode码

```java
System.out.println('a'+10);//得到的结果是107，因为a的Unicode码是97
```

#### **3.4.4 布尔类型**

布尔类型也叫boolean类型，布尔类型数据只允许取值==true==和==false==，不可以为空

boolean类型占一个字节

boolean类型一般用于逻辑运算，一般用于程序流程控制

> if条件控制语句
>
> while循环控制语句
>
> do-while循环控制语句
>
> for循环控制语句
>
> ```java
> //定义布尔值类型的变量
> boolean pass = true;
>         if (pass){
>             System.out.println("真");
>         }else {
>             System.out.println("假");
>         }
> ```
>
> **在java中不能用0或非0的整数来替代false和true，这点和其他语言不同**

### **3.5 自动类型转换**

当java程序在进行赋值或者运算时，精度小的类型自动转换为精度大的数据类型，这个就是==自动类型转换==。

> ==char-->int-->long-->float-->double==
>
> ==byte-->short-->int-->long-->float-->double==
>
> ```java
> int num1 = 'a';
> double num2 = 80;
> System.out.println(num1);
> System.out.println(num2);
> ```

有多种数据类型的数据混合运算时，系统首先自动将所有数据转换成容器量最大的那种数据类型，然后再进行计算。

> ```java
> int n1 = 10;
> double b1 = n1 + 2.2;//n1++2.2-->double类型
> System.out.println(b1);
> float f1 = n1 + 2.2F;//n1+2.2F-->float类型
> System.out.println(f1);
> ```

当我们把精度(容量)大的数据类型赋值给精度(容量)小的数据类型时，就会报错，反之就会进行自动类型转换。

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220216170112811.png)

byte，short，char他们三者可以计算，在计算时首先转换为int类型

boolean类型不参与转换。

自动提升原则：表达式结果的类型自动提升为操作数中最大的类型

```java
byte b1 = 1;
short s1 = 2;
int i1 = 3;
double d1 = 2.3;

double d2 = b1+s1+i1+d1;
```

### 3.6 **强制数据类型转换**

自动类型转的逆过程，将容量大的数据类型转换为容量小的数据类型。使用时要加上强制转换符()，但可能造成精度降低或溢出，==格外要注意==。

```java
int n1 = (int)1.5;
System.out.println("n1="+n1);//结果为1，这造成了精度损失

int n2 = 2000;
byte b1 = (byte)n2;
System.out.println("b1="+b1);//输出结果为-48，数据溢出。
```

强转符号只针对于最近的操作数有效，往往会使用小括号提升优先级

```java
int x = (int)10*9.3+3*3.4;//编译错误，double-->int
int y = (int)(10*9.3+3*3.4);//(int)103.2-->103
System.out.println(y);

```

char类型可以保存int的常量值，但不能保存int的变量值，需要强转

```java
char c1 =100;
int m = 100;
char c2 = m;//编译错误
char c3 = (char)m;
System.out.println(c3);//100对应的字符
```

### **3.7 基本数据类型和String类型的转换**

在程序开发中，我们经常需要将基本数据类型转成String类型。或者将String类型转成基本数据类型

```java
//基本数据类型-->String
int n1 = 100;
float f1 = 2.2F;
double d1 = 3.3;
boolean b1 = true;
String s1 = n1 + "";
String s2 = f1 + "";
String s3 = d1 + "";
String s4 = b1 + "";
System.out.println(s1 + " " + s2 + " " + s3 + " " + s4);
```

```java
//String-->对应的基本数据类型
String s5 = "123";
//使用基本数据类型对应的包装类的相应方法，得到基本数据类型
int num1 = Integer.parseInt(s5);
double num2 = Double.parseDouble(s5);
float num3 = Float.parseFloat(s5);
long num4 = Long.parseLong(s5);
boolean b = Boolean.parseBoolean("true");
byte num5 = Byte.parseByte(s5);
short num6 = Short.parseShort(s5);

System.out.println(num1);
System.out.println(num2);
System.out.println(num3);
System.out.println(num4);
System.out.println(num5);
System.out.println(num6);
System.out.println(b);

//把字符串转成字符char-->含义是指把字符串的第一个字符得到
//s5.charAt(0)得到的是s5字符串的第一个字符
System.out.println(s5.charAt(0));
```

在将String类型转成基本数据类型时，要确保String类型能购转成==有效的数据==，比如：可以把”123”转成一个整数，但是不能把“hello”转成一个整数

如果格式不正确，就会抛出异常，程序就会终止

## 4.运算符

运算符是一种特殊的符号，用以表示数据的运算，赋值和比较等。

### **4.1 算术运算符**

算术运算符是对数值类型的变量进行运算的，在java程序中，使用的非常多。

| 运算符 |           运算           |
| :----: | :----------------------: |
|   +    |           正号           |
|   -    |           负号           |
|   +    |            加            |
|   -    |            减            |
|   *    |            乘            |
|   /    |            除            |
|   %    |           取余           |
|   ++   | 自增（前）：先运算后取值 |
|   ++   | 自增（后）：先取值后运算 |
|   --   | 自减（前）：先运算后取值 |
|   --   | 自减（后）：先取值在运算 |
|   +    |        字符串相加        |

```java
//  /使用
System.out.println(10/4);//整数相除，取整数舍去小数
System.out.println(10.0/4);//现在是浮点数与整数相除，double类型的精度大于int，所以现在这里面是double类型，结果有小数
double b = 10/4;//整数相除舍去小数得到2，赋予给double类型 2-->2.0
System.out.println(b);//2.0
```

```java
//  %取余
//在java中%的本质是看一个公式 a % b = a - a / b * b
//a%b当a是小数时，公式：a % b = a - (int)a / b * b
//注意：有小数运算时，得到的结果时近似值
System.out.println(10%3);//1
System.out.println(-10%3);//-1
System.out.println(10%-3);//1
System.out.println(-10%-3);//-1
```

```java
// 自增++
// 作为独立语句使用时，前++和后++都完全等价于i=i+1;
int i = 10;
i++;//自增1 i->11
++i;//自增1 i->12
System.out.println(i);
/*
作为表达式使用
前++：++i先自增后赋值
后++：i++先赋值后自增
*/
int j = 3;
int k = ++j;//等价 --> j=j+1,j=k
System.out.println("j="+j+"\t"+"k="+k);// 4 4
int j1 = 3;
int k1 = j1++;//等价 --> j1=k1,j1=j1+1
System.out.println("j1="+j1+"\t"+"k1="+k1);// 3 4
```

--和++道理一样可以类推，+，-，*就是数学中的道理

### **4.2 关系运算符**

关系运算符的结果都是boolean类型，也就是要么是true，要么是false

关系表达式经常用在if结构的条件中或循环结构的条件中

| 运算符     | 运算               |
| ---------- | ------------------ |
| ==         | 相等于             |
| !=         | 不等于             |
| <          | 小于               |
| >          | 大于               |
| <=         | 小于等于           |
| >=         | 大于等于           |
| instanceof | 检查是否是类的对象 |

```java
int a = 4;
int b = 6;
System.out.println(a == b);//false
System.out.println(a != b);//true
System.out.println(a > b);//false
System.out.println(a < b);//true
System.out.println(a >= b);//false
System.out.println(a <= b);//true
boolean flag = a > b;//flase
System.out.println(flag);
```

关系运算符组成的表达式，我们称为关系表达式

### **4.3 逻辑运算符**

用于链接多个条件(多个关系表达式)，最终的结果也是一个boolean值

|   a   |   b   | a&b(逻辑与&) | a&&b(短语与&&) | a\|b(逻辑或\|) | a\|\|b(短路或\|\|) | !a(取反!) | a^b(逻辑异或) |
| :---: | :---: | :----------: | :------------: | :------------: | :----------------: | :-------: | :-----------: |
| true  | true  |     true     |      true      |      true      |        true        |   false   |     false     |
| true  | false |    false     |     false      |      true      |        true        |   false   |     true      |
| false | true  |    false     |     false      |      true      |        true        |   true    |     true      |
| false | false |    false     |     false      |     flase      |       flase        |   true    |     flase     |

> **逻辑运算规则：**
>
> **1.a&b：&叫逻辑与，规则：当a和b同时为true，则结果为true，否则为false**
>
> **2.a&&b：&&叫短路与，规则：当a和b同时为true，则结果为true，否则为false**
>
> **3.a|b：|叫逻辑或，规则：当a和b有一个为true，则结果为true，否则为false**
>
> **4.a||b：||叫短路或，规则：当a和b有一个为true，则结果为true，否则为false**
>
> **5.!a：!叫取反，或者非运算，当a为true时，则结果为false，当a为false时，结果为true**
>
> **6.a^b：叫逻辑异或，当a和b不同时，则结果为true，否则为false**

```java
//短路与&&的使用
int age = 19;
if (age > 18 && age < 25) {
	System.out.println("条件都为真，结果为真，我会出现");
}
if (age > 18 && age < 19) {
	System.out.println("条件有一个假，结果为假，我不会出现");
}

//逻辑与&的使用
if (age > 18 & age < 25) {
	System.out.println("条件都为真，结果为真，我会出现");
}
if (age > 18 & age < 19) {
	System.out.println("条件有一个假，结果为假，我不会出现");
}

//&&与&的区别
int a = 1;
int b = 3;
//对于短路与而言，如果第一个条件为false，后面的条件就不会判断
if (a>2&&++b<7){
	System.out.println("条件为假我不会出现");
 }
//因为后面的条件不判断也就不会执行后面的代码，所以b还是3
System.out.println("a="+a+"b="+b);

//对于逻辑与而言，如果第一个条件为false，后面的条件任然会判断
if (a>2&++b<7){
	System.out.println("条件为假我不会出现");
}
//因为后面的条件判断了，所以会执行后面的代码，则b的结果为4
System.out.println("a="+a+"b="+b);
```

在开发中，基本是使用短路与，因为效率高

```java
//短路或||的使用
int day = 19;
if (day > 18 || day < 17) {
	System.out.println("条件有一个为真，结果为真，我会出现");
}
if (day > 20 ||day < 19) {
	System.out.println("条件都为假，结果为假，我不会出现");
}

//逻辑或|的使用
if (day > 18 |day < 17) {
	System.out.println("条件有一个为真，结果为真，我会出现");
}
if (day > 20 |day < 19) {
	System.out.println("条件两个都为假，结果为假，我不会出现");
}

//||与|的区别
int a = 1;
int b = 3;
//对于短路或而言，如果第一个条件为true，后面的条件就不会判断
if (a>0||++b<7){
	System.out.println("条件为真我会出现");
}
//因为后面的条件不判断也就不会执行后面的代码，所以b还是3
System.out.println("a="+a+"b="+b);

//对于逻辑或而言，如果第一个条件为true，后面的条件任然会判断
if (a>0|++b<7){
	System.out.println("条件为真我会出现");
}
//因为后面的条件判断了，所以会执行后面的代码，则b的结果为4
System.out.println("a="+a+"b="+b);
```

在开发中，基本是使用短路或，因为效率高

```java
 //!取反的使用
//取反的操作就是真变假，假变真
System.out.println(1<2);//true
System.out.println(!(1<2));//取反后结果为false
```

```java
//!取反的使用
//取反的操作就是真变假，假变真
System.out.println(1<2);//true
System.out.println(!(1<2));//取反后结果为false
        
//^逻辑异或的使用
//当a和b不同时，结果为真，否则为假
boolean a = 1>0;
boolean b = 2>1;
boolean c = a^b;//因为a和b都为真，两边相同，结果为假
System.out.println(c);
a = 1>2;
c = a^b;//a为假，两边不相同，结果为真
System.out.println(c);
```

### **4.4 赋值运算符**

赋值运算符就是将某个运算后的值，赋给指定的变量

> 基本赋值运算符 =
>
> 复合赋值运算符：
>
> +=、-=、*=、/=、%=等
>
> 重点讲解一个，其他的使用的是一个道理
>
> a +=b;[等价于：a = a+b;]

```java
int num= 10;
num += 5;//num = num + 5
System.out.println(num);
num /= 4;//num = num / 4
System.out.println(num);
```

运算顺序从右到左

赋值运算符左边只能是变量，右边可以是变量、表达式、常量值

复合赋值运算符会进行类型转换

### **4.5 三元运算符**

基本语法：

==条件表达式?表达式1:表达式2;==

运算规则：

1.如果条件表达式为true，运算后的结果是表达式1；

2.如果条件表达式为false，运算后的结果是表达式2； 

```java
int a = 20;
int b = 89;
//条件表达式的结果为假，所以返回b--
int num = a>b?a++:b--;
System.out.println(num);
System.out.println(a);
System.out.println(b);
```

表达式1和表达式2要为可以赋给接收变量的类型（或可以自动转换/或强制转换）

三元运算符可以转成if--else语句

**运算符有不同的优先级，所谓优先级就是表达式运算中的运算顺序，只有单目运算符、赋值运算符是从右向左运算的**

下面是优先级排序

> 1) () {} 等
> 2) 单目运算符
> 3) 算术运算符
> 4) 位移运算符
> 5) 比较运算符
> 6) 逻辑运算符
> 7) 三元运算符
> 8) 赋值运算符

### **4.6 标识符的命名规则和规范**

标识符概念：

java对各种变量，方法和类等命名时使用的字符序列称为标识符

凡是自己可以起名字的地方都叫标识符

**标识符的命名规则（必须遵守）：**

**由26个英文字母大小写，0至9，_或$组成**

**数字不可以开头**

**不可以使用关键字和保留字，但能包含关键字和保留字**

**java中严格区分大小写，长度无限**

**标识符不能包含空格**

### **4.7 键盘输入语句**

在编程中，需要接收用户输入的数据，就可以使用键盘输入语句来获取

```java
//第一步，导包
import java.util.Scanner;//表示把java.util下的Scanner类导入
//Scanner类表示简单文本扫描器
public class input {
    public static void main(String[] args) {
        //第二步，创建Scanner对象
        Scanner scanner = new Scanner(System.in);//代表从键盘输入
        //new 创建一个对象的意思，scanner就是Scanner类的对象

        //第三步，接受用户的输入，使用相关的方法
        System.out.println("输入你的岁数");
        //当程序执行到next方法时，会等待用户的输入，如果用户不输入程序就会停在这里，一直等待
        int age = scanner.nextInt();//接受用户输入的int
        System.out.println("输入你的姓名");
        String name = scanner.next();//接受用户输入的字符串
        System.out.println("输入你每个月的工资");
        double money = scanner.nextDouble();//接受用户输入的double
        System.out.println("你的姓名是"+name+"，今年"+age+"岁，每个月的收入是"+money+"元");
    }
}
```

### **4.8 进制**

对于整数，有四种表示方式：

二进制：0,1，满2进1，以0b或0B开头

十进制：0-9，满10进1

八进制：0-7，满8进1，以数字0开头表示

十六进制：0-9及A(10)-F(15)，满16进1，以0x或0X开头表示，此处A-F不区分大小写

```java
//二进制
int i1 = 0b1010;
//八进制
int i2 = 01010;
//十进制
int i3 = 1010;
//十六进制
int i4 = 0x10101;
System.out.println("二进制"+i1+"八进制"+i2+"十进制"+i3+"十六进制"+i4);
```

**二进制转换成十进制**

规则：从最低位(右边)开始，将每个位上的数提取出来，乘以2的(位数-1)次方，然后求和

**案例：将0b1011转成十进制**

```java
0b1011 = 1*2的(1-1)次方+1*2的(2-1)次方+0*2的(3-1)次方+1*2的(4-1)次方 = 1+2+0+8 = 11
```

**八进制转换成十进制**

规则：从最低位(右边)开始，将每个位上的数提取出来，乘以8的(位数-1)次方，然后求和

**十六进制转换成十进制**

规则：从最低位(右边)开始，将每个位上的数提取出来，乘以16的(位数-1)次方，然后求和

**十进制转换成二进制**

规则，将该数不断除以2，直到商为0为止，然后将每步得到的余数倒过来，就是对应的二进制

**十进制转换成八进制**

规则，将该数不断除以8，直到商为0为止，然后将每步得到的余数倒过来，就是对应的八进制

**十进制转换成十六进制**

规则，将该数不断除以16，直到商为0为止，然后将每步得到的余数倒过来，就是对应的十六进制

**二进制转换成八进制**

规则：从低位开始，将二进制数每三位一组，转成对应的八进制数即可

**二进制转换成十六进制**

规则：从低位开始，将二进制数每四位一组，转成对应的十六进制数即可

**八进制转换成二进制**

规则：将八进制数每1位，转成对应的一个3位的二进制数即可

**十六进制转换成二进制**

规则：将十六进制数每1位，转成对应的一个4位的二进制数即可

### **4.9 位运算**

java中有7个位运算(&、|、^、~、>>、<<、>>>)

分别是按位与&、按位或|、按位异或^、按位取反~

按位与&：两位全为1，结果为1，否则为0

按位或|：两位有一个为1，结果为1，否则为0

按位异或^：两位一个为0一个为1，结果为1，否则为0

按位取反~：0->1,1->0

```java
/*二进制的最高位是符号位，0表示正数，1表示负数
        * 正数的原码，反码，补码都一样(三码合一)
        * 负数的反码=它的原码符号位不变，其他位取反(0->1,1->0)
        * 负数的补码=它的反码+1，负数的反码=负数的补码-1
        * 0的反码补码都是0
        * java没有无符号数，换言之，java中的数都是有符号的
        * 在计算机运算的时候，都是以补码的方式来运算的
        * 当我们看运算结果的时候，要看他的原码*/

        //先得到2的补码，=>2的原码 00000000 0000000 0000000 00000010
        //2的补码 00000000 0000000 0000000 00000010
        //3的原码 00000000 0000000 0000000 00000011
        //3的补码 00000000 0000000 0000000 00000011
        //按位&
        //00000000 0000000 0000000 00000010
        //00000000 0000000 0000000 00000011
        //00000000 0000000 0000000 00000010 运算后的补码
        //运算后的源码也是 00000000 0000000 0000000 00000010
        //结果就是2
        System.out.println(2&3);

        //先得到-2的原码 10000000 00000000 0000000 00000010
        //-2的反码 11111111 1111111 11111111 11111101
        //-2的补码 11111111 1111111 11111111 11111110
        //~-2操作 00000000 00000000 00000000 00000001 运算后的补码
        //运算后的原码就是 00000000 00000000 00000000 00000001
        System.out.println(~-2);

        //先得到2的补码 00000000 0000000 0000000 00000010
        //~2的操作 11111111 11111111 11111111 11111101
        //运算后的反码 11111111 11111111 11111111 11111100
        //运算后的原码 10000000 00000000 00000000 00000011
        System.out.println(~2);//-3

        //先得到2的补码 00000000 0000000 0000000 00000010
        //在得到3的补码 00000000 0000000 0000000 00000011
        //2|3的操作 00000000 0000000 00000000 000000011 运算后的补码
        //运算后的原码 00000000 0000000 00000000 000000011 ->3
        System.out.println(2|3);

        //先得到2的补码 00000000 0000000 0000000 00000010
        //在得到3的补码 00000000 0000000 0000000 00000011
        //2^3操作 00000000 0000000 00000000 00000001 运算后的补码
        //运算后的原码 00000000 0000000 00000000 00000001 ->1
        System.out.println(2^3);
```

还有3个为运算符，>>、<<、>>>，运算规则：

算术右移>> ：低位溢出，符号位不变，并用符号位补溢出的高位

算术左移<<：符号位不变，低位补0

逻辑右移也叫无符号右移>>>：低位溢出，高位补0

没有<<<符号

## 5.控制结构

在程序中，程序运行的流程控制决定程序时如何执行的，是我们必须掌握的，主要有三大控制语句：1.顺序控制、2.分支控制、3.循环控制

### **5.1 顺序控制**

顺序从上到下逐行的执行，中间没有任何判断和跳转

### **5.2 分支控制**

**分支控制if-else** 让程序有选择的执行，分支控制有三种：1.单分支、2.双分支、3.多分支

#### 5.2.1 单分支

基本语法

> if(条件表达式){
>
> ​		执行代码块;	(可以有多条语句)
>
> }

说明：当条件表达式为true时，就会执行{}的代码。如果为false，就不执行。特别说明，如果{}中只有一条语句，则可以不用{}，建议写上{}

```java
import java.util.Scanner;
public class Ifbranch {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("输入你的年龄");
        //接收输入的年龄
        int age = scanner.nextInt();
        //使用if判断，输出对应信息
        if (age>=18){
            System.out.println("你满18的要为做的事负责");
        }
        System.out.println("程序继续");
    }
}
```

#### 5.2.2 双分支

基本语法

> if(条件表达式){
>
> ​		执行代码块1;
>
> }
>
> else{
>
> ​			执行代码块2;
>
> }

说明：当条件表达式成立即执行代码块1，否则执行代码块2，如果执行代码块只有一条语句，则{}可以省略，否则，不能省略，建议书写{}

```java
        if (age>=18){
            System.out.println("你满18的要为做的事负责");
        }else {//双分支
            System.out.println("你还是未成年");
        }

```

#### 5.2.3 多分支

基本语法：

> if(条件表达式){
>
> ​		执行代码块1;
>
> }
>
> else if(条件表达式2){
>
> ​		执行代码块2;
>
> }
>
> ......
>
> else{
>
> ​		执行代码块n;
>
> }

 说明：

当条件表达式1成立时，即执行代码块1.

如果表达式1不成立，才去判断表达式2是否成立，

如果表达式2成立，就执行代码块2，

以此类推，如果所有的表达式都不成立

则执行else的代码块，注意，只能有一个执行入口

多分支可以没有else，如果所有的条件表达式都不成立，则一个执行入口都没有

如果有else，如果所有的条件表达式都不成立，则默认执行else代码块

```java
        System.out.println("输入你的信用分（1-100）");
        double credit = scanner.nextDouble();
        if (credit >100||credit<1){
            System.out.println("请输入正确的信用分");
        }else if (credit == 100){
            System.out.println("信用极好");
        }else if (credit <=99 && credit >80){
            System.out.println("信用优秀");
        }else if (credit <=80&&credit>=60){
            System.out.println("信用一般");
        }else{
            System.out.println("信用差");
        }
```

#### 5.2.4 嵌套分支

在一个分支结构中又完整的嵌套了另一个完整的分支结构，里面的分支的结构称为内层分支外面的分支结构称为外层分支。建议最好不要超过3层(可读性不好)

```java
        //嵌套分支
        System.out.println("输入你的姓别");
        char gender = scanner.next().charAt(0);//先接收到字符串，在接收字符串中的第一个字符
        System.out.println("输入你的分数");
        double score = scanner.nextDouble();
        if (score > 8.0){
            if (gender == '男'){
                System.out.println("你进入了决赛，分到了男子组");
            }else if (gender == '女'){
                System.out.println("你进入了决赛，分到了女子组");
            }else{
                System.out.println("你的性别输错了");
            }
        }else{
            System.out.println("你没有进入决赛");
        }

```

#### 5.2.5 switch分支

基本语法：

> switch(表达式){//在java中，只要有值返回，就是一个表达式
>
> case 常量1: 
>
> 语句块1;
>
> break;
>
> case 常量2:
>
> 语句块2;
>
> break;
>
> ...
>
> case 常量n:
>
> 语句块n;
>
> break;
>
> default:
>
> default语句块;
>
> break;
>
> }

**switch 关键字，表示switch分支**

**表达式，对应一个值**

**case常量1：当表达式的值等于常量1，就执行语句块1**

**break：表示退出switch**

**如果和case常量1匹配，就执行语句块1，如果没有匹配，就继续匹配case常量2**

**如果一个都没有匹配上，执行default**

```java
        System.out.println("输入一个字符（a-g）");
        char c = scanner.next().charAt(0);
        switch (c){
            case 'a':
                System.out.println("今天星期一");
                break;
            case 'b':
                System.out.println("今天星期二");
                break;
            case 'c':
                System.out.println("今天星期三");
                break;
            case 'd':
                System.out.println("今天星期四");
                break;
            case 'e':
                System.out.println("今天星期五");
                break;
            case 'f':
                System.out.println("今天星期六");
                break;
            case 'g':
                System.out.println("今天星期日");
                break;
            default:
                System.out.println("你输入的不正确");
                break;
        }
        System.out.println("程序结束");

```

表达式数据类型，应和case后的常量类型一致，或者是可以自动转成可以相互比较的类型，比如输入的是字符，而常量是int

```java
        char a = 'a';
        switch (a) {
            case 'a':
                System.out.println("a");
                break;
            case 20:
                System.out.println("b");
                break;
            default :
                System.out.println("no");
        }
```

switch(表达式)中的表达式的返回值必须是：（byte、short、int、 char、enum[枚举]、 String）

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220223142207582.png)

case字句中的值必须是常量或者是常量表达式，而不是变量

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220223142830807.png)

default子句是可选的，当没有匹配的case时，执行default，如果没有default子句，又没有匹配任何常量，则没有输出

break语句用来在执行完一个case分支后使程序跳出switch语句块，如果没有写break，程序会顺序执行到switch结尾，除非遇到break

switch和if的比较

如果判断和具体数据不多，而且符合byte、short、int、char、enum[枚举]、String这6种类型，虽然两个语句都可以使用，建议使用switch语句

其他情况：对区间判断，对结果为doolean类型判断，使用if，if的使用范围更广

### 5.3 循环控制

#### 5.3.1 for循环控制

听其名而知其意，就是让你的代码可以循环的执行。

基本语法：

> for(循环变量初始化;循环条件;循环变量迭代){
>
> ​		循环操作(可以多条语句);
>
> }

for关键字，表示循环控制

for有四要素，(1)循环变量初始化(2)循环条件(3)循环操作(4)循环变量迭代

循环操作，这里可以有多条语句，也就是我们要循环执行的代码

如果循环操作(语句)只有一条语句，可以省略{}，建议不要省略

```java
        for (int i = 1; i <= 10; i++) {
            System.out.println("你个傻逼");
        }
```

循环条件是返回一个布尔值的表达式

for(;循环判断条件;)中的初始化和变量迭代可以写到其他地方，但是两边的分号不能省略

```java
        int a = 1;//循环变量初始化
        for(;a<10;){
            System.out.println("牛马");
            a++;
        }
```

循环初始值可以有多条初始化语句，但要求类型一样，并且中间用逗号隔开，循环变量迭代也可以有多条变量迭代语句，中间用逗号隔开

```java
        for (int i = 0, i1 = 5; i < 6; i++, i1--) {
            System.out.println(i + "+" + i1 + "=" + (i + i1));
        }
```

#### 5.3.2 while循环控制

基本语法：

> 循环变量初始化;
>
> while(循环条件){
>
> ​		循环体(语句);
>
> ​		循环变量迭代;
>
> }

while循环也有四要素

只是四要素放的位置和for不一样

```java
        int i = 1;
        while(i<=10){
            System.out.println("牛马"+i);
            i++;
        }
```

循环条件是返回一个布尔值的表达式

while循环是先判断在执行语句

#### 5.3.3 do...while循环控制

基本语法：

> 循环变量初始化;
>
> do{
>
> ​		循环体(语句);
>
> ​		循环变量迭代;
>
> }while(循环条件);

do while 是关键字

也有循环四要素，只是位置不一样

先执行，在判断，也就是说，一定会执行一次

最后有一个分号;

```java
        int i =1;
        do{
            System.out.println("牛马"+i);
            i++;
        }while (i<=10);
```

循环条件是返回一个布尔值的表达式

do...while循环是先执行，在判断，因此它至少会执行一次

#### 5.3.4 多重循环控制

将一个循环放在另一个循环体内，就形成了嵌套循环，其中，for、while、do...while、均可以作为外层循环和内层循环。[建议一般使用两层，最多不超过3层，否则代码的可读性很差]

实质上，嵌套循环就是把内层循环当成外层循环的循环体，当只有内层循环的循环条件为false时，才会完全跳出内层循环，才可结束外层的当次循环，开始下一次的循环

假设外层循环次数为m次，内层为n次，则内层循环体实际上需要执行m*n次

```java
        for (int i = 0;i<2;i++){
            for (int j = 0;j<3;j++){
                System.out.println("i="+i+"j="+j);
            }
        }
```

#### 5.3.5 跳转控制语句-break

break语句用于终止某个语句块的执行，一般使用switch或者循环中

基本语法：

> {......
>
> ​		break;
>
> ​		......
>
> }

```java
        for (int i = 0; i < 10; i++) {
            if (i==3){break;}//i==3时，执行break语句，跳出循环,提前结束当前循环
            System.out.println("i="+i);
        }
```

break语句出现在多层嵌套的语句块中时，可以通过标签指明要终止的是那一层语句块

标签的基本使用：

> label1:{......//标签的命名没有指定的，满足标签的命名规则就可以
>
> label2:	{......
>
> babel3:		{......
>
> ​						break label2;
>
> ​						......
>
> ​		}
>
> ​	}
>
> }

break语句可以指定退出那层

label1是标签

break后指定那个label就退出到哪里

在实际开发中，尽量不要使用标签

如果没有指定break，默认退出最近的循环体

**ps:随机生成数字方法：(int)(Math.random()*100)+1;**

#### 5.3.6 跳转控制语句-continue

continue语句用于结束本次循环，继续执行下一次循环

continue语句出现在多层嵌套的循环语句体中时，可以通过标签指明要跳过的是那一层循环，这个和前面的标签使用的规则一样

基本语法：

> {......
>
> ​	continue;
>
> ​	......
>
> }

```java
        for (int i = 0; i < 4; i++) {
            if (i==2){
                continue;
            }
            System.out.println("i="+i);
        }
```

#### 5.3.6 跳转控制语句-return

return使用在方法，表示跳出所在的方法，如果return写在mian方法，执行到就会退出程序

```java
        for (int i = 0; i < 5; i++) {
            if (i==2){
                System.out.println("牛马"+i);
                break;//退出循环
            }
            System.out.println("i="+i);
        }
        System.out.println("程序继续");

        for (int i = 0; i < 5; i++) {
            if (i==2){
                System.out.println("牛马"+i);
                continue;//退出当次循环
            }
            System.out.println("i="+i);
        }
        System.out.println("程序继续");

        for (int i = 0; i < 5; i++) {
            if (i==2){
                System.out.println("牛马"+i);
                return;//退出方法，写在main方法中就是退出程序
            }
            System.out.println("i="+i);
        }
        System.out.println("程序继续");

```

## 6.数组、排序和查找

### 6.1 数组

数组可以存放==多个同一类型的数据==。数组也是一种数据类型，是引用类型。即：数组就是一组数据

```java
        //定义一个数组
        double[] hens = {1,3,3.4,5,29,45,5,7.8,423.6,78.7};
        //double[] 表示是double类型的数组，数组名hens
        //{1,3,3.4,5,29} 表示数组的值/元素，依次表示数组的第几个元素

        double totalWeight  = 0;
        //遍历数组得到数组的所有元素的和，使用for
        //可以通过 数组名.length 得到数组的大小/长度
        System.out.println("数组的长度="+hens.length);
        for (int i = 0; i < hens.length; i++) {
            //可以通过hens[下标]来访问数组的元素
            //下标是从0开始编号的比如第一个元素就是hens[0],第二个就是hens[1]，依次类推
            //通过for就可以循环的访问数组的元素/值
            System.out.println("第"+(i+1)+"个数据的值是"+hens[i]);
            totalWeight +=hens[i];
        }
        System.out.println("总数量="+totalWeight+"平均数是="+(totalWeight/ hens.length));

```

#### **6.1.1 数组的使用方式1**-**动态初始化**

数组的定义

数据类型 数组名[] = new 数据类型[大小]

实例：int a[] = new int[5];--> 创建一个数组，名字为a 存放5个int

数组的引用(使用)

数组名[下标/索引]

数组的下标是从0开始的

```java
        Scanner scanner = new Scanner(System.in);
        //创建一个double数组,长度为5
        double scores[] = new double[5];
        //循环获取数值
        for (int i = 0; i < scores.length; i++) {
            System.out.println("请输入第"+(i+1)+"个元素的值");
            scores[i] = scanner.nextDouble();
        }
        //循环遍历数组的值并输出
        for (int i = 0; i < scores.length; i++) {
            System.out.println("第"+(i+1)+"个元素的值为"+scores[i]);
        }
```

#### **6.1.2 使用方法2-动态初始化**

先声明数组

语法：数据类型 数组名[]; 也可以 数据类型[] 数据名;

int a[]; 或者 int[] a;

创建数组

语法：数组名 = new 数据类型[大小];

a = new int[10];

```java
        double scores1[];//声明一个double的数组 这时的数组是空(null)
        scores1 = new double[5];//分配内存空间，可以存放数据
        //循环获取数值
        for (int i = 0; i < scores1.length; i++) {
            System.out.println("请输入第"+(i+1)+"个元素的值");
            scores1[i] = scanner.nextDouble();
        }
        //循环遍历数组的值并输出
        for (int i = 0; i < scores1.length; i++) {
            System.out.println("第"+(i+1)+"个元素的值为"+scores1[i]);
        }
```

#### 6.1.3 **使用方法3**-**静态初始化**

初始化数组

语法：数据类型 数组名[] = {元素值,元素值,.....}

> 参考数组最开始的代码

数组是多个相同类型数据的组合，实现对这些数据的统一管理

```java
        int[] arr = {1,3,4,56,3};//同数据，可以正常运行不报错
//        int[] arr = {1,3,4,56,3.2};//double->int  报错，类型不能转换
        double[] arr1 = {1,3,4,56,3.3};//int->double 可以，自动类型转换
```

数组中的元素可以是任何数据类型，包括基本类型和引用类型，但是不能混用

数组创建后，如果没有赋值，有默认值

>  int、short、byte、long的值是0
>
>  float、double的值是0.0
>
>  char的值是\u0000
>
>  boolean的值是false
>
>  String的值是null

```java
int[] arr4 = new int[3];//不赋值，里面全是0
for (int i = 0; i < arr4.length; i++) {
    System.out.println(arr4[i]);
}
```

使用数组的步骤：1.声明数组并开辟空间 2.个数组各个元素赋值 3.使用数组

数组的下标是从0开始的

数组的下标必须在指定范围内使用，否则报错：下标越界错误

>  int[] arr = new int[5]; 则有效的下标为0-4
>
>  即：数组的下标/索引 最小是0 最大是数组长度-1

```java
        int[] arr5 = new int[5];
        System.out.println(arr5[4]);
//        System.out.println(arr5[5]);//报错，数组越界
```

数组属于引用类型，数组型数据是对象(object)

### 6.2 **数组赋值机制**

基本数据类型赋值，这个值就是具体的数据，而且相互不影响

数组在默认情况下是引用传递/地址拷贝，赋的值是地址

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220305154544514.png)

```java
        //基本数据类型赋值，赋值方式为拷贝
        //n2的变化，不会影响到n1的值
        int n1 = 10;
        int n2 =n1;
        n2 = 39;
        System.out.println(n1);
        System.out.println(n2);

        //数组在默认情况下是引用传递/地址拷贝，赋的值是地址，赋值方式为引用赋值，是一个地址
        //arr2变化会影响到arr1
        int[] arr1 = {1,3,4};
        int[] arr2 = arr1;
        arr2[0] = 19;

        for (int i = 0; i < arr1.length; i++) {
            System.out.println("arr1="+arr1[i]);
        }
        for (int i = 0; i < arr2.length; i++) {
            System.out.println("arr2="+arr2[i]);
        }
```

#### 6.2.1 **数组的拷贝**

```java
int[] arr = {10,39,489};
//创建一个新的数组，开辟新的数据空间
int[] arr3 = new int[arr.length];//新的数组长度和arr的数据长度一样
//遍历arr的数值/元素，把每个元素拷贝到arr3中对应的位置
for (int i = 0; i < arr.length; i++) {
    arr3[i] = arr[i];
}
arr3[2] = 29;//修改arr3中的值，不会对arr有影响
//循环遍历每个数组，看看结果如何
for (int i = 0; i < arr.length; i++) {
    System.out.println("arr="+arr[i]);
}
for (int i = 0; i < arr3.length; i++) {
    System.out.println("arr3="+arr3[i]);
}
```

#### 6.2.2 **数组的反转**

```java
//自己的想法：
int[] arr4 = {11,22,33,44,55,66,77,88,99,1010};//定义数组
//定义一个新的数值
int[] arr5 = new int[arr4.length];
//遍历数组的内容，将arr4的元素拷贝到arr5
for (int j=0;j<arr4.length; j++) {
    arr5[j]=arr4[j];
}
//将arr5中的数据反向拷贝(逆序遍历)到arr4数组中去(正序拷贝)，实现反转
for (int i = (arr4.length-1),j=0; i >=0 ; i--,j++) {
    arr4[j] = arr5[i];//i是逆序，j是正序
    System.out.print(arr4[j]+"\t");
}

System.out.println(" ");

//老师的思路
//int[] arr6 = {11,22,33,44,55,66};
//规律
//1，把arr[0]和arr[5]进行交换
//2.把arr[1]和arr[4]进行交换
//3.把arr[2]和arr[3]进行交换
//4.一共要交换3次 = arr6.length/2
//5.每次交换时，对应的下标时arr6[i]和 arr6[arr6.length-1-i]
int[] arr6 = {11,22,33,44,55,66};
for (int i = 0; i < arr6.length/2; i++) {
    int temp = arr6[arr6.length-1-i];//临时变量，储存数据
    arr6[arr6.length-1-i]=arr6[i];//将开头的转换给结尾
    arr6[i] = temp;//将临时保存的结尾的传递给开头的
}
//查看最后的结果
for (int i = 0; i < arr6.length; i++) {
    System.out.print(arr6[i]+"\t");
}
```

#### 6.2.3 **数组添加**

```java
//定义一个数组
int[] arr = {1,2,3};
//定义一个新的数组
int[] arrnew = new int [arr.length+1];
//遍历arr数组，将每个元素拷贝到arrnew数组
for (int i = 0; i < arr.length; i++) {
    arrnew[i] = arr[i];
}
//将新的元素赋值给arrnew最后的一个元素
arrnew[arrnew.length-1] = 4;
//让arr指向arrnew数组
arr = arrnew;
//遍历看最后的结果
for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i]+"\t");
}

Scanner scanner = new Scanner(System.in);
while (true){
    System.out.println("当前数据长度"+arr.length);
    System.out.println("你要添加数据吗：y/n");
    char order = scanner.next().charAt(0);
    //判断是否要添加数据
    if (order == 'y'){
        //定义一个新的数组，长度是arr的长度加一
        int[] arrnew1 = new int[arr.length+1];
        System.out.println("添加后的长度"+arrnew1.length);
        //遍历arr数组，将每个元素拷贝到arrnew1数组
        for (int i = 0; i < arr.length; i++) {
            arrnew1[i] = arr[i];
        }
        //将要添加的元素赋值给数组最后一位
        System.out.println("输入你要添加的数字");
        arrnew1[arrnew1.length-1] = scanner.nextInt();//直接将获得的元素赋值给数组最后的一个元素
        //让arr指向arrnew1数组的地址
        arr = arrnew1;
        //遍历数组查看最后的结果
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]+"\t");
        }
    }else{
        break;
    }
}
```

#### 6.2.4 **数组的缩减**

和添加异曲同工

```java
//数组的缩减
//定义初始数组
int[] arr1 = {1,2,3,4,5,6};
while (true){
    System.out.println("你要缩减数组内的元素吗");
    char order = scanner.next().charAt(0);
    //判断是否要缩减
    if (order == 'y'){
        //判断数组是否只剩最后一个元素
        if (arr1.length==1){
            System.out.println("只有一个元素了，不能在缩减了");
            break;
        }else{
            //定义一个变量，长度是原数组的长度减一
            int[] arrnew1 = new int[arr1.length-1];
            //遍历赋值
            for (int i = 0; i < arrnew1.length; i++) {
                arrnew1[i] = arr1[i];
            }
            //让原数组指向缩减后的数组
            arr1 = arrnew1;
            //查看结果
            for (int i = 0; i < arr1.length; i++) {
                System.out.print(arr1[i]+"\t");
            }
        }
    }else{
        break;
    }
}
```

### 6.3 排序

排序是将多个数据，依指定的顺序进行排列的过程

排序的分类：

> 内部排序：
>
> 指将需要处理的所有数据都加载到内部存储器中进行排序，包括(交换式排序法、选择式排序法和插入式排序法)
>
> 外部排序法：
>
> 数据量过大，无法全部加载到内存中，需要借助外部存储进行排序，包括(合并排序法和直接合并排序法)

#### 6.3.1 冒泡排序法

冒泡排序的基本思想是：通过对待排序序列从后向前(从下标较大的元素开始)，依次比较相邻的元素的值，若发现逆序则交换，是值较大的元素逐渐从前移向后部，就像水底下的气泡一样逐渐向上冒。

冒泡排序法的特点：

> 当数组有n个元素时，会进行n-1次的排序，可以看成是一个外层循环
>
> 每1轮排序可以确定一个数的位置，比如：第一轮排序确认最大数的位置，第二轮排序确认第二大的数位置，以此类推
>
> 当进行比较时，如果前面的数大于后面的数，就交换
>
> 每轮比较的次数在减少，因为每比较一轮就会确认一个元素的位置，所以下一次的比较次数就会减少

```java
//定义数组
int[] arr = {15,789,74,687,45,65,879,451,78,256,85};
//定义一个变量来存储数值，辅助交换
int temp = 0;
//定义一个变量，该变量是表示要比较几轮
int num = arr.length-1;
//进行轮循环
for (int i = num; i>0; i--) {
    //每轮中进行循环比较，来确定数的位置
    for (int j = 0; j < num; j++) {
        //判断前面的数是否大于后面的数
        if (arr[j]>arr[j+1]){
            //进行交换
            temp = arr[j];//将前面那个元素的值先赋值给temp
            arr[j] = arr[j+1];//将后面元素的值赋值给前面的元素
            arr[j+1] = temp;//将temp中保存的前元素的值赋值给后面元素的值，这样就完成了前元素与后元素的交换了
        }
    }
}

//查看最后的结果
for (int i = 0; i < arr.length; i++) {
    System.out.print(arr[i]+"\t");
}
```

### 6.4 查找

在java中，常用的查找有两种：

顺序查找

二分查找[二分法]

```java
//顺序查找
//定义数组
String[] name = {"牛马","北京大学","清华大学","南京大学","斯坦福"};
Scanner scanner = new Scanner(System.in);
System.out.println("输入你要查找的大学");
String seq = scanner.next();
int index = -1;
for (int i = 0; i < name.length; i++) {
    if (name[i].equals(seq)){//字符串的比较方法
        System.out.println("有你要找的大学，下标位置在"+i);
        index = i;
        break;//退出循环
    }
}

if (index == -1){
    System.out.println("没有找到"+seq);
}
```

### 6.5 多维数组-二维数组

二维数组就是：

> 从定义形式上看 int后面两个[]
>
> 原来的一维数组的每个元素是一个一维数组，就构成了二维数组
>
> 二维数组的每个元素都是一维数组，所以如果需要得到每个一维数组的值，就需要再次遍历

```java
//定义一个二维数组
int arr[][] = {{0,0,0,0,0,0},{0,1,2,3,0,4},{0,0,0,0,7,5},{0,0,0,0,0,0,}};
//遍历每个二维数组的每个元素
for (int i = 0; i < arr.length; i++) {
    //遍历二维数组的每个元素(数组)
    //arr[i] 表示 二维数组的第i+1个元素 比如arr[i]：二维数组的第一个元素
    //arr[i].length 得到，对应的每一个一维数组的长度
    for (int j = 0; j < arr[i].length; j++) {
        System.out.print(arr[i][j]+" ");//输出了一维数组
        //arr[i][j]->访问arr数组第(i+1)个元素(一维数组)中的第(j+1)个元素的值，下标一样是从0开始
    }
    System.out.println();//换行
}
```

**二维数组的使用方式**

使用方式1：动态初始化

```java
//语法：类型[][] 数组名 = new 类型[大小][大小]
//第一个大小表示数组包含几个一维数组，第二个大小表示每个一维数组有几个元素

        //动态初始化定义二维数组
        int[][] arr1 = new int[2][3];
        //遍历二维数组
        for (int i = 0; i < arr1.length; i++) {
            for (int j = 0; j < arr1[i].length; j++) {
                System.out.print(arr1[i][j] + " ");
            }
            System.out.println();
        }
```

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220306113424953.png)

使用方式2：动态初始化2

先声明二维数组，再开辟内存空间

```java
//声明二维数组
int arr2[][];
arr2 = new int[2][3];//再开辟内存空间
```

使用方法3：动态初始化-列数不确定

```java
int[][] arr3 = new int[3][];//列数不确定 创建二维数组，但是只是确定一维数组的个数，每个一维数组还没有开数据空间
//遍历arr每个一维数组
for (int i = 0; i < arr3.length; i++) {
    //给每个一维数组开辟空间
    //如果没有给一维数组new，那么arr[i]就是null
    arr3[i] = new int[i+1];
    //遍历一维数组，并给一维数组的每个元素赋值
    for (int j = 0; j < arr3[i].length; j++) {
        arr3[i][j] = i+1;
    }
}

//遍历查看结果
for (int i = 0; i < arr3.length; i++) {
    for (int j = 0; j < arr3[i].length; j++) {
        System.out.print(arr3[i][j] + " ");
    }
    System.out.println();
}
```

使用方法4：静态初始化

```java
int arr[][] = {{0,0,0,0,0,0},{0,1,2,3,0,4},{0,0,0,0,7,5},{0,0,0,0,0,0,}};
```

二维数组实际上就是由多个一维数组组成的，它的各个一维数组的长度可以相同，也可以不相同，长度不行同的也称为列数不等的二维数组

## 7.面向对象编程(基础部分)

### 7.1 类与对象 

java设计者引入类与对象(oop)，根本原因就是现有的技术，不能完美的解决新的需求

==**对象[属性,行为]**==

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220306122919763.png)

类就是数据类型，比如cat

对象就是一个具体的实例

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220306123207648.png)

```java
public class Object01 {
    public static void main(String[] args) {

        //使用oop面向对象
        //创建一个对象
        Cat cat1 = new Cat();//将创建的对象赋值给cat1，所以cat1就是一个对象
        //new Cat()  -> 创建一个新的对象
        cat1.name = "马超";//给属性name赋值
        cat1.age = 20;
        cat1.color = "黄色";

        //访问对象
        System.out.println("信息=="+cat1.name+" "+cat1.age+" "+cat1.color);

    }
}

//定义一个类 -> 自定义的数据类型
class Cat{
    //属性
    String name;//名字
    int age;//年龄
    String color;//颜色
}
```

类是抽象的，概念的，代表一类事物，比如人类、猫类...即它是数据类型

对象是具体的，实际的，代表一个具体事物，即是实例

类是对象的模板，对象是类的一个个体，对应一个实例

#### 7.1.1 **对象在内存中的存在形式(重点)**

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220306145547123.png)

创建对象时，会在方法区先加载cat类的信息

然后为每个数据分配空间，根据属性不一样会分配不同的空间

如果时字符串就会分配一个地址，然后在指向常量池，如果时基本数据类型，就直接存放

最后把地址返回给对象

#### 7.1.2 **属性/成员变量**

从概念或叫法上看：成员变量 = 属性 = field(字段) （即，成员变量是用来表示属性的）

属性是类的一个组成部分

属性的定义语法同变量，示例：访问修饰符 属性类型 属性名;

访问修饰符：控制属性的访问范围

有四种访问修饰符：public、proctected、默认(不写就是默认)、private

属性可以是基本数据类型，也可以是引用类型(对象，数组)

属性如果不赋值，有默认值，规则和数组一致：

> int、short、byte、long的值是0
>
> float、double的值是0.0
>
> char的值是\u0000
>
> boolean的值是false
>
> String的值是null

```java
public class Property {
    public static void main(String[] args) {

        //创建对象
        Passer p1 = new Passer();
        //new Passer();  创建的对象空间(数据)才是真正的对象
        //p1叫做对象引用(对象名)，意思是p1指向对象，比如：小明不是一个人，是一个人的名字

        //查看当前的属性默认值
        System.out.println("name="+p1.name+" age="+p1.age+" inpass="+p1.inpass+" money="+p1.money);

    }
}

//创建类
class Passer {
    String name;
    int age;
    boolean inpass;
    double money;
}
```

#### 7.1.3 对象的创建

**1.先声明在创建：**

Cat cat;//声明对象

cat = new Cat();//创建

**2.直接创建：**

Cat cat = new Cat();

**访问属性：**

对象名.属性名;//基本语法

#### 7.1.4 类和对象的内存分配机制

**[视频讲解地址](https://www.bilibili.com/video/BV1fh411y7R8?p=199&spm_id_from=pageDriver)**

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220306161510072.png)

```java
p1.age = 10;
p1.name = "王刚";
Passer p2 = p1;
System.out.println(p2.age);
```

java内存的结构分析：

> 栈：一存放基本数据类型(局部变量)
>
> 堆：存放对象(Cat cat、数组等)
>
> 方法区：常量池(常量、比如字符串)、类加载信息

```java
Person p = new Person();
p.name = "牛马";
p.age = 19;
/*
java创建对象的流程简单分析：
1.先在方法区加载person类信息(属性和方法信息，只会加载一次)
2.在堆中分配空间，进行默认初始化(看规则)
3.把地址赋给p。p就指向对象
4.进行指定初始化 比如：p.name = "牛马";
*/
```

```java
//练习
Passer a = new Passer();
a.age = 10;
a.name = "马亮";
Passer b;
b = a;
System.out.println(b.name);
b.age = 200;
b = null;//把b滞空，即b没有了指向，也不是一个对象了
System.out.println(a.age);
System.out.println(b.age);//b现在是空，也不是对象了，所以这里会异常
```

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220306163554751.png)

### 7.2 成员方法

在某些情况下，我们需要定义成员方法(简称方法) 。比如人类：除了有一些属性外，还有一些行动：比如跑步，说话等。这时就要用成员方法才能完成了。

```java
public class Method {
    public static void main(String[] args) {

        //方法使用
        //1.方法写好后，如果不去调用(使用)，不会输出
        //2.先创建对象，然后调用方法即可
        Person p = new Person();
        p.speak();//调用方法
        p.colo1();
        p.colo2(38);//调用方法，并且给了n=38
        //调用方法getSum，同时给两个形参赋值
        //吧方法getSum返回的值赋给变量res
        int res = p.getSum(19,13);
        System.out.println("getSum返回的值="+res);

    }
}
//创建类
class Person{
    //属性
    String name;
    int age;

    //方法
    public void speak(){
        System.out.println("我是好人");
    }
    //1. public ： 表示方法是公开的
    //2. void ： 表示方法没有返回值
    //3. speak() ： speak是方法名 ()是形参列表
    //4. {} 方法体，可以写我们要执行的代码

    public void colo1(){
        int sum = 0;
        for (int i = 0; i <=1000 ; i++) {
            sum += i;
        }
        System.out.println("累加的结果为"+sum);
    }

    //(int n) 形参列表 表示当前有一个形参n 可以接收用户的输入
    public void colo2(int n){
        int sum = 0;
        for (int i = 0; i <=n ; i++) {
            sum += i;
        }
        System.out.println("从1加到"+n+",累加的结果为"+sum);
    }

    //int：表示方法执行后，返回一个int值
    //(int num1,int num2)：形参列表，2个形参，表示可以接收两个数据
    //return res; ：表示吧res的值返回
    public int getSum(int num1,int num2){
        int res = num1+num2;
        return res;
    }

}
```

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220307144431970.png)

**[图片视频讲解](https://www.bilibili.com/video/BV1fh411y7R8?p=204&spm_id_from=pageDriver)**

成员方法带来的好处：

> 提高了代码的复用性
>
> 可以将实现的细节封装起来，然后供其他用户调用即可

#### 7.2.1 方法的定义

```java
//public就是访问修饰符
访问修饰符 返回数据类型 方法名 (形参列表...) {//方法体
    语句;
    return 返回值;
}
```

> 访问修饰符：作用是控制方法使用范围(有四种：public、protected、默认、private。如果不写就是默认访问)
>
> 形参列表：表示成员方法输入
>
> 数据类型(返回类型)：表示成员方法输出，void 表示没有返回值
>
> 方法主体：表示为了实现某一功能代码块
>
> return 语句不是必须的
>
> 可以结合前面的示意图来理解

#### **7.2.2 返回数据类型**

> 一个方法最多有一个返回值【如果要返回多个值，可以使用数组来返回】
>
> ```java
> public class Method02 {
>     public static void main(String[] args) {
>         Arr a = new Arr();
>         //定义一个数组变量来接收方法返回的值
>         //什么类型的返回值就要用什么类型的变量来接收
>         int[] arr = a.getarr(1,4);
>         System.out.println("和=" +arr[0]);
>         System.out.println("差=" +arr[1]);
> 
>     }
> }
> 
> class Arr{
>     //int[] 返回的结果是一个数组
>     //一个方法只能返回一个值，但返回值的类型是数组的时候就可返回多个值
>     public int[] getarr(int num1,int num2){
>         int[] res = new int[2];//定义一个数组
>         res[0]= num1+num2;//两数之和
>         res[1]= num1-num2;//两数之差
>         return res;
>     }
> }
> ```
>
> 返回类型可以为任意类型，包含基本类型和引用类型(数组，对象)
>
> 如果方法要求有返回数据类型，则方法体中最后的执行语句必须为return 值;而且要求返回值类型必须和return的值类型一致或兼容
>
> 如果方法是void，则方法体中可以没有return语句，或者只写return ;不能带值

#### 7.2.3 形参列表

一个方法可以有0个参数，也可以有多个参数，中间用逗号隔开

参数类型可以是任意类型，包含基本数据类型和引用类型

调用带参数的方法时，一丁对应着参数列表传入相同类型或兼容类型的参数

方法定义时的参数称为形式参数，简称形参；方法调用时的传入参数称为实际参数，简称实参，实参和形参的类型要一致或兼容、个数、顺序必须一致

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220307160222610.png)

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220307160702605.png)

#### 7.2.4 方法体

方法体里面写完成功能得具体语句，可以为输入、输出、变量、运算、分支、循环、方法调用，但是里面不能在定义方法，即方法不能嵌套定义

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220307161142192.png)

#### 7.2.5 方法的调用

同一个类中的方法调用：直接调用即可

```java
public class Method03 {
    public static void main(String[] args) {
        AA a = new AA();
        a.sayOk();

    }
}

class AA{
    //同一个类中的方法调用：直接调用即可
    public void print(int n){
        System.out.println("我被调用了 n="+n);
    }
    public void sayOk(){//sayOk调用print
        print(10);
        System.out.println("继续执行");
    }
}
```

跨类中的方法A类调用B类方法：需要创建对象名调用

```java
public class Method03 {
    public static void main(String[] args) {
        AA a = new AA();
        a.m1();

    }
}

class AA{
    //跨类中的方法A类调用B类方法：需要创建对象名调用
    public void m1(){
        //创建b类对象，然后在调用方法即可
        BB b = new BB();
        b.hi();
        System.out.println("继续执行");
    }
}

class BB{
    public void hi(){
        System.out.println("我是b类的方法");
    }
}
```

跨类的方法调用和方法的访问修饰符相关

#### 7.2.6 成员方法的传参机制

```java
public class MethodParameter {
    public static void main(String[] args) {
        Parameter par = new Parameter();
        int a = 1;
        int b = 2;
        par.swap(a,b);
        System.out.println("a="+a+"b="+b);//1，2
    }
}

class Parameter{
    public void swap(int a,int b){
        System.out.println("a="+a+"b="+b);//1，2
        //两个数的互换
        int temp = a;
        a = b;
        b = temp;
        System.out.println("a="+a+"b="+b);//2，1
    }
}
```

对于基本数据类型，传递的是值(值拷贝)，形参的任何改变不影响实参

```java
public class MethodParameter01 {
    public static void main(String[] args) {

        Parameter01 par = new Parameter01();
        int[] arr = {1,3,4};
        par.teas(arr);
        System.out.println("\nmain的arr数组");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }

    }
}

class Parameter01{
    public void teas(int[] arr){
        arr[0] = 10;
        //遍历数组
        System.out.println("teas的arr数组");
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i] + " ");
        }
    }

}
```

引用类型传递的是地址(传递也是值，但是值是地址)，可以通过形参影响实参。总结：引用传递本质是传递地址，而相同的地址指向的是堆区的同一块，因为是修改的地址，所以一改全改

### 7.3 对象的拷贝

```java
public class MethodExercise01 {
    public static void main(String[] args) {

        Mytools01 my = new Mytools01();
        Parse p = new Parse();
        p.age = 13;
        p.name = "牛马";
        System.out.println("p.age=" + p.age + " p.name=" + p.name);
        Parse p1 = my.cloning(p);
        //p1和p就都是Parse对象了，但是是两个独立的对象，属性相同
        System.out.println("p1.age=" + p1.age + " p1.name=" + p1.name);
        //可以通过对象比较来看看是否是同一个对象
        System.out.println(p==p1);//同一个返回true，不是相同返回false
    }
}

class Parse {
    int age;
    String name;
}

class Mytools01 {
    
    //对象的拷贝
    //方法的返回类型是Parse
    public Parse cloning(Parse p) {
        //第一种，创建一个新的对象，将原先的数据复制到新的
        Parse p1 = new Parse();
        p1.age = p.age;
        p1.name = p.name;

        //第二种，开辟一个新的空间，给新空间赋值原空间的数值
        int age = p.age;
        String name = p.name;
        p = new Parse();
        p.age = age;
        p.name = name;

        //两种方式都可以，
//        return p1;
        return p;
    }
}
```

### 7.4 方法递归调用

简单地说：递归就是方法自己调用自己，每次调用是传入不同的变量，递归有助于编程者解决复杂问题，同时可以让代码变得简洁

```java
public class Recursion {
    public static void main(String[] args) {
        Recur r = new Recur();
        r.test(5);
    }
}

class Recur{
    public void test(int n){
        if (n>2){
            test(n-1);//递归
        }
        System.out.println("n="+n);
    }
}
```

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220312161624417.png)

[**视频讲解**](https://www.bilibili.com/video/BV1fh411y7R8?p=216&spm_id_from=pageDriver)

```java
//阶乘
public int factorial(int n){
    if (n==1){
        return 1;
    }else{
        return factorial(n-1)*n;
    }
}
```

递归的规则：

> 执行一个方法时，就创建一个新的受保护的独立空间(栈空间)
>
> 方法的局部变量时独立的，不会相互影响(基本数据类型)
>
> 如果方法中使用的时引用类型变量(比如数组，对象)，就会共享该引用类型的数据
>
> 递归必须向退出递归的条件逼近，否则就是无限递归，出现死龟了
>
> 当一个方法执行完毕，或者遇到了return就会返回，遵守谁调用，就将结果返回给谁，同时当方法执行完毕或者返回时，该方法也就执行完毕

**总结：递，就是把当前方法通过一些计算得到的参数传递到下一个方法(自己)，告诉他，这是你要的参数**

​			**归，就是把结果(可能是真\假或者某个数值)返回给上一个方法，告诉他，这是你要的答案，如果答案不满意你可以进行回溯**

#### 7.4.1 递归经典习题：老鼠出迷宫

```java
public class MouseGoMiGong {
    public static void main(String[] args) {
        //实现思路
        //1.先创建迷宫，用二维数组表示
        int[][] map = new int[8][7];
        //2.规定数组中的元素值为0表示是老鼠可以走的路，1是不能走的路
        //3.将最上面一行和最下面一行，全部设置为1
        for (int i = 0; i < 7; i++) {
            map[0][i] =1;
            map[7][i] =1;
        }
        //4.将最右边的一列和最左边的一列，全部设置为1
        for (int i = 0; i < 8; i++) {
            map[i][0] =1;
            map[i][6] =1;
        }
        //5.设置障碍物
        map[3][1]=1;
        map[3][2]=1;

        //调用方法
        MouseToMiGong mtg = new MouseToMiGong();
        mtg.findWay(map,1,1);



        //查看当前地图：
        for (int i = 0; i < 8; i++) {
            for (int j = 0; j < 7; j++) {
                System.out.print(map[i][j]+" ");
            }
            System.out.println();
        }


    }
}

class MouseToMiGong{

    //使用递归回溯的思想来解决老鼠出迷宫

    //1.返回值为boolean来判断是否出了迷宫
    //2.int[][]map是地图
    //3.i，j是坐标位置
    //4.因为是递归的找路，所以先规定map数组的各个值的含义
    //  0表示可以走但是没有走过、1表示障碍物、2表示可以走、3表示走过，但是走不通的路
    //5.当map[6][5]=2就说明找到通路，就可以结束，否则继续找
    //6.确定老鼠找路的策略：下->右->上->左
    public boolean findWay(int[][] map,int i,int j){

        if (map[6][5]==2){//表示找到了出路
            return true;
        }else {
            if (map[i][j]==0){//当前位置为0，说明没有走过，可以走
                //先假定可以走通
                map[i][j]=2;
                //使用找路策略来判断是否真的走通了
                if (findWay(map,i+1,j)){//向下走
                    return true;
                }else if (findWay(map,i,j+1)){//向右
                    return true;
                }else if (findWay(map,i-1,j)){//向下
                    return true;
                }else if (findWay(map, i,j-1)){//向左
                    return true;
                }else{
                    map[i][j]=3;//表示走过，但是走不通的路
                    return false;
                }
            }else {//map[i][j]=1\2\3
                return false;
            }
        }

    }

}
```

#### 7.4.2 递归经典习题：汉诺塔

```java
public class HanLuoTa {
    public static void main(String[] args) {

        Ta ta = new Ta();
        ta.move(3,'A','B','C');

    }
}

class Ta {
    //num表示要移动的个数，a，b，c别表示啊三个塔
    //形参abc不是固定对应实参ABC的三根柱子，而是“起点”，“过度”，“终点”三根柱子
    //“起点”，“过度”，“终点”都是形参
    public void move(int num, char a, char b, char c) {
        //如果只有一个盘 num==1
        if (num == 1) {
            System.out.println(a + "->" + c);
        }
        //else代码中的内容：
        //A上面的一摞(num-1)挪到B,所有是“起点”=A，“过度”=C，“终点=B”
        //(num-1)挪回A之后，之前A最底下的，已经挪到C最底下了
        else{
            //如果有多个盘，可以看成两个，最下面的和上面的所有盘
            //(1)先移动上面的所有盘到b，借助c
            move(num-1,a,c,b);
            //(2)把最下面的这个盘，移动到c
            System.out.println(a+"->"+c);
            //(3)再把b塔的所有盘移动到c借助a
            move(num-1,b,a,c);
        }

    }

}
```

#### 7.4.3 递归经典习题：八皇后

```java
public class EightQueen {
    public static void main(String[] args) {
        int[] nums = new int[8];//定义一个一维数组
        Eight eight = new Eight();
        eight.Queen(nums,0,0);
    }
}

class Eight{
    //定义一个变量，来统计一共有多少种方法
    int sum =0;
    //数组用来保存八个皇后的位置，该数组中的下标就是代表了行，数组内每个元素为皇后在该下标行的那列
    //i为探测用的行，j为列
    public void Queen(int[] nums,int i,int j){
        //j为列，当j的长度超过了数组的最大长度的时候，就结束方法
        if (j==nums.length){
            return;
        }
        //i为行，当i的长度超过了数组的最大长度的时候，就说明这个摆法可行，结束方法
        if (i==nums.length){
            sum++;//计数器加一
            print(nums);//调用方法来打印结果
            return;
        }
        if(judge(nums,i,j)) {//调用方法判断各个方向是否有皇后
            nums[i] = j;   //为true则在数组中存入该位置
            Queen(nums,i+1,0);//从0列继续探测下一行,
        }
        Queen(nums,i,j+1);//这里不是用else连接。因为我们是要找出所有可行结果，不管上面是怎样，我们都要往后面找出所有的可能
    }

    //定义方法来判断皇后的四周是否有其他的皇后
    public boolean judge(int[] nums,int i,int j){
        for(int k = 0;k <i ;k++) {//循环判断各个方向是否有皇后
            //因为行就是i所有不用考虑同行是否有皇后
            //nums[k] == j 这个是判断同列是否有皇后的存在
            //对角线的判断公式是：x1-x2=y1-y2，这个要是成立，就代表对角线存在皇后
            //Math.abs是用来求绝对值
            if(nums[k] == j || i-k  == Math.abs(j - nums[k])) {// i-k  == j-nums[k] || i-k == -(j-nums[k])
                return false;
            }
        }
        return true;
    }

    //定义方法，来打印八皇后摆放的结果
    public void print(int[] nums){
        System.out.println("第"+sum+"种摆放方法");
        for(int i = 0;i < nums.length;i++) {
            System.out.print(nums[i] + "  ");
        }
        System.out.println();
    }

}
```

### 7.5 方法重载

java中允许同一个类中，多个同名方法的存在，但要求形参列表不一致

重载减轻了起名的麻烦和记名的麻烦

```java
public class Overloading {
    public static void main(String[] args) {

        MyCalculator my = new MyCalculator();
        System.out.println(my.calculate(1, 3));
        System.out.println(my.calculate(1, 3.5));
        System.out.println(my.calculate(1.5, 3));
        System.out.println(my.calculate(1, 3,8));

    }
}

class MyCalculator {
    //下面的四个calculate方法构成了重载
    public int calculate(int n1, int n2) {//计算两个整数的和
        return n1 + n2;
    }

    public double calculate(int n1, double n2) {//整数和浮点数的和
        return n1 + n2;
    }

    public double calculate(double n1, int n2) {//浮点数和整数的和
        return n1 + n2;
    }

    public int calculate(int n1, int n2, int n3) {//三个整数的和
        return n1 + n2 + n3;
    }
}
```

方法重载的使用注意事项：

> 方法名必须相同
>
> 形参列表：必须不同(参数类型或个数或顺序，至少有一样不同，参数名无要求)
>
> 返回类型无要求

### 7.6 可变参数

java允许将同一个类中多个同名同功能但参数个数不同的方法，封装成一个方法，就可以通过可变参数实现

基本语法：

> 访问修饰符 返回类型 方法名(数据类型... 形参名){
>
> }

```java
public class VariableParameter {
    public static void main(String[] args) {

        Variable var = new Variable();
        var.sum();
        System.out.println("接收参数的和="+var.sum(5,8,5,78));
        //可变参数的实参可以为数组
        int[] arr = {1,5,4,8,7};
        System.out.println("接收参数的和="+var.sum(arr));
        
        var.sum1("牛马");

    }
}
 
class Variable{
    //1.int... 表示接收的是可变参数，类型是int，即可以接收多个int(0-多)
    //2.使用可变参数时，可以当做数组来使用，即sums可以当作数组
    //3.通过遍历来求多个数字的和
    public int sum(int... nums){
        System.out.println("接收的参数个数="+nums.length);
        int sum=0;
        for (int i = 0; i < nums.length; i++) {
            sum += nums[i];
        }
        return sum;
    }
    
    //可变参数可以和普通类型的参数一起放在形参列表，但必须保证可变参数在最后
    public void sum1(String str,int... nums){
        System.out.println("接收传入的数组为="+str);
        System.out.println("可变参数接收到="+nums.length+"位");
    }
    
}
```

可变参数使用细节：

> 可变参数的实参可以为0个或任意多个
>
> 可变参数的实参可以为数组
>
> 可变参数的本质就是数组
>
> 可变参数可以和普通参数类型的参数一起放在参数列表，但必须保证可变参数在最后
>
> 一共形参列表中只能出现一个可变参数

### 7.7 作用域

在java得面向对象中，变量作用域时非常重要得知识点

> 在java编程中，主要的变量就是属性(成员变量)和局部变量
>
> 局部变量一般是指在成员方法中定义的变量
>
> 全局变量：也就是属性，作用域是整个类体
>
> 局部变量：也就是除了属性之外的其他变量，作用域为定义它的代码块中
>
> 全局变量(属性)可以不赋值，直接使用，因为有默认值，局部变量必须赋值后，才能使用，因为没有默认值

```java
public class Scope {
    public static void main(String[] args) {

        VariableScope vars = new VariableScope();
        //属性的生命周期比较长，伴随着对象的创建而创建，伴随着对象的销毁而销毁。局部变量的生命周期较短，伴随着它的代码块的执行而创建，伴随着代码块的结束而销毁。即在一次方法调用过程中生效
        vars.say();//当执行say方法时，say方法的局部变量会创建，比如age，当say执行完毕后，age局部变量就销毁，但是属性(全局变量)任然可以使用
        VariableScope1 var = new VariableScope1();
        var.test(vars);//将main方法中的vars对象的地址指向传递给方法

    }
}

class VariableScope1{
    public void test(){
        //在其他类通过对象的调用使用VariableScope类中的age变量
        VariableScope var = new VariableScope();
        System.out.println(var.age);
    }

    public void test(VariableScope var){//接收后，这里的var就也指向了main方法中的vars的地址
        System.out.println(var.age);//所以这里就直接访问，访问的也是Var中的age属性
    }
}

class VariableScope{
    //全局变量：也就是属性，作用域是整个类体
    //属性在定义时，可以直接赋值
    //属性可以加修饰符
    public int age = 19;

    //全局变量(属性)可以不赋值，直接使用，因为有默认值
    double d;//默认值0.0

//    public void eat(){
//        //局部变量必须赋值后，才能使用，因为没有默认值
//        int num;
//        System.out.println(num);//报错，变量未初始化
//    }

    public void say(){
        //局部变量一般是指在成员方法中定义的变量
        //n 和 name 就是局部变量
        //n 和 name的作用域在say方法中
        int n;
        String name;
        //属性和局部变量可以重名，访问时遵循就近原则
        int age= 29;
        System.out.println("在say方法中使用全局变量age age="+age);//就近
        System.out.println(d);
    }

    {
         String str ="牛马";//在代码块中定义了局部变量
    }

}
```

作用域使用细节：

> 属性和局部变量可以重名，访问时遵循就近原则
>
> 在同一个作用域中，两个局部变量不能重名
>
> 属性的生命周期比较长，伴随着对象的创建而创建，伴随着对象的销毁而销毁。局部变量的生命周期较短，伴随着它的代码块的执行而创建，伴随着代码块的结束而销毁。即在一次方法调用过程中生效
>
> 作用域范围不同：
>
> ​	全局变量/属性：可以被本类使用，或其他类使用(通过对象调用)
>
> ```java
> class VariableScope1{
>     public void test(){
>         //在其他类通过对象的调用使用VariableScope类中的age变量
>         VariableScope var = new VariableScope();
>         System.out.println(var.age);
>     }
> }
> 
> class VariableScope{
>     int age = 19;
> }
> ```
>
> ​	局部变量：只能在本类中对应的方法中使用
>
> 修饰符不同：
>
> ​	全局变量/属性可以加修饰符
>
> ​	局部变量不可以加修饰符

### 7.8 构造方法/构造器

看一个需求：前面在创建人类的对象时，是先把一个对象创建好后，在给它的年龄和姓名属性赋值，如果现在要求，在创建人类的对象时，就直接指定这个对象的年龄和姓名，该怎么做？这时就可以使用构造器

构造方法又叫构造器，是类的一种特殊的方法，它的主要作用是完成对**==新对象的初始化==**，它有几个特点：

> 方法名和类名一样
>
> 没有返回值
>
> 在创建对象时，系统会自动和调用该类的构造器完成对对象的初始化

基本语法：

> [修饰符] 方法名 (形参列表){
>
> ​		方法体;
>
> }
>
> 构造器的修饰符可以默认，也可以是其他的
>
> 构造器没有返回值
>
> 方法名和类名字必须一样
>
> 参数列表和成员方法一样的规则
>
> 构造器的调用系统完成

```java
public class Constructor {
    public static void main(String[] args) {

        //当我们创建新的对象时，直接通过构造器指定元素的值
        ConstructorPerson cop = new ConstructorPerson("马亮",28);
        System.out.println(cop.name+cop.age);

    }
}

class ConstructorPerson{
    String name;
    int age;
    //1.构造器没有返回值，也不能写void
    //2.构造器的名称和类的ConstructorPerson一样
    //3.(String Pname,int Page) 是构造器形参列表，规则和成员方法一样
    public ConstructorPerson(String Pname,int Page){
        System.out.println("构造器被调用 完成对象属性的初始化");
        name = Pname;
        age = Page;
    }
}
```

构造器使用细节：

> 一个类可以定义多个不同的构造器，即构造器重载
>
> 构造器名和类名要相同
>
> 构造器没有返回值
>
> 构造器是完成对象的初始化，并不是创建对象
>
> 在创建对象时，系统自动调用该类的构造器
>
> 如果程序员没有定义构造器，系统会自动给类生成一个默认无参构造器(也叫默认构造器)
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220316213945931.png)
>
> 一旦定义了自己的构造器，默认的构造器就覆盖了，就不能再使用默认的无参构造器，除非显式的定义一下
>
> ```java
> public class Constructor {
>     public static void main(String[] args) {
> 
>         Dog d1 = new Dog();//这样就又是使用无参构造器
> 
>     }
> }
> 
> class Dog{
>     //如果程序员没有定义构造器，系统会自动给类生成一个默认无参构造器(也叫默认构造器)
>     /*
>     *   默认构造器
>     *   Dog(){
>     *
>     *   }
>     * 通过javap来反编译查看
>     * */
> 
>     //自己定义的构造器，会覆盖默认的无参构造器
>     public Dog(String str){
> 
>     }
> 
>     //再重新定义一下无参构造器就又可以使用无参构造器
>     Dog(){
> 
>     }
> 
> }
> ```

对象创建的流程分析：

1.先会在方法区中加载类的信息(类名.class)，只会加载一次

2.然后会在堆中分配内存空间(会得到一个地址)

3.完成对象初始化：

> 第一步：先默认初始化
>
> 第二步：显示初始化
>
> 第三步：构造器初始化

4.再把对象在堆中的地址返回给对象名，对象名也可以理解成对象的引用

[对象创建流程分析](https://www.bilibili.com/video/BV1fh411y7R8?p=245)

### 7.9 this关键字

java虚拟机会给每个对象分配this，代表当前对象。简单来说，那个对象调用，this就代表那个对象

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220319135848373.png)

[上图视频讲解地址](https://www.bilibili.com/video/BV1fh411y7R8?p=248&spm_id_from=pageDriver)

```java
public class This {
    public static void main(String[] args) {

        ThisDog td = new ThisDog("刘华强",38);
        System.out.println("td.hashCode="+td.hashCode());
        td.info();

    }
}

class ThisDog{
    String name;
    int age;

    //根据变量作用域的原则
    //这里构造器的name 是局部变量，而不是属性
    //这里构造器的age 是局部变量，而不是属性
    public ThisDog(String name,int age){
        //this.name就是当前对象的属性
        this.name = name;
        //this.age就是当前对象的属性
        this.age = age;
        //通过hashCode() 方法来查看暂时的内存地址
        System.out.println("this.hashCode="+this.hashCode());
    }

    public void info(){
        System.out.println(name+"\t"+age);
    }

}
```

this的注意事项：

> this关键字可以用来访问本类的属性、方法、构造器
>
> this用于区分当前类的属性和局部变量
>
> 访问成员方法的语法：this.方法名(参数列表);
>
> 访问构造器语法：this(参数列表);	注意只能在构造器中使用(即只能在构造器中访问另外一个构造器)	注意：如果有访问构造器语法：this(参数列表); 必须放在第一条语句
>
> this不能在类定义的外部使用，只能在类定义的方法中使用

```java
public class ThisDetal {
    public static void main(String[] args) {

        Thisdteal td = new Thisdteal();
        td.t2();
        td.t3();

    }
}

class Thisdteal{

    String name;
    int age;

    //访问构造器语法：this(参数列表);
    // 注意只能在构造器中使用(即只能在构造器中访问另外一个构造器)
    //注意：如果有访问构造器语法：this(参数列表); 必须放在第一条语句
    public Thisdteal(){
        //在这个构造器去访问另外一个构造器
        this("牛马",13);
        System.out.println("Thisdteal() 构造器");
    }

    public Thisdteal(String name,int age){
        this.name = name;
        this.age = age;
        System.out.println("Thisdteal(String name,int age)构造器");
    }

    public void t1(){
        System.out.println("这是t1方法");
    }

    public void t2(){
        System.out.println("这是t2方法");
        //调用本类的t1
        //第一种方法
        t1();
        //第二种方法
        this.t1();
    }

    //this访问属性
    public void t3(){
        String name = "憨批";
        //传统方式->是按变量作用域的就近原则来访问，如果有局部变量name和age那就不是输出属性name和age了
        //上面有局部变量name这里的name就不在是属性的name值，但是没有局部age，所以age的值还是属性
        System.out.println("name="+name+"age="+age);
        //使用this访问，就是访问类中的属性
        System.out.println("name="+this.name+"age="+this.age);
    }

}
```

## 8.面向对象编程(中级部分)

### IDE(集成开发环境)I-DEA

IDEA全称IntelliJ IDEA，在世界被公认为最好的开发工具

下载地址：[https://www.jetbrains.com/](https://www.jetbrains.com/)

Idea快捷键：

> 删除当前行：ctrl+y
>
> 复制当前行到下一行：ctrl+d
>
> 补全代码：alt+/
>
> 添加注释：ctrl+/
>
> 导入该行需要的类，先配置auto import ，然后使用alt+enter即可
>
> ![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220320151637354.png)
>
> 快速格式化代码：ctrl+alt+l
>
> 查看一个类的继承关系：Ctrl+h
>
> 将光标放在一个方法上，点击ctrl+b可以定位到方法
>
> 自动分配变量名，通过在后面加.var

### 8.1 包

包的作用：

1.区分相同名字的类

2.当类很多时，可以很好的管理类

3.控制访问范围

包的基本语法：

> package 包名;

package关键字，表示打包

**包实际上就是创建不同的文件夹/目录来保存类文件**

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220320154148062.png)

#### 8.1.1 包的命名

命名规则：只能包含数字、字母、下划线、小圆点.，但不能用数字开头，不能时关键字或保留字

命名规范：一般是小写字母+小圆点

java中常用的包：

> java.lang.*	lang包是基本包，默认引入，不需要再引入
>
> java.util.*	  uril包，系统提供的工具包，工具类，例如使用Scanner
>
> java.net.*	  网络包，用于网络开发
>
> java.awt.*	 是做java的界面开发，GUI

package的作用是声明当前来所在的包，需要放在类的最上面，一个类中最多只有一句package

impor指令，位置放在package的下面，再类定义前面，可以有多句且没有顺序要求

### 8.2 访问修饰符

java提供四种访问控制修饰符号，用于控制方法和属性(成员变量)的访问权限(范围)：

1.公开级别：用==**pubic**== 修饰，对外公开

2.受保护级别：用==**protected**==修饰，对子类和同一个包中的类公开

3.默认级别：没有修饰符号，向同一个包的类公开

4.私有级别：用==**private**==修饰，只有类本身可以访问，不对外公开

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220321142003023.png)

1）修饰符可以用来修饰类中的属性，成员方法以及类

2）只有默认的和public才能修饰类，并且遵循上述访问权限的特点

3）成员方法的访问规则和属性完全一样

### 8.3 封装

封装就是把抽象出的数据[属性]和对数据的操作[方法]封装在一起，数据被保户在内部，程序的其他部分只有通过被授权的操作[方法]，才能对数据进行操作

封装的好处：

> 1）隐藏实现细节：方法(连接数据库)<--调用(传入参数...)
>
> 2）可以对数据进行验证，保证安全合理

#### 8.3.1 封装的实现步骤

1)将属性进行私有化private【让外部不能直接修改属性】

2）提供一个公共的(public)set方法，用于对属性判断并赋值

> public void setXxx (类型 参数名){//Xxx 表示某个属性
>
> ​		//加入数据验证的业务逻辑
>
> ​		属性 = 参数名;
>
> }

3)提供一个公共的(public)get方法，用于获取属性的值

> pubic 数据类型 getXxx(){//权限判断，Xxx 某个属性
>
> ​		return xx;
>
> }

```java
import java.util.Scanner;

public class Encapsulation {
    public static void main(String[] args) {

        Person person = new Person();
        person.setName("牛马");
        person.setAge(23);
        person.setSalary(20000);
        System.out.println(person.getAge());
        System.out.println(person.getSalary());

        System.out.println(person.info());

    }
}

class Person{
    public String name;//name 公开的
    private int age;//age 私有化
    private double salary;//salary 私有化

    //快捷键：鼠标右键选择Generate，然后在选择Getter and Setter，在选择你要get和set的属性


    public String getName() {
        return name;
    }

    public void setName(String name) {
        if (name.length()>=2&&name.length()<=6){
            this.name = name;
        }else{
            System.out.println("名字字符数不对，正确范围(2-6)");
        }

    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        if (age>=1&&age<=120){
            this.age = age;
        }else{
            System.out.println("年龄范围1-120");
            this.age = 19;//给一个默认年龄
        }

    }

    public double getSalary() {
        Scanner scanner = new Scanner(System.in);
        System.out.println("输入密码来查看工资");
        int mi = scanner.nextInt();
        if (mi == 521666){
            System.out.println("密码正确，工资如下：");
            return salary;
        }else{
            System.out.println("密码错误，给你看鸭蛋");
            return 0;
        }

    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public String info(){
        return "信息为 name="+name+" age="+age+" salary="+salary;
    }

}
```

#### 8.3.2 封装与构造器

如果想要在构造器构造属性时，也生效你的防护，只需要把set方法写在构造器中就可以了

```java
public Person(String name, int age, double salary) {
    //将set方法写在构造器中，这样任然可以验证
    setName(name);
    setAge(age);
    setSalary(salary);
}
```

### 8.4 继承

继承可以解决代码复用，让我们的编程更加靠近人类思维，当多个类存在相同的属性(变量)和方法时，可以从这些类中抽象出父类，在父类中定义这些相同的属性和方法，所有的子类不需要重新定义这些属性和方法，只需要通过extends来声明继承父类即可

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220322144719298.png)

[视频讲解地址](https://www.bilibili.com/video/BV1fh411y7R8?p=287)

继承的基本语法：

> class 子类 extends  父类{
>
> }

1）子类就会自动拥有父类定义的属性和方法

2）父类又叫超类、基类

3）子类又叫派生类

```java
//父类
public class Student {
    //共有属性
    public String name;
    public int age;
    private double score;

    //共有方法
    public void setScore(double score) {
        this.score = score;
    }

    public void info() {
        System.out.println("小学生：" + name + " 年龄：" + age + " 分数：" + score);
    }
}
```

```java
//子类
//让Pupil继承Student类
public class Pupil extends Student {
    public void pinfo(){
        System.out.println("小学生"+name+"在考试");
    }
}
```

```java
//实际使用
public class TestExtends {
    public static void main(String[] args) {
        com.hwg.variable.chapter08.extends_.superclass.Graduate graduate = new Graduate();
        graduate.age = 23;
        graduate.name = "牛马";
        graduate.setScore(88);
        graduate.Ginfo();
        graduate.info();

        com.hwg.variable.chapter08.extends_.superclass.Pupil pupil = new Pupil();
        pupil.age = 10;
        pupil.name = "王强";
        pupil.setScore(89);
        pupil.pinfo();
        pupil.info();
    }
}
```

继续的细节问题：

1.子类继承了父类所有的属性和方法，非私有的方法和属性可以在子类直接访问，但是私有属性的方法不能在子类直接访问，要通过父类提供的公共的方法去访问		[视频详细讲解地址](https://www.bilibili.com/video/BV1fh411y7R8?p=289&spm_id_from=pageDriver)

2.子类必须调用父类的构造器，完成父类的初始化

3.当创建子类对象时，不管使用子类的那个构造器，默认情况下总会去调用父类的无参构造器，如果父类没有提供无参构造器，则必须在子类的构造器中用super去指定使用父类的那个构造器完成对父类的初始化工作，否则编译不会通过		(1、子类如果向初始化对象，就得先让父类初始化对象2、如果父类没有，或者只有 无参构造器，子类不管调用无参/有参构造器，都得先调用父类的无参构造器3、富国父类有一个有参构造器，并且把无参构造器覆盖，而子类想初始化对象，就得在构造器里面写super(父类的有参构造器)，来指定父类使用那个构造器来初始化)

4.如果希望指定的去调用父类的某个构造器，则显示的调用一下：super(参数列表)

5.super在使用的时候，只能在构造器中使用，而且必须放在构造器中的第一行

6.super()和this() 都只能放在构造器的第一行，因此这两个方法不能共存在一个构造器

7.java所有类都是Object类的子类，Object是所有类的父类

8.父类构造器的调用不限于直接父类，将一直往上追溯直到Object类(顶级父类)

9.子类最多只能继承一个父类(指直接继承)，即java中是单继承机制

10.不能滥用继承，子类和父类之间必须满足种属(is-a)的逻辑关系，也就是继承合理：比如猫类继承动物类

```java
//当前的第二级父类，顶级父类是Object
public class TopBase {
    public TopBase(){
        System.out.println("TopBase的无参构造器被调用");
    }
}
```

```java
//父类
public class Base extends TopBase {//Base是TopBase的子类
    //    四种属性
    public int n1 = 100;
    protected int n2 = 200;
    int n3 = 300;
    private int n4 = 400;

    public Base() {
        System.out.println("Base构造器被调用");
    }

    public Base(String name){
        System.out.println("Base的name构造器被调用");
    }

    public Base(String name,int age){
        System.out.println("Base的(String name,int age)构造器被调用");
    }

    //父类提供一个公共的方法让子类来访问私有的
    //将n4的值返回
    public int getN4(){
        return n4;
    }

    public void test1(){
        System.out.println("test1");
    }

    protected void test2(){
        System.out.println("test2");
    }

    void test3(){
        System.out.println("test3");
    }

    private void test4(){
        System.out.println("test4");
    }

    //Base父类提供的公共方法来访问test4方法
    public void callTest4(){
        test4();
    }

}
```

```java
//子类
public class Sub extends Base {//Sub是Base的子类
    public Sub(String name,int age){
        //调用父类的无参构造器
        super();//super的参数列表为空就是调用无参构造器
        //或者不写super 不写就是默认调用无参构造器
        System.out.println("Sub(String name,int age)构造器被调用");
    }

    public Sub() {
        //写与不写都可以
        //super(); //默认调用父类的无参构造器
        //如果父类没有提供无参构造器，则必须在子类的构造器中用super去指定使用父类的那个构造器完成对父类的初始化工作
        super("n");
        System.out.println("Sub构造器被调用");
    }

    public Sub(String name) {
        super("n",23);
        System.out.println("Sub的name构造器被调用");
    }

    public void sayOk() {
        //非私有的方法和属性可以在子类直接访问
        //但是私有属性的方法不能在子类直接访问
        System.out.print(n1 + " " + n2 + " " + n3);
        System.out.println();//换行
        test1();
        test2();
        test3();
        //test4(); 错误不能直接访问私有

        //通过父类提供的公共的方法去访问
        System.out.println("n4=" + getN4());
        callTest4();

    }
}
```

```java
//主方法，运行测试看结果
public class ExtendsDetail {
    public static void main(String[] args) {
        //子要是类都需要通过构造器初始化，子类构造器一般只管自己的属性初始化，那么在内存当中，父类那一块的属性并没有初始化，因此子类在对自己进行构造前，会先调用父类的构造器把父类那一块的内存初始化
        Sub sub = new Sub();
        sub.sayOk();
        //当创建子类对象时，不管使用子类的那个构造器，默认情况下总会去调用父类的无参构造器
        Sub sub1 = new Sub("牛马");
        Sub sub2 = new Sub("ma",23);
    }
}
```

 继承的内存布局：  [视频讲解地址](https://www.bilibili.com/video/BV1fh411y7R8?p=294&spm_id_from=pageDriver)

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220323160545103.png)

```java
public class ExtendsTheory {
    public static void main(String[] args) {
        Son son = new Son();
        //1.先看子类是否有该属性
        //2.如果子类有这个属性，并且可以访问，则返回信息
        //3.如果子类没有这个属性，就看父类有没有这个属性(如果父类有该属性，并且可以访问，就返回信息)
        //4.如果父类没有就按照 3的规则，继承找上级父类，直到Object
        System.out.println(son.name);
        System.out.println(son.getAge());
        System.out.println(son.hobby);
    }
}

class GrandPa {
    String name = "中头爷爷";
    String hobby = "打麻将";
}

class Father extends GrandPa {
    String name = "小头爸爸";
    private int age = 45;

    public int getAge() {
        return age;
    }
}

class Son extends Father {
    String name = "大头儿子";
}
```

#### 8.4.1 super关键字

super代表父类的引用，用于访问父类的属性、方法、构造器

```java
//父类
public class A {
    public int n1 = 100;
    protected int n2 = 200;
    int n3 = 300;
    private int n4 = 400;

    public void test1(){

    }
    protected void test2(){

    }
    void test3(){

    }
    private void test4(){

    }
}
```

```java
//子类
public class B extends A{
    //访问父类的构造器：super(参数列表);  只能放在构造器的第一句话，只能出现一句
    public B(){
        super();
    }

    //访问父类的属性，但不能访问父类的private属性
    public void hi(){
        System.out.println(super.n1+" "+super.n2+" "+super.n3);
//        System.out.println(super.n4); //不能访问私有的属性
    }

    //访问父类的方法，但不能访问父类的private方法
    public void ok(){
        super.test1();
        super.test2();
        super.test3();
        //super.test4();  //不能访问私有的方法
    }
}
```

1.访问父类的属性，但不能访问父类的private属性：super.属性名;

2.访问父类的方法，但不能访问父类的private方法：super.方法名(参数列表);

3.访问父类的构造器：super(参数列表);  只能放在构造器的第一句话，只能出现一句

**super带来的便利/细节**

1）调用父类的构造器的好处（分工明确，父类属性由父类初始化，子类的属性由子类初始化）

2） 当子类中有和父类中的成员（属性和方法）重名时，为了访问父类的成员，必须通过super。如果没有重名，使用super、this、直接访问是一样的效果

```java
//父类
public class A {
    public void cal(){
        System.out.println("a类的cal方法");
    }
}
```

```java
//子类
public class B extends A{
    public int n1 = 888;
    
    public void cal(){
        System.out.println("B类的cal方法");
    }

    public void sum(){
        System.out.println("b类的sum方法");
        //调用父类-A的cla方法
        //因为子类-B没有cal方法，因此可以使用三种方法来调用

        //1.找cal方法时，顺序是：先找本类，如果有，则调用
        //2.如果没有，则找父类(如果有，并可以调用，则调用)
        //3.如果父类没有就继续找父类的父类，整个规则，就是一样的，直到Object类
        //如果在查找过程中，找到了，但是不能访问，则报错。如果没有找到，则提示方法不存在
        cal();

        this.cal();//等价cal()

        //找cal super.cal()方法的顺序是直接查找父类，其他的规则一样
        super.cal();
        
        //访问属性的规则
        //n1和this.n1查找的规则是：
        //1.先找本类，如果有，则调用
        //2.如果没有，则找父类(如果有，并可以调用，则调用)
        //3.如果父类没有就继续找父类的父类，整个规则，就是一样的，直到Object类
        //如果在查找过程中，找到了，但是不能访问，则报错。如果没有找到，则提示方法不存在
        System.out.println(n1);
        System.out.println(this.n1);
        
        //找cal super.n1 的顺序是直接查找父类，其他的规则一样
        System.out.println(super.n1);
    }

}
```

```java
//主方法，运行看结果
public class Super {
    public static void main(String[] args) {
        B b = new B();
        b.sum();
    }
}
```

3）super的访问不限于直接父类，如果爷爷类和本类中有同名的成员，也可以使用super去访问爷爷的类的成员；如果多个父类(上级类)中都有同名的成员，使用super访问遵循就进原则  A->B->C   当然也要遵守访问权限的相关规则

**super和this的区别**

|      | 区别点     | this                                                   | super                                    |
| ---- | :--------- | :----------------------------------------------------- | :--------------------------------------- |
| 1    | 访问属性   | 访问本类中的属性，如果本类没有此属性则从父类中继续查找 | 从父类开始查找属性                       |
| 2    | 调用方法   | 访问本类中的方法，如果本类没有此方法则从父类中继续查找 | 直接从父类开始查找方法                   |
| 3    | 调用构造器 | 调用本类构造器，必须放在构造器的首行                   | 调用父类构造器，必须放在子类构造器的首行 |
| 4    | 特殊       | 表示当前对象                                           | 子类中访问父类对象                       |

### 8.5 方法重写/覆盖

方法覆盖(重写)就是子类有一个方法，和父类的某个方法的名称、返回类型、参数一样，那么我们就说子类的这个方法覆盖了父类的方法

```java
public class Override {
    public static void main(String[] args) {
        Dog dog = new Dog();
        dog.cry();
    }
}

class Animal{
    public void cry(){
        System.out.println("你在狗叫什么");
    }
}

class Dog extends Animal{
    //1.因为Dog是Animal子类
    //2.Dog的cry方法和Animal的cry定义形式一样(名称、返回类型、参数)
    //3.这时就发生了方法的重写
    public void cry(){
        System.out.println("你就是在狗叫");
    }
}
```

**方法重写的注意事项**

1.子类方法的参数，方法名称，要和父类方法的参数，方法名称完全一样

2.子类方法的返回类型和父类方法返回类型一样，或者是父类返回类型的子类

比如：父类的返回类型是Object，子类方法返回类型是String，String是Object的子类，所以一样满足方法的重写

3.子类方法不能缩小父类方法的访问权限   public > protected > 默认 > private

| 名称           | 发生范围 | 方法名   | 参数列表                         | 返回类型                                                     | 修饰符                             |
| -------------- | -------- | -------- | -------------------------------- | ------------------------------------------------------------ | ---------------------------------- |
| 重载(overload) | 本类     | 必须一样 | 类型、个数或者顺序至少有一个不同 | 无要求                                                       | 无要求                             |
| 重写(override) | 父子类   | 必须一样 | 相同                             | 子类重写的方法、返回的类型和父类返回的类型一致，或者是其子类 | 子类方法不能缩小父类方法的访问范围 |

### 8.6 多态

方法或对象具有多种形态，是面向对象的第三大特征，多态是建立在封装和继承继承之上的

#### 8.6.1 方法的多态

重写和重载就体现了多态

```java
public class PloyMethod {
    public static void main(String[] args) {
        A a = new A();
        B b = new B();
        //方法重载体现多态
        System.out.println(b.sum(21,4));
        System.out.println(b.sum(23,45,7));

        //方法重写体现多态
        a.say();
        b.say();
    }
}

class A{
    public void say(){
        System.out.println("a的say方法");
    }
}

class B extends A{
    public int sum(int i1,int i2){
        return i1+i2;
    }
    public int sum(int i1,int i2, int i3){
        return i1+i2+i3;
    }

    public void say(){
        System.out.println("b类的say方法");
    }
}
```

#### 8.6.2 对象的多态

1.一个对象的编译类型和运行类型可以不一致

2.编译类型在定义对象时，就确定了，不能改变

3.运行类型是可以变化的

4.编译类型看定义时 = 号的左边，运行类型看 = 号的右边

```java
//父类
public class Animal {
    public void cay(){
        System.out.println("Animal cay()");
    }
}
```

```java
//子类
public class Cat extends Animal{
    public void cay(){
        System.out.println("Cat cay()");
    }
}
```

```java
//子类
public class Dog extends Animal{
    public void cay(){
        System.out.println("Dog cay");
    }
}
```

```java
//主方法
public class PolyObject {
    public static void main(String[] args) {
        //对象的多态特点

        //animal 的编译类型时Animal 运行类型是Dog
        Animal animal = new Dog();
        animal.cay();//当程序运行到这里时，因为运行类型是Dog，所以这里的cay就是Dog里面的cay

        //这时，animal的运行类型变成了Cat，但是编译类型还是Animal
        animal = new Cat();
        animal.cay();//当程序运行到这里时，因为运行类型是Cat，所以这里的cay就是Cay里面的cay
    }
}
```

#### 8.6.3 多态的注意事项和细节

多态的前提是：两个对象或类存在继承关系

多态的向上转型：

1）本质：父类的引用指向了子类的对象

2）语法：父类类型 引用名 = new 子类类型();

3）特点：编译类型看左边，运行内存看右边。可以调用父类中的所有成员(需要遵顼访问权限)，不能直接调用子类中的特有成员，最终运行效果看子类(运行类型)的具体实现，即调用方法时，按照从子类(运行类型)开始查找方法 ，然后调用，规则和前面讲的方法调用规则一致

#### 8.6.4 多态的向下转型：

1）语法：子类类型 引用名 = (子类类型) 父类引用;

2）只能强转父类的引用，不能强转父类的对象

3）要求父类的引用必须指向的是当前目标类型的对象

4）当向下转型后，可以调用子类类型中所有的成员

```java
public class PolyDetail {
    public static void main(String[] args) {

        //向上转型：父类的引用指向了子类的对象
        //语法：父类类型引用名 = new 子类类型();
        Animal animal = new Cat();
        Object object = new Cat();//也是可以的 Object也是cat的父类

        //可以调用父类中的所有成员(需要遵顼访问权限)，不能直接调用子类中的特有成员
        animal.run();
        //因为在编译阶段，能调用那些成员，是由编译类型来决定的
        //animal.catchMouse();//错误

        //最终运行效果看子类(运行类型)的具体实现，即调用方法时，按照从子类(运行类型)开始查找方法 ，然后调用，规则和前面讲的方法调用规则一致
        animal.eat();
        animal.show();
        animal.sleep();

        //多态的向下转型
        //语法：子类类型 引用名 = (子类类型) 父类引用;
        Cat cat = (Cat) animal;
        //要求父类的引用必须指向的是当前目标类型的对象
        //Dog dog = (Dog) animal;//运行就会报错，类的转换错误

        cat.catchMouse();

    }
}

public class Animal {

    String name ="动物";
    int age = 10;
    public void sleep(){
        System.out.println("睡觉");
    }
    public void run(){
        System.out.println("跑");
    }
    public void eat(){
        System.out.println("吃");
    }
    public void show(){
        System.out.println("你好");
    }

}

public class Cat extends Animal{
    public void eat(){
        System.out.println("猫吃鱼");
    }
    public void catchMouse(){
        System.out.println("猫抓老鼠");
    }
}

public class Dog extends Animal{
}
```

属性没有重写之说，属性的指看编译类型

```java
public class PolyDetail01 {
    public static void main(String[] args) {

        //属性没有重写之说，属性的指看编译类型
        Base base = new Sub();
        System.out.println(base.count);
    }
}

//
class Base{
    int count = 13;
}

class Sub extends Base{
    int count = 23;
}
```

instanceOf 比较操作符，用于判断对象的运行类型是否为xx类型或xx类型的子类型

```java
public class PolyDetail02 {
    public static void main(String[] args) {
        //判断对象的运行类型是否为xx类型或xx类型的子类型
        BB bb = new BB();
        System.out.println(bb instanceof BB);//true
        System.out.println(bb instanceof AA);//true bb是AA的子类型

        AA aa = new BB();//向上转型
        System.out.println(aa instanceof AA);//true aa的运行类型是BB，BB是AA的子类
        System.out.println(aa instanceof BB);//true

        Object obj = new Object();
        System.out.println(obj instanceof AA);//false
        String str = "hello";
        System.out.println(str instanceof Object);//true

    }
}

class AA{}
class BB extends AA{}
```

##### java的动态绑定机制

当调用对象方法的时候，该方法会和该对象的内存地址/运行类型绑定

当调用对象属性时，没有动态绑定机制，哪里声明哪里使用

```java
public class DynamicBinding {
    public static void main(String[] args) {
        A a = new B();// 向上转型
        // 运行类型是B，所以a.sum开始从B类中开始查找
        //将B类中的sum注销后，查找父类的sum
        System.out.println(a.sum());//40->30
        System.out.println(a.sum1());//30->20
    }
}

class A {
    public int i = 10;

    //动态绑定机制：
    //当调用对象方法的时候，该方法会和该对象的内存地址/运行类型绑定
    //当调用对象属性时，没有动态绑定机制，哪里声明哪里使用

    public int sum() {
        //a的运行类型是B，所以这里调用了子类B的getI
        return getI() + 10;
    }

    public int sum1() {
        return i + 10;
    }

    public int getI() {
        return i;
    }
}

class B extends A {
    public int i = 20;

//    public int sum() {
//        return i + 20;
//    }

    public int getI() {
        return i;
    }

//    public int sum1() {
//        return i + 10;
//    }
}
```

#### 8.6.4 多态的应用

1）多态数组：

数组的定义类型为父类类型，里面保存的实际元素类型为子类类型

```java
public class PloyArrar {
    public static void main(String[] args) {
        //多态数组，接收类型是父类
        Person[] persons = new Person[5];
        persons[0] = new Person("牛马",23);
        persons[1] = new Student("牛马1",18,98);
        persons[2] = new Student("牛马2",19, 50);
        persons[3] = new Teacher("牛马3",30,4000);
        persons[4] = new Teacher("牛马4",50,8000);

        //循环遍历查看结果
        for (int i = 0; i < persons.length; i++) {
            //编译类型是Person，运行类型是根据实际情况来动态绑定
            System.out.println(persons[i].say());
            if (persons[i] instanceof Student){
                Student student = (Student)persons[i];
                student.study();
                //或者一条语句解决
//                ((Student)persons[i]).study();
            }else if (persons[i] instanceof Teacher){
                ((Teacher)persons[i]).teach();
            }

        }

    }
}

class Person {//父类
    private String name;
    private int age;

    public Person(String name, int age) {
        this.name = name;
        this.age = age;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public String say(){
        return name+"\t"+age;
    }
}

class Student extends Person{
    private double score;

    public Student(String name, int age, double score) {
        super(name, age);
        this.score = score;
    }

    public double getScore() {
        return score;
    }

    public void setScore(double score) {
        this.score = score;
    }

    //重写say方法
    public String say() {
        return super.say()+"\t"+score;
    }

    public void study(){
        System.out.println("学生 "+getName()+"正在上课");
    }
}

class Teacher extends Person{
    private double salary;

    public Teacher(String name, int age, double salary) {
        super(name, age);
        this.salary = salary;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    public String say(){
        return super.say()+"\t"+salary;
    }

    public void teach(){
        System.out.println("老师 "+getName()+"在教课");
    }
}
```

2）参数多态

方法定义的形参类型为父类类型，实参类型允许为子类类型

```java
public class PloyParameter {
    public static void main(String[] args) {
        Worker worker = new Worker("小李", 3800);
        Manager manager = new Manager("王经理", 15000, 200000);
        PloyParameter parameter = new PloyParameter();
        parameter.showEmpAnnual(worker);
        parameter.showEmpAnnual(manager);
        parameter.testWork(worker);
        parameter.testWork(manager);
    }

    public void showEmpAnnual(Employee e){
        System.out.println(e.getAnnual());//动态绑定机制
    }

    public void testWork(Employee e){
        if (e instanceof Worker){
            ((Worker) e).work();//向下转型
        }else if (e instanceof Manager){
            ((Manager) e).manage();
        }
    }
}

class Employee {
    private String name;
    private double salary;

    public Employee(String name, double salary) {
        this.name = name;
        this.salary = salary;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public double getSalary() {
        return salary;
    }

    public void setSalary(double salary) {
        this.salary = salary;
    }

    //得到年工资
    public double getAnnual(){
        return 12*salary;
    }

}

class Worker extends Employee{
    public Worker(String name, double salary) {
        super(name, salary);
    }

    public void work(){
        System.out.println("工人 "+getName()+"在上班");
    }

    @Override
    public double getAnnual() {
        return super.getAnnual();
    }
}

class Manager extends Employee{
    private double bonus;

    public Manager(String name, double salary, double bonus) {
        super(name, salary);
        this.bonus = bonus;
    }

    public double getBonus() {
        return bonus;
    }

    public void setBonus(double bonus) {
        this.bonus = bonus;
    }

    public void manage(){
        System.out.println("经理 "+getName()+"在管理员工");
    }

    @Override
    public double getAnnual() {
        return super.getAnnual()+bonus;
    }
}
```

### 8.7 Object类详解

#### 8.7.1 equals方法

equals和==的区别

==是一个比较运算符

1.==：既可以判断基本类型，也可以判断引用类型

2.==：如果判断基本类型，判断的是值是否相等

3.==：如果判断引用类型，判断的是地址是否相等，即判断是不是同一个对象

```java
public class Equals01 {
    public static void main(String[] args) {
        int num =10;
        double num1 = 10;
        System.out.println(num == num1);
        B b = new B();
        B c = b;
        B d = c;
        System.out.println(d == b);
        System.out.println(c == d);
        A a = b;
        System.out.println(a==d);
    }
}
class A{}
class B extends A{}
```

4.equals：是Object类中的方法，只能判断引用类型

5.默认判断的是地址是否相等，子类中往往重写该方法，用于判断内容是否相等

| 名称   | 概念                                   | 用于基本类型         | 用于引用类型                                                 |
| ------ | -------------------------------------- | -------------------- | ------------------------------------------------------------ |
| ==     | 比较运算符                             | 可以，判断值是否相等 | 可以，判断两个对象(地址)是否相等                             |
| equals | Object类的方法，java类都可以使用equals | 不可以               | 可以，默认是判断两个对象是否相等，但是子类往往重写该方法，用于比较对象的属性是否相等，比如(String , Integer) |



##### 8.7.1.1 自己重写equals方法

```java
public class Equals {
    public static void main(String[] args) {
        Person person = new Person("nm", 18, '男');
        Person person1 = new Person("nm", 18, '男');
        Equals equals = new Equals();
        //这里是调用Object中的equals方法，他是判断是否是同一个对象，重写前是false，重写后是ture
        System.out.println(person.equals(person1));//true
        System.out.println(equals.equals(person, person1));

    }

    //自己的重写equals
    public boolean equals(Person person, Person person1) {
        if (person.getAge() == person1.getAge()) {//判断age是否相等
            if (person.getGender() == person1.getGender()) {//判断gender是否相等
                if ((person.getName()).length() == (person1.getName()).length()) {//判断字符串的长度是否相等
                    int n = (person.getName()).length();
                    while (n-- != 0) {//循环判断字符串中每个字符是否相等
                        char c = ((person.getName()).charAt(n));
                        char c1 = ((person1.getName()).charAt(n));
                        if (c != c1) {//有一个字符不相等就返回false
                            return false;
                        }
                    }
                    return true;//当以上条件都成立的时候，就返回真
                }
            }
        }
        return false;//以上条件有一个没有成立就返回false
    }
}

class Person {
    private String name;
    private int age;
    private char gender;

    public Person(String name, int age, char gender) {
        this.name = name;
        this.age = age;
        this.gender = gender;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }

    public void setAge(int age) {
        this.age = age;
    }

    public char getGender() {
        return gender;
    }

    public void setGender(char gender) {
        this.gender = gender;
    }

    //老师的重写
    public boolean equals(Object obj) {
        if (this == obj) {//判断比较的两个对象是否是同一个对象，是就直接返回true
            return true;
        }
        //是Person类型才判断
        if (obj instanceof Person) {
            //向下转型，得到各个属性
            Person p = (Person) obj;
            return this.name.equals(p.name) && this.age == p.age && this.gender == p.gender;
        }
        return false;
    }
}
```

#### 8.7.2 hashCode方法

1）提高具有哈希结构的容器的效率

2）两个引用，如果指向的是同一个对象，则哈希值肯定是一样的

3）俩个引用，如果指向的不同的对象，则哈希值是不一样的

4）哈希值主要根据地址号来的，不能完全将哈希值等价于地址

#### 8.7.3 toString方法

默认返回：全类名+@+哈希值的十六进制

子类往往重写toString方法，用于返回对象的属性信息

重写toString方法，打印对象或拼接对象时，都会自动调用该对象的toString形式

当直接输出一个对象时，toString方法会被默认调用

```java
public class ToString {
    public static void main(String[] args) {
        /*
        Object的toString()源码
        1.getClass().getName() 类的全类名(包名+类名)
        2.Integer.toHexString(hashCode()) 将对象的hashCode值转成16进制字符串
        public String toString() {
            return getClass().getName() + "@" + Integer.toHexString(hashCode());
        }
         */

        monster monster = new monster("牛马", "溜达");
        System.out.println(monster.toString());
        //当直接输出一个对象时，toString方法会被默认调用
        System.out.println(monster);//等价monster.toString()
    }
}


class monster{
    private String name;
    private String job;

    public monster(String name, String job) {
        this.name = name;
        this.job = job;
    }

    //重写toString方法
    @Override
    public String toString() {//重写后，一般吧对象的属性值输出，当然也可以自定义
        return "monster{" +
                "name='" + name + '\'' +
                ", job='" + job + '\'' +
                '}';
    }
}
```

#### 8.7.4 finalize方法

1.当对象被回收时，系统自动调用该对象的finalize方法，子类可以重写该方法，做一些释放资源

2.什么时候被回收：当某个对象没有任何引用时，则jvm就认为这个对象是一个垃圾对象，就会使用垃圾回收机制来销毁该对象，在销毁该对象前，会先调用finalize方法

3.垃圾回收机制的调用，是由系统来决定(即有自己的GC算法)，也可以通过System.gc() 主动触发垃圾回收机制

在实际开发中，几乎不会运用finalize方法，所以更多就是为了应付面试

```java
public class Finalize {
    public static void main(String[] args) {
        Car car = new Car("奔驰");
        car = null;
        /*
        这时，car对象就是一个垃圾，垃圾回收器就会回收(销毁)对象，在销毁对象前，会调用该对象的finalize方法
        可以在finalize中，写自己的业务逻辑代码(比如释放资源：数据库连接等)
        如果不重写finalize，那么就会调用Object类的finalize，即默认处理
        如果重写了finalize，就可以实现自己的逻辑
         */
        System.gc();//主动调用垃圾回收器
    }
}

class Car{
    private String name;

    public Car(String name){
        this.name = name;
    }

    //重写finalize
    @Override
    protected void finalize() throws Throwable {
        System.out.println("我们销毁了"+name);
    }
}
```

### 8.8 断点调试(debug)

**在断点调试过程中，是运行状态，是以对象的运行类型来执行的**

1.断点调试是指在程序的某一行设置一个断点，调试时，程序运行到这一行就会停住，然后你可以一步一步往下调试，调试过程中可以看各个变量当前的值，出错的话，调试到出错的代码行即显示错误，停下，进行分析从而找到这个bug

2.断点调试是程序员必须掌握的技能

3.断点调试也能帮助我们查看java底层源代码的执行过程，提高我们的java水平

**断点调试的快捷键**

F7(跳入)：跳入方法内

F8(跳过)：逐行执行代码

shift+F8(跳出)：跳出方法

F9(resume，执行到下一个断点)

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220401093951598.png)

[断点调试视频讲解](https://www.bilibili.com/video/BV1fh411y7R8?p=328)(看328到334集)

### 8.9 现有知识编写的小项目（零钱通）

功能：记账

缺点：现有知识做不到数据保存，所以该项目为一次性用品

```java
import java.text.SimpleDateFormat;
import java.util.Scanner;
import java.util.Date;

public class SmallChangeSys {
    public static void main(String[] args) {

        /*
        完成零钱通系统
        1.先完善基本的显示菜单和选择功能
        2.完善零钱通明细功能
         */

        //接收用户输入
        Scanner scanner = new Scanner(System.in);
        Add add = new Add();
        String[][] str = new String[0][4];
        //循环条件变量
        boolean loop = true;
        //使用do-while循环结构 让菜单起码显示一次
        do {
            //菜单界面
            System.out.println("\n--------------零钱通菜单--------------");
            System.out.println("\t\t\t1 零钱通明细");
            System.out.println("\t\t\t2 收益入账");
            System.out.println("\t\t\t3 消费");
            System.out.println("\t\t\t4 退     出");
            System.out.print("请选择(1-4)：");
            int sum = scanner.nextInt();
            int num = 0;
            //使用switch分支语句
            switch (sum) {
                case 1:
                    //输出零钱明细
                    System.out.println("--------------零钱通明细--------------");
                    for (int i = 0; i < str.length; i++) {
                        for (int j = 0; j < str[i].length; j++) {
                            System.out.print(str[i][j] + "\t");
                        }
                        System.out.println();
                    }
                    break;
                case 2:
                    //调用收入方法
                    str = add.income(str);
                    break;
                case 3:
                    //调用消费方法
                    str = add.spending(str);
                    break;
                case 4:
                    System.out.println("你真的打算退出了吗(y/n)");
                    String s = scanner.next();
                    if (s.equals("y")) {
                        System.out.println("你退出了零钱通系统");
                        loop = false;
                    } else {
                        System.out.println("继续使用系统");
                    }
                    break;
                default:
                    System.out.println("你选择的菜单有误");
            }

        } while (loop);
    }
}


class Add {
    //余额
    double num = 0;

    //数组的添加
    public String[][] getArr(String[][] arr, String src, String scr) {
        //记录原数组的长度
        int sum = arr.length;
        Scanner scanner = new Scanner(System.in);
        //新数组的长度是原数组的长度加一
        String[][] str = new String[sum + 1][4];
        //拷贝原数组的元素
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr[i].length; j++) {
                str[i][j] = arr[i][j];
            }
        }
        //接收输入的金额
        double bu = 0;
        //记录是支出还是收入
        str[str.length - 1][0] = scr;
        //对其他位置进行对应值的写入
        for (int i = 0; i < str[str.length - 1].length; i++) {
            switch (i) {
                //记录收入或支出的金额
                case 1:
                    boolean k = true;
                    do {
                        if (src.equals("+")) {
                            System.out.println("输入你这单的收入金额");
                            bu = scanner.nextDouble();
                            if (bu > 0) {
                                str[str.length - 1][i] = src + bu;
                                k = false;
                            } else {
                                System.out.println("你输入的金额有误重新输入，收入金额大于0");

                            }
                        } else if (src.equals("-")) {
                            System.out.println("输入你这单的支出金额");
                            bu = scanner.nextDouble();
                            if (bu <= 0 || bu > this.num) {
                                System.out.println("消费金额不能为0，也不能大于余额，你当前的余额为："+this.num);
                            } else {
                                str[str.length - 1][i] = src + bu;
                                k = false;
                            }
                        }
                    } while (k);
                    break;
                //记录日期
                case 2:
                    Date date = null;//表示日期
                    SimpleDateFormat sdf = new SimpleDateFormat("yyyy-MM-dd HH:mm");//用于日期格式化 yyyy=年 MM=月 dd=日 HH=时 mm=分
                    date = new Date();//
                    str[str.length - 1][i] = sdf.format(date);
                    break;
                //记录收入或支出后账号的余额
                case 3:
                    if (src.equals("+")) {
                        this.num += bu;
                    } else if (src.equals("-")) {
                        this.num -= bu;
                    }
                    str[str.length - 1][i] = "余额:" + this.num;
                    break;
            }
        }
        //让原数组指向新数组
        arr = str;
        //返回结果
        return arr;
    }

    //零钱收入
    public String[][] income(String[][] arr) {
        boolean b = true;
        do {
            //调用方法记账
            arr = getArr(arr, "+", "收益入账");
            Scanner scanner = new Scanner(System.in);
            //判断是否要再次记账
            System.out.print("你还有要继续添加的收入吗(y/n):");
            char car = scanner.next().charAt(0);
            if (car == 'y') {
            } else {
                b = false;
            }
        } while (b);
        return arr;
    }

    //零钱支出
    public String[][] spending(String[][] arr) {
        boolean b = true;
        do {
            Scanner scanner = new Scanner(System.in);
            System.out.println("请输入你这笔钱的用途");
            String scr = scanner.next();
            arr = getArr(arr, "-", scr);
            System.out.print("你还有要继续添加的收入吗(y/n):");
            char car = scanner.next().charAt(0);
            if (car == 'y') {
            } else {
                b = false;
            }
        } while (b);
        return arr;
    }
}
```

## 9. 综合小项目--房屋出租系统

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220408095946751.png)

### 工具类

```java
package com.hwg.variable.project.HouseToRent.utils;

/**
 工具类的作用:
 处理各种情况的用户输入，并且能够按照程序员的需求，得到用户的控制台输入。
 */

import java.util.*;
/**


 */
public class Utility {
    //静态属性。。。
    private static Scanner scanner = new Scanner(System.in);


    /**
     * 功能：读取键盘输入的一个菜单选项，值：1——5的范围
     * @return 1——5
     */
    public static char readMenuSelection() {
        char c;
        for (; ; ) {
            String str = readKeyBoard(1, false);//包含一个字符的字符串
            c = str.charAt(0);//将字符串转换成字符char类型
            if (c != '1' && c != '2' &&
                    c != '3' && c != '4' && c != '5') {
                System.out.print("选择错误，请重新输入：");
            } else break;
        }
        return c;
    }

    /**
     * 功能：读取键盘输入的一个字符
     * @return 一个字符
     */
    public static char readChar() {
        String str = readKeyBoard(1, false);//就是一个字符
        return str.charAt(0);
    }
    /**
     * 功能：读取键盘输入的一个字符，如果直接按回车，则返回指定的默认值；否则返回输入的那个字符
     * @param defaultValue 指定的默认值
     * @return 默认值或输入的字符
     */

    public static char readChar(char defaultValue) {
        String str = readKeyBoard(1, true);//要么是空字符串，要么是一个字符
        return (str.length() == 0) ? defaultValue : str.charAt(0);
    }

    /**
     * 功能：读取键盘输入的整型，长度小于2位
     * @return 整数
     */
    public static int readInt() {
        int n;
        for (; ; ) {
            String str = readKeyBoard(10, false);//一个整数，长度<=10位
            try {
                n = Integer.parseInt(str);//将字符串转换成整数
                break;
            } catch (NumberFormatException e) {
                System.out.print("数字输入错误，请重新输入：");
            }
        }
        return n;
    }
    /**
     * 功能：读取键盘输入的 整数或默认值，如果直接回车，则返回默认值，否则返回输入的整数
     * @param defaultValue 指定的默认值
     * @return 整数或默认值
     */
    public static int readInt(int defaultValue) {
        int n;
        for (; ; ) {
            String str = readKeyBoard(10, true);
            if (str.equals("")) {
                return defaultValue;
            }

            //异常处理...
            try {
                n = Integer.parseInt(str);
                break;
            } catch (NumberFormatException e) {
                System.out.print("数字输入错误，请重新输入：");
            }
        }
        return n;
    }

    /**
     * 功能：读取键盘输入的指定长度的字符串
     * @param limit 限制的长度
     * @return 指定长度的字符串
     */

    public static String readString(int limit) {
        return readKeyBoard(limit, false);
    }

    /**
     * 功能：读取键盘输入的指定长度的字符串或默认值，如果直接回车，返回默认值，否则返回字符串
     * @param limit 限制的长度
     * @param defaultValue 指定的默认值
     * @return 指定长度的字符串
     */

    public static String readString(int limit, String defaultValue) {
        String str = readKeyBoard(limit, true);
        return str.equals("")? defaultValue : str;
    }


    /**
     * 功能：读取键盘输入的确认选项，Y或N
     * 将小的功能，封装到一个方法中.
     * @return Y或N
     */
    public static char readConfirmSelection() {
        System.out.println("请输入你的选择(Y/N): 请小心选择");
        char c;
        for (; ; ) {//无限循环
            //在这里，将接受到字符，转成了大写字母
            //y => Y n=>N
            String str = readKeyBoard(1, false).toUpperCase();
            c = str.charAt(0);
            if (c == 'Y' || c == 'N') {
                break;
            } else {
                System.out.print("选择错误，请重新输入：");
            }
        }
        return c;
    }

    /**
     * 功能： 读取一个字符串
     * @param limit 读取的长度
     * @param blankReturn 如果为true ,表示 可以读空字符串。
     *                   如果为false表示 不能读空字符串。
     *
     * 如果输入为空，或者输入大于limit的长度，就会提示重新输入。
     * @return
     */
    private static String readKeyBoard(int limit, boolean blankReturn) {

        //定义了字符串
        String line = "";

        //scanner.hasNextLine() 判断有没有下一行
        while (scanner.hasNextLine()) {
            line = scanner.nextLine();//读取这一行

            //如果line.length=0, 即用户没有输入任何内容，直接回车
            if (line.length() == 0) {
                if (blankReturn) return line;//如果blankReturn=true,可以返回空串
                else continue; //如果blankReturn=false,不接受空串，必须输入内容
            }

            //如果用户输入的内容大于了 limit，就提示重写输入
            //如果用户如的内容 >0 <= limit ,我就接受
            if (line.length() < 1 || line.length() > limit) {
                System.out.print("输入长度（不能大于" + limit + "）错误，请重新输入：");
                continue;
            }
            break;
        }

        return line;
    }
}
```

### 数据层

```java
package com.hwg.variable.project.HouseToRent.domain;

/**
 * House的对象表示一个房屋信息
 */
public class House {
    //编号 房主 电话 地址 月租 状态(未出租/已出租)
    private int id;
    private String name;
    private String phone;
    private String address;
    private int rent;
    private String state;

    //构造器
    public House(int id, String name, String phone, String address, int rent, String state) {
        this.id = id;
        this.name = name;
        this.phone = phone;
        this.address = address;
        this.rent = rent;
        this.state = state;
    }

    //方法
    public int getId() {
        return id;
    }

    public void setId(int id) {
        this.id = id;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getPhone() {
        return phone;
    }

    public void setPhone(String phone) {
        this.phone = phone;
    }

    public String getAddress() {
        return address;
    }

    public void setAddress(String address) {
        this.address = address;
    }

    public int getRent() {
        return rent;
    }

    public void setRent(int rent) {
        this.rent = rent;
    }

    public String getState() {
        return state;
    }

    public void setState(String state) {
        this.state = state;
    }

    //为了方便输出对象信息，重写一下toString
    @Override
    public String toString() {
        return  id +
                "\t\t" + name +
                "\t" + phone +
                "\t" + address +
                "\t" + rent +
                "\t" + state ;
    }
}
```

### 界面层

```java
package com.hwg.variable.project.HouseToRent.view;

import com.hwg.variable.project.HouseToRent.domain.House;
import com.hwg.variable.project.HouseToRent.service.HouseService;
import com.hwg.variable.project.HouseToRent.utils.Utility;

/**
 * 1.显示界面
 * 2.接收用户的输入
 * 3.调用HouseService完成对房屋信息的各种操作
 */
public class HouseView {

    private boolean loop = true;//控制显示器
    private char key = ' ';//接收用户选择
    private HouseService houseService = new HouseService(2);//设置数组大小

    //显示房屋列表
    public void listHouses(){
        System.out.println("\n\n===============房屋列表===============");
        System.out.println("编号\t\t房主\t\t\t电话\t\t地址\t\t月租\t\t状态(未出租/已出租)");
        House[] houses = houseService.list();//得到房屋信息
        for (int i = 0; i < houses.length; i++) {
            if (houses[i]!=null){//判断，当数组为非空时，才显示
                System.out.println(houses[i]);
            }else{//为空就退出
                break;
            }
        }
        System.out.println("===============房屋列表显示完毕===============");
    }

    //接收输入，创建House对象，调用add方法
    public void addHouse(){
        System.out.println("\n\n===============添加房屋===============");
        System.out.print("姓名：");
        String name = Utility.readString(8);
        System.out.print("电话：");
        String phone = Utility.readString(11);
        System.out.print("地址：");
        String address = Utility.readString(18);
        System.out.print("月租：");
        int rent = Utility.readInt();
        System.out.print("状态：");
        String state = Utility.readString(3);

        //创建一个新的对象，将信息保存,注意id是系统分配的，
        House house = new House(0, name, phone, address, rent, state);
        if (houseService.add(house)){
            System.out.println("===============添加房屋成功===============");
        }else{
            System.out.println("===============添加房屋失败===============");
        }
    }

    //接收用户输入的id信息。调用Service的del方法
    public void delHouse(){
        System.out.println("\n\n===============删除房屋信息===============");
        System.out.print("请输入待删除房屋的编号(-1退出)：");
        int delId = Utility.readInt();
        if (delId == -1){
            System.out.println("===============放弃删除房屋===============");
            return;
        }

        //该方法本身就有循环判断的逻辑，必须输入Y/N
        char choice = Utility.readConfirmSelection();
        if (choice =='Y'){
            if (houseService.del(delId)){
                System.out.println("===============删除房屋信息成功===============");
            }else{
                System.out.println("===============房屋编号不存在，删除失败===============");
            }
        }else{
            System.out.println("===============放弃删除房屋===============");
        }

    }

    //查找房屋信息
    public void findHouse(){
        System.out.println("\n\n===============查找房屋信息===============");
        System.out.print("请输入要查找房屋的编号(-1退出)：");
        int findId = Utility.readInt();
        if (findId == -1){
            System.out.println("===============退出查找房屋===============");
            return;
        }

        House house = houseService.find(findId);
        if (house==null){
            System.out.println("===============未找到你要寻找的房屋===============");
        }else{
            System.out.println("已找到你需要的房屋：");
            System.out.println(house);
            System.out.println("===============房屋查找结束===============");
        }
    }

    //修改房屋信息
    public void ReviseHouse(){
        System.out.println("\n\n===============修改房屋信息===============");
        System.out.print("请输入要修改房屋的编号(-1退出)：");
        int ReviseId = Utility.readInt();
        if (ReviseId == -1){
            System.out.println("===============退出修改房屋===============");
            return;
        }

        if (!houseService.Revise(ReviseId)){
            System.out.println("未找到你要的房屋,修改不了信息");
            System.out.println("===============结束房屋修改===============");
        }

    }

    //退出
    public void exit(){
        //这里使用Utility提供的方法完成确认
        char c = Utility.readConfirmSelection();
        if (c =='Y'){
            loop = false;
        }
    }

    //显示主菜单
    public void mainMenu(){

        do {
            System.out.println("\n\n===============房屋出租系统菜单===============");
            System.out.println("\t\t\t\t1 新 增 房 源");
            System.out.println("\t\t\t\t2 查 找 房 屋");
            System.out.println("\t\t\t\t3 删除房屋信息");
            System.out.println("\t\t\t\t4 修改房屋信息");
            System.out.println("\t\t\t\t5 显示房屋信息");
            System.out.println("\t\t\t\t6 退       出");
            System.out.print("请输入你的选择(1-6)：");

            key = Utility.readChar();
            switch(key){
                case '1':
                    addHouse();
                    break;
                case '2':
                    findHouse();
                    break;
                case '3':
                    delHouse();
                    break;
                case '4':
                    ReviseHouse();
                    break;
                case '5':
                    listHouses();
                    break;
                case '6':
                    exit();
                    break;
            }

        } while(loop);

    }

}
```

### 业务层

```java
package com.hwg.variable.project.HouseToRent.service;

import com.hwg.variable.project.HouseToRent.domain.House;
import com.hwg.variable.project.HouseToRent.utils.Utility;

/**
 * HouseService [业务层]
 * 定义House[] 保存House对象
 * 响应HouseView的调用
 * 完成对房屋信息的各种操作(增删查改)
 */
public class HouseService {

    private House[] houses;//保存House对象
    private int houseNums = 1;//记录当前数组有多少个元素
    private int idCounter = 1;//记录当前的id增长到那个值

    public HouseService(int sit) {
        houses = new House[sit];//当创建HouseService对象时，指定数组大小
        //初始化一个对象，方便测试
        houses[0] = new House(1, "许文强", "18888888888", "铜锣湾", 10000, "未出租");
    }

    //方法
    //返回函数数组
    public House[] list() {
        return houses;
    }

    //添加新对象，返回boolean
    public boolean add(House newHouse) {
        label1:
        if (houseNums == houses.length) {//判断是否还能在添加
            System.out.println("位置已满，添加不进房源");
            System.out.println("你是否要扩容数组容量(y/n)");
            String s = Utility.readString(1);
            if (s.equals("y")) {
                House[] newHouses = new House[houses.length + 1];
                for (int i = 0; i < houses.length; i++) {
                    newHouses[i] = houses[i];
                }
                houses = newHouses;
                System.out.println("数组扩容完毕");
                break label1;//扩容完成后跳出label标签所指向的方法
            } else {
                System.out.println("暂不扩容");
                return false;
            }
        }

        //id自增长的机制，然后更新newHouse的id
        newHouse.setId(++idCounter);
        //把newHouse对象加入到数组，新增加了一个房源
        houses[houseNums++] = newHouse;
        return true;

    }

    //del ，删除一个房屋信息
    public boolean del(int delId) {
        //应当先找到要删除的房屋信息对应的下标，下标和房屋的编号不是一回事
        int index = -1;
        for (int i = 0; i < houseNums; i++) {//有几个房屋就判断几次，不全部判断
            if (delId == houses[i].getId()) {//要删除的房屋(id)，是数组下标为i的元素
                index = i;
            }
        }

        if (index == -1) {//说明delId在数组中不存在
            return false;
        }

        //这里houseNums-1是，houseNums是有几个房屋信息，但是数组的下标是从0开始，所以要减一，不然会报错
        for (int i = index; i < houseNums - 1; i++) {
            houses[i] = houses[i + 1];
        }
        //这里把存在的房屋信息的最后一位滞空，就是删除了 --houseNUms也表示房屋少了一个
        houses[--houseNums] = null;
        return true;

    }

    //修改房屋信息
    public boolean Revise(int ReviseId){
        House house = find(ReviseId);
        if (house == null){
            return false;
        } else{
            System.out.println("已查找到你要修改的房屋，如要修改请输入新的数据，不用修改即直接回车：");
            System.out.print("姓名("+house.getName()+")：");//展示原来的数值
            String name = Utility.readString(8,house.getName());//获取输入的，如果直接回车就是使用默认值
            house.setName(name);//将新的或未更改的原值重写写入
            System.out.print("电话("+house.getPhone()+")：");
            String phone = Utility.readString(11,house.getPhone());
            house.setPhone(phone);
            System.out.print("地址("+house.getAddress()+")：");
            String Address = Utility.readString(16,house.getAddress());
            house.setAddress(Address);
            System.out.print("月租("+house.getRent()+")：");
            int rent = Utility.readInt(house.getRent());
            house.setRent(rent);
            System.out.print("状态("+house.getState()+")：");
            String state = Utility.readString(8,house.getState());
            house.setState(state);

            System.out.println("===============房屋修改成功===============");
            return true;
        }

    }

    //根据id查找房屋
    public House find(int id) {
        for (int i = 0; i < houseNums; i++) {
            if (id == houses[i].getId()) {
                return houses[i];
            }
        }
        return null;

    }

}
```

### 程序入口

```java
package com.hwg.variable.project.HouseToRent;

import com.hwg.variable.project.HouseToRent.view.HouseView;

public class HouseRentApp {
    public static void main(String[] args) {
        //创建HouseView对象，并且显示主菜单，是整个程序的入口
        new HouseView().mainMenu();
        System.out.println("==========你退出了房屋出租系统=========");
    }
}
```

## 10. 面向对象编程(高级部分)

 ### 10.1 类变量和类方法

#### 10.1.1 类变量快速了解

```java
public class ChildGame {
    public static void main(String[] args) {

        Child child1 = new Child("jack");
        child1.join();
        child1.count++;
        Child child2 = new Child("tom");
        child2.join();
        child2.count++;
        Child child3 = new Child("miss");
        child3.join();
        child3.count++;

        //类变量可以通过类名来访问
        System.out.println("共有"+Child.count+"个小孩在玩");

    }
}

class Child{
    private String name;
    //定义一个变量 count ，是一个类变量(静态变量) static静态
    //该变量最大的特点就是会被Child类的所有的对象实例共享
    public static int count = 0;

    public Child(String name){
        this.name = name;
    }
    public void join(){
        System.out.println(name+ "加入了游戏");
    }
}
```

**1.静态变量是被同一个类的所有对象共享的  2.静态变量是在类加载的时候就生成了**

#### 10.1.2 类变量详讲

**什么是类变量**

类变量也叫静态变量/静态属性，是该类的所有对象共享的对象，任何一个该类的对象去访问它时，取到的都是相同的值，同样任何一个该类的对象去修改它时，修改的也是同一个变量

**类变量的定义**

访问修饰符 static 数据类型 变量名

static 访问修饰符 数据类型 变量名

**如何访问类变量**

类名.类变量名

对象名.类变量名

【静态变量的访问修饰符的访问权限和范围是和普通属性一样的】

```java
public class VisitStatic {
    public static void main(String[] args) {
        //类名.类变量名
        //类变量时随着类的加载而创建的，所有即使没有创建对象实例也可以访问
        System.out.println(A.name);

        //通过对象名.类变量名
        A a = new A();
        System.out.println(a.name);
    }
}

class A{
    //类变量的访问，必须遵守相关的访问权限
    public static String name = "jack";
    //普通属性
    private int num = 10;
}
```

**类变量的使用细节**

1.什么时候需要用类变量：

当我们需要让某个类的所有对象都共享一个变量时，就可以考虑使用类变量（静态变量)：比如：定义学生类，统计所有学生共交多少钱。Student(name,static fee)

2.类变量与实例变量（普通属性）区别：

类变量是该类的所有对象共享的，而实例变量是每个对象独享的。

3.加上statici称为类变量或静态变量，否则称为实例变量/普通变量/非静态变量

4.类变量可以通过类名.类变量名或者对象名.类变量名来访问【==前提是满足访问修饰符的访问权限和范围==】

5.实例变量不能通过类名.类变量名来访问

6.静态变量时类加载的时候，就创建了，所以我们没有创建对象实例，也可以通过类名.类变量名来访问

7.类变量的生命周期是随类的加载开始，随着类消亡而销毁

```java
public class StaticDetail {
    public static void main(String[] args) {

        B b = new B();
        //实例变量不能通过类名.类变量名来访问
//        System.out.println(B.n1);//错误
        System.out.println(B.n2);

        //静态变量时类加载的时候，就创建了，所以我们没有创建对象实例，也可以通过类名.类变量名来访问
        System.out.println(C.name);

    }
}

class B{
    public int n1 = 100;
    public static int n2 = 200;
}

class C{
    public static String name = "张三";
}
```

#### 10.1.3 类方法快速了解

类方法也叫静态方法

形式如下：

访问修饰符 static 数据返回类型 方法名(){ }

static 访问修饰符 数据返回类型 方法名(){ }

**类方法的调用**

类名.类方法名 或者 对象名.类方法名【==前提是满足访问修饰符的访问权限和范围==】

```java
public class StaticMethod {
    public static void main(String[] args) {

        Stu jack = new Stu("jack");
        //对象名.类方法名
        jack.payFee(1000);

        Stu ton = new Stu("ton");
        ton.payFee(4999);

        //类名.类方法名
        Stu.showFee();

    }
}

class Stu{
    private String name;//普通变量
    //类变量
    private static double fee = 0;

    public Stu(String name) {
        this.name = name;
    }

    //当方法使用了static修饰后，该方法就是静态方法
    //静态方法就可以访问静态属性/变量
    public static void payFee(double fee){
        Stu.fee +=fee;//累加
    }

    public static void showFee(){
        System.out.println("总学费："+Stu.fee);
    }
}
```

**类方法的使用场景**

当方法中不涉及到任何和对象相关的成员时，则可以将方法设计成静态方法，提高开发效率

#### 10.1.4 类方法详讲

1)类方法和普通方法都是随着类的加载而加载，将结构信息存储在方法区：

类方法中无this的参数普通方法中隐含着this的参数

2)类方法可以通过类名调用，也可以通过对象名调用。

3)普通方法和对象有关，需要通过对象名调用，比如对象名方法名（参数），不能通过类名调用。

4)类方法中不允许使用和对象有关的关键字，比如this和super。普通方法可以

5)类方法中 只能访问静态变量和静态方法

6)普通成员方法即可以访问非静态成员，也可以访问静态成员

小结：静态方法，只能访问静态的成员，非静态方法，可以访问非静态方法，也可以访问静态方法(==必须遵守访问权限==)

```java
public class StaticMethodDetail {
    public static void main(String[] args) {
        D.hi();

        //非静态方法，不能通过类名调用
//        D.say();//错误，需要先创建对象，在调用
        new D().say();
    }
}

class D{
    private int n =100;
    private static int n2 = 200;
    public void say(){//非静态方法
        System.out.println("say");
    }

    public static void hi(){//静态方法
        System.out.println("hi");
        //类方法中不允许使用和对象有关的关键字，比如this和super。普通方法可以
//        System.out.println(this.n);
    }

    //类方法中 只能访问静态变量和静态方法
    public static void hello(){
        System.out.println(n2);
        System.out.println(D.n2);
//        System.out.println(this.n2);//不能使用
        hi();
//        say();//错误
    }

    //普通成员方法即可以访问非静态成员，也可以访问静态成员
    public void ok(){
        //非静态成员
        System.out.println(n);
        say();
        //静态成员
        System.out.println(n2);
        hi();
        hello();
    }
}
```

#### 10.1.5 理解main方法语法

#### 10.1.6 深入理解main方法

解释main方法的的形式：public static void main(String[] args){ }

1.main方法是虚拟机调用的

2.java虚拟机需要调用类的main()方法，所以该方法的访问权限必须是public

3.java虚拟机在执行main()方法时不必创建对象，所以该方法必须是static

4.该方法接收String类型的数组参数，该数组中保存执行java命令是传递给所运行的类的参数

5.java执行的程序 参数1 参数2 参数3

![](https://cdn.jsdelivr.net/gh/HWG56127443/Image/image-20220409200708558.png)

**特别提示:**

1）在main()方法中，我们可以直接调用main方法所在类的静态方法或静态属性

2）但是，不能直接访问该类中的非静态成员，必须创建该类的一个实例对象后，才能通过这个对象去访问类中的非静态成员

```java
public class Main01 {

    //静态的属性
    private static String name = "牛马";
    //非静态属性
    private int n1 = 1000;

    //静态方法
    public static void hi(){
        System.out.println("Main的hi方法");
    }

    //非静态方法
    public void say(){
        System.out.println("Main的say方法");
    }

    public static void main(String[] args) {

        //可以直接使用name
        //静态方法main 可以访问本类的静态成员
        System.out.println(name);
        hi();

        //静态方法main 不可以访问本类的非静态成员
//        System.out.println(n1);//错误
//        say();//错误

        //静态方法main 要访问本类的非静态成员，需要先创建对象，在调用即可
        Main01 main01 = new Main01();
        System.out.println(main01.n1);
        main01.say();
    }
}
```

### 10.2 代码块

#### 10.2.1 初识代码块

**基本介绍**

代码块又称为初始化块，属于类中的成员[即，是类的一部分]，类似于方法，将逻辑语句封装在方法体中，通过{}包围起来。

但和方法不同，没有方法名，没有返回，没有参数，只有方法体，而且不同通过对象或类显示调用，而是加载类时，或创建对象时隐式调用

**基本语法**

[修饰符]{

代码

};

说明：

1）修饰符可选，要写的话，也只能写static

2）代码块分为两类，使用static修饰的叫静态代码块，没有static修饰的，叫普通代码块

3）逻辑语句可以为任何逻辑语句（输入、输出、方法调用、循环、判断等）

4）;号可以写上，也可以省略

```java
public class CodeBlock01 {
    public static void main(String[] args) {
        Movie movie = new Movie("你好，李焕英");
        System.out.println("=============");
        Movie movie1 = new Movie("唐探3", 34, "成思城");
    }
}

class Movie {
    private String name;
    private double price;
    private String director;

    //下面是三个构造器都有相同的语句，这样代码看起来比较冗余，这时我们把相同的语句，放到一个代码块中即可
    //这样不管我们调用那个构造器，创建对象，都会先调用代码块的内容
    //代码块调用的顺序优先于构造器
    {
        System.out.println("电影屏幕打开了");
        System.out.println("电影开始了");
    };
    public Movie(String name) {
        System.out.println("Movie(String name) 被调用");
        this.name = name;
    }

    public Movie(String name, double price) {
        this.name = name;
        this.price = price;
    }

    public Movie(String name, double price, String director) {
        System.out.println("Movie(String name, double price, String director) 被调用");
        this.name = name;
        this.price = price;
        this.director = director;
    }
}
```

#### 10.2.2 代码块详讲

1）static代码块也叫静态代码块，作用就是对类进行初始化，而且它随着==类的加载==而执行，并且只会执行一次，如果是普通代码块，没创建一个i对象，就执行

2）类什么时候被加载

1.创建对象实例时(new)

2.创建子类对象实例，父类也会被加载

3.使用类的静态成员时(静态属性，静态方法)

3）普通代码块，在创建对象实例时，会被隐式调用，被创建一次，就会调用一次，如果只是使用类的静态成员时，普通代码块不会被执行

```java
public class CodeBlockDetail01 {
    public static void main(String[] args) {

        //类加载的情况
        //1.创建对象实例
//        AA aa = new AA();

        //2.创建了子类对象实例，父类也会被加载，而且父类先被加载，子类后被加载
        AA aa1 = new AA();
        System.out.println("==============");
        //3.使用类的静态成员时
        System.out.println(Cat.n);
        System.out.println("=============");
        //static代码块，是在类加载时，执行的，而且只会执行一次
        //普通代码块，在创建对象实例时，会被隐式调用，被创建一次，就会调用一次
        CC cc = new CC();
        CC cc1 = new CC();
        System.out.println("===========");
        //如果只是使用类的静态成员时，普通代码块不会被执行
        System.out.println(DD.n);

    }
}

class DD{
    public static int n = 100000;
    //静态代码块
    static {
        System.out.println("CC的静态代码块被执行");
    }
    //普通代码块可以简单的理解为是构造器的补充
    {
        System.out.println("CC的普通代码块被执行");
    }
}

class CC{
    //静态代码块
    static {
        System.out.println("CC的静态代码块被执行");
    }
    //普通代码块
    {
        System.out.println("CC的普通代码块被执行");
    }
}

class Cat{

    public static int n = 1000;//静态属性

    //静态代码块
    static {
        System.out.println("Cat的代码块被执行");
    }
}

class BB{
    //静态代码块
    static {
        System.out.println("BB的代码块被执行");
    }
}

class AA extends BB{
    //静态代码块
    static {
        System.out.println("AA的代码块被执行");
    }
}
```
