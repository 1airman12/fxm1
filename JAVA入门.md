# JAVA入门

## 1.JAVA是什么

---

JAVA是一个编程语言

### JAVA学习

#### 1.JAVA可以做些什么呢?

##### 1.1三大平台

JAVASE	JAVAME	JAVAEE

###### 1.2JAVA SE

Java语言的(标准版)，用于桌面的开发，是其他两个版本的基础。

桌面应用开发

用户打开程序，程序会让用户在最短时间内找到他们需要的功能，同时主动带领用户完成工作并得到最好的体验

学习Java的目的为今后从事Java ee做基础

###### 1.3JAVA ME

Java语言(小型版)，用于嵌入式电子设备或小型移动设备

###### 1.4JAVA EE

 Java语言的(企业版)，用于web方向的网站开发。在这个领域，是当之无愧的no1

网站开发

浏览器+服务器

##### 常见六大类

###### ● 桌面应用开发

各种税务管理软件，IDEA,Clion,pycharm

###### ● 企业级应用开发

微服务，springcloud

###### ● 移动应用开发

鸿蒙，Android，医疗设备

###### ● 科学计算

matlab

###### ● 大数据开发

hadoop

###### ● 游戏开发

我的世界

#### Java为什么这么火

###### ● Java的特性

● 面向对象

###### ● 跨平台

##### ● 开源

##### ● 简单易用

##### ● 多线程

##### ● 安全性

#### JRE和JDK

##### 1.JDK是什么?有哪些内容组成?

JDK是java开发工具包

JVM虚拟机:java程序运行的地方

核心类库:java已经写好的东西,我们可以直接御用.

开发工具:javac,java、jdb,jhat...

##### 2.JRE是什么?有哪些内容组成?

JRE是java运行环境

JVM,核心类库,运行工具

##### 3.JDK,JRE,JVM三者的包含关系

JDK包含了JRE

JRE包含了JVM

#### JAV程序初体验

##### 下载和安装

---

1.通过官网下载● .[http://www.oracle.com]

2.注意针对操作系统，下载对应安装包

3.安装路径不要包含中文

4jdk安装目录

```typescript
1.bin:该路径↓存放了各种工具命令其中比较重要的有:javac和Java
2.conf:该路径下存放了相关配置文件
3.include:该路径下存放了一些平台特定的头文件
4.jmods:该路径下存放了各种模块。
5.legal:该路径下存放了各模块的授权文档
6.lib:该路径下存放了工具一些补充jar包
```

##### **配置环境变量**

```java
●JAVA_HOME
变量值填写电脑安装jdk的跟目录(C:\Program Files\Java\jdk-22)
●Path
%JAVA_HOME%\bin;%JAVA_HOME%\jre\bin;
●CLASSPATH 
.;%JAVA_HOME%\lib;%JAVA_HOME%\lib\tools.jar

```

##### Notepad++

● 常见的高级记事本Editplus  notepad++  sublime等

### 第一个程序Hello Word

#### 1.创建一个Hello Word.JAVA文件

```java
public class Helloworld{
    public static void main(String[]args){
            System.out.println("Hello world");
    }
}
```

#### 2.打开cmd，跳转到程序所在目录

```typescript
javac 你需要编译的文件名称加后缀
```

#### 3.编译结束以后回出现一个class后缀的文件,现在去运行

![image-20240414111443960](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414111443960.png)

```java
java 你需要运行的文件的名称(不需要后缀)
```

![image-20240414111731305](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414111731305.png)

#### ● 案列常见问题

##### 中英文符号间隔

```
英文的是(;)
```

##### 单词拼写问题

```
System S为大写
```

##### 类 HelloWorld 是公共的

```
源文件名应与类名一致
```

## 2.JVAA基础语法

---

### 注释

使用细节

1.注释内容不会参与编译和运行,仅仅是对代码的解释说明

2.不管是单行注释还是多行注释,在书写的时候都不要嵌套

```typescript
单行注释
//注释信息
多行注释
/*注释信息*/
文档注释
/**注释信息**/
```

```java
public class HelloWorld{
	//叫做main方法,表示程序的主入口
	public static void main(String[] args){
			/*叫做输出语句(打印语句)
			会把小括号里面的内容进行输出打印*/
			System.out.println("HelloWorld");
	}
}

```



### 关键字

---

关键字::被java赋予了特定函数的英文单词

#### 关键字特点

关键字的字母**全部小写**

常营的的代码编辑器,针对关键字有特殊的颜色标记,非常直观.

```java
public class HelloWord{
    public static void main(String[] args){
        System.out.println("这是一个关键字");
    }
}
```

![image-20240414130048606](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414130048606.png)

#### class

---

![image-20240414130323866](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414130323866.png)

class:用于(创建/定义)一个类 类是java最基本的组成单元

### 字面量

---

告诉程序员:数据在程序中的书写格式

```java
public class HelloWorld{
	public static void main(string[] args){
		18	放心嘛	1.85
	}
}
```



#### 字面量的分类

|               **字面量类型**                |                         **说明**                         |               **举例**                |
| :-----------------------------------------: | :------------------------------------------------------: | :-----------------------------------: |
|                整数型类型int                |                     不带小数点的数字                     |                666,-88                |
| <font color='red'>**小数型**</font>(double) |         <font color='red'>带小数点的数字</font>          | <font color='red'>13.14 ,-5.21</font> |
|                 字符串类型                  |                   用双引号括起来的内容                   |         "HelloWorld","放心嘛"         |
|      <font color='red'>字符类型</font>      | <font color='red'>用单引号括起来的,内容只能有一个</font> |             'A','1','我'              |
|                  布尔类型                   |                     布尔值,表示真假                      |         只有两个值:true,false         |
|                   空类型                    |                    一个特殊的值,空值                     |               值是:null               |

空类型:null只能用字符串的形式进行打印

---



```java
public class valueDemo1{
	public static void main(String[] args){
		//目标:需要大家掌握常见的数据在代码中如何书写的?
		
		//整数
		System.out.println(666);
		System.out.println(-777);
		
		//小数
		System.out.println(666);
		System.out.println(-3.14);
		
		//字符串
		System.out.println("这是一串字符串");
		System.out.println("放心嘛");
		
		//字符
		System.out.println('男');
		System.out.println('女');
		System.out.println('A');
		System.out.println('1');
		
		//布尔
		System.out.println(true);
		System.out.println(false);
		
		//空类型
		//细节:null不能直接打印店
		//如果要打印null,那么只能用字符串的形式进行打印
		System.out.println("null");
	}
}


```

##### 扩展点:特殊字符

---

###### \t	制表符

在打印的时候,把前面的字符串的长度补齐到8,或者8的整数倍.最少补1个空格,最多补8个空格.

```java
public class HelloWorld
    public static void main(string[] args){
    System.out.println("abcd"+'\t');
}
```

---

用途可以使代码更好看

```
public class valueDemo2{
	public static void main(String[] args){
	//目标:更熟悉指标的基本用法
	
	System.out.println("name"+'\t'+"age");
	System.out.println("tom"+'\t'+"18");
	}
}
```

![image-20240414145525186](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414145525186.png)

### 变量

变量:在程序执行过程中,其值有可能发生改变的量(数据)

---

####  1.变量的定义格式

> <font color='red'>数据类型 变量名=数据值;</font>
>
> 数据类型:为空间中存储的数据,加入类型[<font color='red'>限制</font>]整数?小数?...
>
> 变量名:为空间(小箱子)起的名字
>
> 数据值:存在空间里面的数值 

```java
public class valueDemo3{
	//主入口
	
	public static void main(String[]args){
		//定义变量
		//数据类型 变量名 =数据值;
		//数据类型:限定了变量能存储数据的类型
		//int(整数) double(小数)
		//变量名:就是存储空间的名字
		//作用:方便以后使用
		//数据值:真正存在变量中的数据
		
		//等号=赋值.把右边的数据赋值给左边的变量
		int age =19;
        System.out.println(age)	;	
	}
}
```

#### 2.变量的使用方法

---

##### 注意事项

###### 只能存在<font color='red'>一个值</font>

###### 变量名<font color='red'>不允许重复</font>定义

###### 一条语句<font color='red'>可以定义多个变量</font>

###### 变量在使用前<font color='red'>一定要进行赋值</font>

##### 1.输出打印

```java
int a = 10;
System.out.println(a);//10
```

##### 2.参与计算

```java
int a = 18;
int b = 12;
System.out.println(a+b);//30
```

##### 3.修改记录的值

```
int a = 10;
System.out.println(a);//10
a = 18;
System.out.println(a);//18
```

```
public class valueDemo4{
	//主入口
	
	public static void main(String[]args){
		//1.基本用法
		//定义变量,再进行输出
		int a = 10;
        System.out.println(a);	//10
		System.out.println(a);	//10
		System.out.println(a);	//10
		//2.变量参与计算
		int c =20;
		int b=20;
		System.out.println(c+b);
		//3.修改变量记录的值
		a = 50;
		System.out.println(a);//50
		System.out.println("------------");
		//注意事项
		//在一条语句中,可以使用多个变量
		int d = 100, e = 200, f = 300;
		System.out.println(d);
		System.out.println(e);
		System.out.println(f);
		System.out.println(d+e+f);
		
		//变量在使用之前必须要赋值
		//int = g;
		//g = 500;
		//建议:以后在定义变量的时候,请直接赋值
		//不要把赋值分开写.
		System.out.println(g);
	}
}
```

![image-20240414154900590](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240414154900590.png)

#### 3.使用场景

##### 重复使用某个值

##### 某个数据经常发生改变

#### 4.注意事项

##### 变量 只能存一个值

##### 变量名不能重复

##### 一条语句可以定义多个变量

##### 使用之前一定要赋值

#### 变量的练习(公交车)

----

##### 题目

```typescript
	//一开始没有乘客
	//第一站:上去一位乘客
	//第二站:上去两位乘客,下去一位乘客	
	//第三站:上去两位乘客.下去一位乘客
	//第四站:下去一位乘客
	//第五站:上去一位乘客
	//请问:到了终点站,车上还有几位乘客.
```

解答

```
public class VariableTest{
	//主入口
	public static void main(String[] args){
		//一开始没有乘客
		int count = 0;
		//第一站:上去一位乘客
		//在原有的基础上+1
		count = count + 1;
		//第二站:上去两位乘客,下去一位乘客
		//在原有的基础上+2-1,然后在赋值给count
		count = count+2-1;
		//第三站:上去两位乘客.下去一位乘客
		count = count+2-1;
		//第四站:下去一位乘客
		count = count-1;
		//第五站:上去一位乘客
		count = count+1;
		//请问:到了终点站,车上还有几位乘客.
		System.out.println(count);//3
		}
}
```

### 数据类型

#### 1.基本数据类型

<table>
    <tr>
        <td>数据类型</td>
        <td>关键字</td>
        <td>取值范围</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>byte</td>
        <td>-128~127</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>short</td>
        <td>-32768~32767</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>int</td>
        <td>-2.147483648~2147483647(10位数)</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>整数</td>
        <td>long</td>
        <td>-9223372036854775808~9223372036854775807(19位数)</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>浮点数</td>
        <td>float</td>
        <td>-3.401298e-324到1.797693e+308</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>字符</td>
        <td>char</td>
        <td>0-65535</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td>布尔</td>
        <td>boolean</td>
        <td>true,false</td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
    <tr>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
        <td></td>
    </tr>
</table>


```java
public class VariableDemo1{
	//主入口
	public static void main(String[] args){
		//byte
		byte b = -52;
		System.out.println(b);
		//short
		short s = 5625;
		System.out.println(s);
		//int
		int a = 1952;
		System.out.println(a);
		//long
		//数值后面要加L大小写都可以
		//推荐大写方便区分
		long l = 156325463L;
		System.out.println(l);
		//float
		//数值后面要加F
		float f = 1.6586F;
		System.out.println(f);
		//char
		char c = '航';
		System.out.println(c);
		//boolean
		boolean o = true;
		System.out.println(o);
	}
}
```

---

##### 整数和小数取值范围大小关系

![image-20240415122959158](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415122959158.png)

##### **练习**

###### 练习1

![image-20240415123128282](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415123128282.png)

```java
public class VariableTest1{
	//主入口
	public static void main (String[]args){
		//使用string定义name变量
		String name = "黑马谢广坤";
		System.out.println("姓名:"+name);
		//使用int定义age变量
		int age = 18;
		System.out.println("年龄:"+age);
		//使用char定义gender
		char gender = '男';
		System.out.println("性别:"+gender);
		//使用doulbe定义height
		double height = 178.9;
		System.out.println("身高:"+height);
		//使用bollean定义ds
		boolean ds = true;
		System.out.println("是否单身:"+ds);
	}
}
```



###### 练习2

![image-20240415125816010](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415125816010.png)

```java
public class VariableTest2{
	//主入口
	public static void main (String[]args){
		//使用String定义test
		String test = "送初恋回家";
		//使用String定义name
		String name = "刘鑫 张雨提 高媛";
		//使用int定义years
		int years = 2020;
		//使用double定义score
		double score = 9.0;
		System.out.println("电影名称:"+test);
		System.out.println("主演:"+name);
		System.out.println("年份:"+years);
		System.out.println("评分:"+score);
	}
}
```

###### 练习3

![image-20240415134252922](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415134252922.png)

```java
public class VariableTest3{
	//主入口
	public static void main (String[]args){
	//定义手机价格
	double price = 2599.00;
	//定义手机品牌
	String name = "华为";
	System.out.println("手机价格:"+price);
	System.out.println("手机品牌:"+name);
	}
}
```



#### 2.引用数据类型

### 标识符

---

标识符:就是给类 方法 变量等起名字

<font color='red'>由数字,字母下划线_和美元$组成</font>

<font color='red'>不能以数字开头</font>

<font color='red'>不能是关键字</font>

<font color='red'>区分大小写</font>

---

小驼峰![image-20240415140603137](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415140603137.png)

大驼峰

![image-20240415140851292](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240415140851292.png)

### 键盘录入Scanner

#### 步骤一:导包---Scanner这个类在哪

```java
import java.util.Scanner;		//导包的动作必须出现在类定义的上边.
```

#### 步骤二:创建对象---表示我要开始用Scanner这个类了

```java
Scanner sc = new Scanner(System.in);
//上面这个格式里面,只有sc是变量名,可以改变,其他的都可以变
```

#### 步骤三:接受数据---真正开始干活了

```java
int i = sc.nextInt();
//这个格式里面,只有i是变量,可以变,其他的都不允许变.
```



例子

```java
	//导包
	import java.util.Scanner;
public class ScannerDemo1{
	public static void main(String[] args){
		//导包
		
		//创建对象
		Scanner sc = new Scanner(System.in);
		//提示防止你不知道在做什么
		System.out.println("请输入整数");
		int i = sc.nextInt();
		System.out.println(i);
	}
}
```

##### 练习

<font color='red'>键盘录入两个整数,求他们的和并打印出来</font>

```java
import java.util.Scanner;
public class ScannerTest{
	public static void main(String[] args){
		//导包
		//创建对象
		Scanner sc = new Scanner(System.in);
		System.out.println("请输入第一个数字");
		//接受数据
		int number1 = sc.nextInt();
		System.out.println("请输入第二个数字");
		int number2 = sc.nextInt();
			System.out.println(number1+number2);
		
	}
}
```

### 运算符

---

运算符优先级

#### 1.算术运算符

---

```
+	加
-	减
*	乘
/	除
%	取余,取模
```



##### 隐式转换

---

![image-20240416081413775](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416081413775.png)

##### 强制转换

a=97 A=65

#### 2.自增自减运算符

![image-20240416085357634](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416085357634.png)

![image-20240416090252134](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416090252134.png)

#### 3.赋值运算符

![image-20240416090826361](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416090826361.png)

#### 4.关系运算符

![image-20240416094331027](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416094331027.png)

练习

![image-20240416101428973](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416101428973.png)

```
package com.Compare1.a;

import java.util.Scanner;

public class lianxi {
    public static void main(String[] args) {
        //键盘录入
        Scanner sc = new Scanner(System.in);
        System.out.println("请输入你的衣服时髦度");
        int me = sc.nextInt();
        System.out.println("请输入相亲对象的时髦度");
        int dx = sc.nextInt();
        System.out.println("相亲"+(me > dx));

    }
}

```



#### 5.逻辑运算符

![image-20240416102955465](C:\Users\w2071\AppData\Roaming\Typora\typora-user-images\image-20240416102955465.png)

```
&
```



#### 6.三元运算符

#### 
