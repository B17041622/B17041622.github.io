-------
## Designed by Ocmo
-------
## 拜访对象村
面向对象让你的生活更美好
对象如何改变你的一生
至少程序设计工作的部分会更好，但对于是否能够受到异性的青睐就不一定了
-------
## 术语
Square继承自Shape，Shape是Square的父类，Square可以覆盖（override）Shape的方法
覆盖：由子类重新定义继承下来的方法，以改变或延伸此方法的行为
面向过程 -> 面向对象
![image.png](https://upload-images.jianshu.io/upload_images/19474730-f1f399b90195b0c2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/19474730-322ea78c81947e0e.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/19474730-997713d1a31155ac.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/19474730-270a0c7380c6bc02.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
```java
// 数据和操作数据的方法 -> 类
// 状态和行为
class Dog{
    int size;
    String breed;
    String name;
    
    void bark(){
      System.out.println("xxx.......");
    }
}

class DogTestDrive{
    public static void main(String[] args){
      Dog d = new Dog();
      d.size = 40;
      d.bark();
    }
}
```
-------
## Movie类
![image.png](https://upload-images.jianshu.io/upload_images/19474730-11ddf43a4dd1821d.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
-------
## 猜数字游戏
![image.png](https://upload-images.jianshu.io/upload_images/19474730-094a35044a3bf5a7.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
![image.png](https://upload-images.jianshu.io/upload_images/19474730-d54427f853a46483.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
-------
## 对象存放在堆内存中
![image.png](https://upload-images.jianshu.io/upload_images/19474730-70c0ae811227b841.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
-------
## 问题思考
![image.png](https://upload-images.jianshu.io/upload_images/19474730-9563d6e2f9ae7094.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
1. 面向对象设计扩展功能不需改动之前已经测试好的程序代码
2. Java中全局变量的问题：在Java中并没有全局变量这回事，然而实际上会有需要方法或者常量可被任何的程序存取（在任何类中的任何程序都可以存取public static的方法，任何变量只要加上public static final基本上都会变成全局变量取用的常数）




