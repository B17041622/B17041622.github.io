-------
## 进入Java的世界
+ 友好的语法
+ 面向对象
+ 内存管理
+ 跨平台可移植性（write once、run anywhere）
------
## Java运行方式
1. 源代码：编写源代码文件
2. 编译器：编译器运行源代码，检查错误
3. 输出：编译器会输出字节码，任何支持Java的装置都可以把它转译成可执行的内容，字节码与平台无关
4. Java虚拟机（JVM）：虚拟机可以读取和执行字节码，你的朋友不会买一台真正的Java机器，但是他们都会有Java虚拟机
------
## Coding的步骤
1. 编写源代码 Party.java
2. 执行javac程序来编译Party.java，命令 javac Party.java
3. 输出：如果程序没有错误的话，会产生Party.class这个文件
4. 运行：启动JVM来运行Party.class文件，命令java Party

![image.png](https://upload-images.jianshu.io/upload_images/19474730-d39f2c0a2aadcee9.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
------
## Java简史
![image.png](https://upload-images.jianshu.io/upload_images/19474730-06c1a6d5954e10ff.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
------
## 版本的小问题
![image.png](https://upload-images.jianshu.io/upload_images/19474730-f58656bf5aede2b7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
------
## 代码学习
![image.png](https://upload-images.jianshu.io/upload_images/19474730-8f21505f35132c27.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
核心部分
```java
int[] numList = { 2, 3, 4, 5 };

String num = "8";
int z = Integer.parseInt(num);

try{
    // ...
}catch(XXXException ex){
    // ...
}
```
## Java的程序结构
源文件->类->方法->语句
方法必须在类的内部声明
## 剖析类
![image.png](https://upload-images.jianshu.io/upload_images/19474730-af06d57b7d04d9a5.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
这本书的习惯叫法 声明一个变量，声明一个类
main()是程序的起点/入口
JVM加载XXX类，执行它的main()方法
```java
// 基本结构
public class MyFirstApp{
    public static void main(String[] args){
        // ...
    }
}
```
## 代码学习
```java
int x = 3;
System.out.print("x is " + x);
/*
Java中数字和字符串拼接的问题
注意细节
字符是char 类型，字符串是String 类型
1、数字拼接char，得到的还是数字，相当于和它的ASCII编码相加（如果定义成String 会编译错误）
2、数字拼接String，得到的是String
3、数字同时拼接char 和 String，就看和谁先拼接，和谁后拼接
4、String 拼接任何类型，得到的都是String
*/
public static void main(String[] args) {
    String s1 = 1234 + '_' + "test";
    System.out.println("s1 = " + s1);
    String s2 = 1234 + "_" + "test";
    System.out.println("s2 = " + s2);
    String s3 = "test" + '_' + 1234;
    System.out.println("s3 = " + s3);
    String s4 = "test" + 1234 + 56789;
    System.out.println("s4 = " + s4);
    System.out.println('_');
    System.out.println(0 + '_');
}
/*
s1 = 1329test
s2 = 1234_test
s3 = test_1234
s4 = test123456789
_
95
*/

double d = Math.random();
// random() 方法用于返回一个随机数，随机数范围为 0.0 =< Math.random < 1.0。[0.0, 1.0)
// static double random()

if(name.equals("Ocmo")){
    // ...
}

/*
Java中有三种循环 for，while，do...while
循环的关键是条件测试，在Java中，条件测试的结果只能是boolean值，true/false

类是对象的蓝图
Java中的绝大多数东西都是对象
用名称和类型声明变量
*/
```
## 经典问题
![image.png](https://upload-images.jianshu.io/upload_images/19474730-80ce8913bbc31246.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
Java中的integer和boolean不相容
## print与println
```java
// 输出不换行
System.out.print("blabla...");
// 输出并换行
System.out.println("blabla...");
// 输出空行
System.out.println();
```
## 代码欣赏
![image.png](https://upload-images.jianshu.io/upload_images/19474730-b8e53c4de6670546.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```java
String[] names= { "Ocmo", "Lisa", "Jony" };
int len = names.length; // 注意这里是length属性而不是方法
/*
1.java中的length属性是针对数组说的,比如说你声明了一个数组,想知道这个数组的长度则用到了length这个属性.
2.java中的length()方法是针对字符串String说的,如果想看这个字符串的长度则用到length()这个方法.
3.java中的size()方法是针对集合,测量集合元素的个数.
*/
String[] list = { "ma", "cao", "yuan" };
String a = "macaoyuan";
System.out.println(list.length);
System.out.println(a.length());

/*
random()函数包含在Math中，不需要import任何包
Math.random()的功能是产生0和1之间（包括0，但不包括1）的一个double值，要产生0到n之间的int型的随机数，可以先把Math.random()产生的double型数乘n，再进行强制转换成int型的数
比如，现在产生一个0到100（不包含100）之间的随机数：
int temp = (int)(Math.random() * 100);
*/

int x = (int)3.14;
```
------
## 有趣的小对话
![image.png](https://upload-images.jianshu.io/upload_images/19474730-57fef424124b637b.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/19474730-5407791617f6e96e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
