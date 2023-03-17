# Java基础

一、JDK是什么？
1.JDK全称Java Development Kit 中文意思是Java 开发工具包
2.JDK是sun公司开发的
3.JDK包括 jre (Java Runtime Environment) Java 运行环境，一堆Java工具和Java基础的类库
4.JDK下载网址：http://www.sun.com

jre为运行环境

JDK  = JRE + Java的开法工具

JRD = JVM +Java核心类库

JDK(JRE(JVM))

JAVA_HOME = bin的上一层目录

path  = %JAVA_HOME%bin

(Java运行环境)

<font color= "red">JVM(Java虚拟机)</font>

#### 常用的几个命令操作有那些？

cd

md

rd

del 

cd..

cd/

### 创建类 

创建java文件: ChairMan.java

public class  类名chairman{

   public static void main (Strinf[] args){

​        System.out.printLn(""); //输出

}

}

#### 编译和运行指令

编译： java ChairMan.Java

运行：java.ChairMan



#### java基础语法

关键字和保留字 

```java
public class Class {
    public static void main(String[] args) {
        System.out.println("helloWorld");
    }
}

```

二进制 0d   八进制0   十六进值0x

BigDecimal   浮点型类 银行存储

long 需要加个L(小写)

float 需要加个 f

#### 强制转换

高精度转换低精度的时候需要强制转换   int i =6  byte b = (byte)i;

#### 常量 

final double PI =3.14

<=>C语言中的#define



## 命名规范

类成员变量:首字母小写和驼峰规则：monthSalary

局部变量：首字母小写和驼峰规则

常量：大写字幕和下划线：	MAX_VALUE

类名：首字母小写和驼峰规则：Man,GoodMan

方法名：首字母小写和驼峰规则：run(),runRun

#### 包机制

import 引用包成员

例： import package1[.package2...].(classname\*);

​        import.java.util.*工具包

​        import.java.net*网络包

import.java.util.scanner 表示只会引入scanner(推荐)

package 的作用是声明当前类所在的包，需要放在类或着文件的最上面



java doc 生成文档

com.公司名.项目名.业务模块名

1. 区分相同名字的类
2. 可以引用相同名字的类
3. 控制访问访问

#### Scanner 对象

可以获取用户输入

例：  Scanner  scanner = new Scanner =(System.in);

```java
package 基础语法.com.ansisn;

import java.net.SocketTimeoutException;
import java.util.Scanner;

public class scanner {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("next");//next以空白为结束符   nextLine以回车为结束符
        //判断用户是否输出字符串
        if (scanner.hasNext()) {//hasNextline
            String str = scanner.next();
            System.out.println("输出内容是：" + str);
        }
        scanner.close();

    }
}
     
```




#### for的强化使用

```
int [] num ={10 ,20,30,50};

for(int x ：num)    <=>   for（int i=0,i<num.length;i++)
```



#### 方法《=》C的函数



#### 方法的重载规则：

（1） 方法名相同

（2）参数列表必须不同

（3）方法的返回类型可以相同可以不同

（4）仅仅返回类型不同不足以成为方法重载。



#### 可变参数Variadic  parameters

```java
package 基础语法.com.ansisn;

public class Variadicparameters {
    public static void main(String[] args) {
        Variadicparameters variadicparameters = new Variadicparameters();
        variadicparameters.text( 2,3,4,5);
    }
    public  static  void text(int... i){//可传任意个数
        System.out.println(i[2]);
    }
}

```

#### 数组

int [] num;

num = new int[10]; //开辟十个空间

![1673858931644](assets/1673858931644.png)

#### 构造器

1. 必须和类的名字相同

2.  必须没有返回值类型，不能写void

   
  
  #### this关键字
  
  1.  this关键字可以用来访问本类得属性，方法，构造器；
  2. this用于区分当前类得属性和局部变量
  3. 访问成员方法得语法：this.方法名
  4. 访问构造器：this(参数列表)（只能在构造器调用另一个构造器，且访问语句必需在第一个语句）
  5. this不能再类定义外使用；
  
  

​    任何一个类都可以有main方法

#### 方法调用小结（提高代码的复用性）

1. 当程序执行到方法时，就会开辟一个独立的栈空间
2. 当方法执行完毕，或者执行到return语句时，就会返回
3. 返回到调用方法的地方
4. 返回后，继续执行方法后面的代码
5. 当main方法（栈）执行完毕，整个程序就会退出。

#### 递归的重要原则

1. 执行一个方法时，就创建一个新的受保护的独立空间（栈空间）
2. 方法的局部变量是独立的，不会相互影响，比如n变量
3. 如果方法中使用的是引用类型变量（比如数组，对象），就会共享该引用类型的数据
4. 递归必须退出递归条件逼近，否则无限递归
5. 当一个方法执行完毕，或者遇到return就会返回，遵守谁调用，就将结果返回给谁

## 快捷键

1. alt + ins 快速生成构造器
2. ctrl +b 可以定位到方法
3. ctrl+h 查看类的继承层次关系
4.  alt加回车 或者 .var自动分配变量名
5. CTRL+ATL+l 格式化快捷键



## 访问修饰 符号

1. 公开级别：
2. public 对外公开   （ 本类  同包 子类 不同包都可以访问   往下依次从右到左不可以访问）
3. 受保护级别：用protected修饰，对子类和同一个包中的类公开
4. 默认级别：没有修饰符，对同一个包的类公开
5. 私有级别：用private修饰，只有类本身可以访问，对外不公开
6. 只有public 和 默认 才能修饰类



# 创建对象流程

1. 加载   某类信息
2. 初始化 ： 默认初始化，显示初始化，构造器初始化
3. 返回对象地址



# 封装和继承多态

#### 封装（encapsulation）

封装就是把抽象的属性和方法封装在一起，数据保护在内部，通过方法进行操作

1. 隐藏实现细节（private）
2. 可以对数据进行验证，保证安全合理



#### 继承extends

主要价值是提高代码的复用性和可维护性

```java
public class Pupil extends Student
```

pupil为子类，students为父类

1. 代码复用性提高
2. 代码的扩展性提高了
3. 子类继承了所有属性和方法，但是私有属性和方法不能在子类直接访问，要通过父类公共的方法去访问 
4.  子类必须调用父类的构造器，完成父类的初始化
5. 如果父类构造器被覆盖了，必须在子类每一个构造器中去指定到底用父类的那一个构造器，子类加super（参数类表）；
6. 如果希望指定去调用父类某个构造器，则显示的调用一下：super（参数类表）当子类没有调任父类 构造器，会默认调任父类的默认构造器
7. super的使用需要在构造去的第一行
8. super（）和this（）只能放在构造器第一行，因此两个方法不能共存在一个构造器
9. Java所有类都是object类的子类
10. 父类构造器的调用不限于直接父类，将一直往上追随直到object类
11. 子类只能继承一个父类，即Java中的单继承机制
12. 不能滥用继承，子类和父类之间必须满足is-a的逻辑关系 
13. 不能缩小父类的访问权限



#### super

1. super.属性 访问父类属性
2. super.方法 （参数类表） 访问父类方法
3. super（参数类表） 访问构造器 

#### 方法重写/覆盖（overrid）

1. 方法覆盖就子类有一个方法，和父类的某个方法的名称，返回类型，参数一样，那么我们就说子类的这个方法覆盖了父类的方法
2. 子类的返回类型必须在父类的返回类型中，或者相同
3. 子类方法不能缩小父类的访问权限

#### 多态（polymorphic）

1. 方法的重写和重载体现多态
   1. 一个对象的编译类型和运行类型可以不一致
   2. 编译类型在定义对象时，就确定了，不能改变
   3. 运行类型是可以改变的
   4. 编译类型看定义时 = 号 的左边，运行类型看 = 号 的右边

 

例：Animal animal = new Dog(); {animal 编译类型（Javac）是Animal，运行类型(java)是Dog}

animal = new Cat(); {animal的运行类型变成 Cat ，编译类型仍然是 Animal  }

多态的前提是：两个对象存在继承关系

#### 多态的向上转型

1. 本质：父类的引用指向了子类的对象
2. 语法：父类类型    引用名 = new 子类类型（）；《==》Animal animal = new Dog()
3. 特点：编译类型看左，运行类型看右，可以调用父类所有成员（遵循访问权限）：不能调用子类中特有成员；最终运行看子类的具体实现



#### 多态的向下转型 

  Dog dog = (Dog) animal

1. 语法：子类类型   引用名 = （子类类型）父类引用；
2. 只能强转父类的引用，不能强转父类的对象
3. 要求父类的引用必须指向的是当前目标类型的对象
4. 可以调用子类类型中所有的成员

#### 多态的注意事项

1. 属性没有重写之说，属性的值看编译类型

2. instanceOf 比较操作符，用于判断对象的运行类型是否为某类型或者某类型的子类型

3. 方法定义的形参类型为父类，实参类型允许为子类

   ```
   BB bb = new BB
   bb instanceOf BB
   ```

   判断为true

# java的动态绑定机制

 

1. 当调用对象方法的时候，改方法会和改对象的 内存地址绑定/运行类型绑定
2. 当调用属性时，没有动态绑定机制

 

# object类详解



### == 与equals 方法比较

#### == 的详解

1. == 为比较运算符

2. 既可以判断基本类型也可以判断引用类型

3. 如果是基本类型，判断值是否相等

4. 如果判断引用类型，判断地址是否相等 

   

#### getcalss方法

返回该对象的运行类型

#### equals方法

1. equals是方法  

2.  只能判断引用类型

4. 默认判断地址是否相等，子类中往往重写该方法，用于判断内容是否相等 

  

#### equals方法的重写

```java
public boolean equals(object obj){
    if(this == obj){//判断两个比较对象是否相同
        return true;
    }
    if(!(obj instanceof Doctor)){
        return false;//判断是否属于doctor类
    }
    //向下转型，以为obj的运行类型是Doctor或者其子类型
    Doctor doctor = (Doctor)obj;
    return this.name.equals(doctor.name) && this.age == doctor.age;//判断各种属性是否相等
}
class Doctor{}
```



### hashCode方法

1. 提高具有哈希结构的容器效率
2. 两个引用，如果指向一个对象，则哈希值一样，否则不一样
3. 哈希值主要根据地址号，哈希值不等价于地址
4. 在集合中哈希方法需要重写

例：

  A obj1 = new A(); A obj2 = new  A(); Aobj3 =obj1 ;

### toString方法

1. 默认返回：全类名（包名+类名）+ @ +哈希值的十六进制
2. 子类往往重写toString 方法，用于返回对象属性信息 
3. 当直接输出一个对象时，默认调用toString



### finalize方法 

1. 当对象被回收时，系统自动调用该对象finalize方法。子类可以重写该方法，做一些释放资源的操作
2. 什么时候被回收：当某个对象没有引用时，则jvm就认为这个对象是一个垃圾对象，就会使用垃圾回收机制来摧毁该对象，在销毁该对象前，会先调用finalize方法
3. 垃圾回收机制的调用，是由系统决定，也可以通过System.gc（）主动触发垃圾回收机制，测试：car[name ]



# 断点调试（debug）

### 介绍

1.  在断点调试过程中，是运行状态，是以对象的运行类型来执行的
2. 断点调试是指在程序的某一行设置一个断点，调试时，程序运行到这一行就会停住，然后一步步进行调试，当发现错误时会显示
3. 断点调试也是Java底层源代码执行过程 



###  断点调试快捷键

1. F7 跳入方法内  （跳入）   F8  （跳过）逐行执行代码 
2. shift  + F8 (跳出)跳出方法
3. F9 执行到下一个断点
4. alt + shift +F7 强制进入方法



# SimpleDateFormat方法

用于格式化日期

```
SimpleDateFormat sdf = new SimpleDateFormat();
```

```java
date = new Date();detail += "\n收入情况\t+" + money + sdf.format(date) + balance;
```



# static

#### 类变量

1. 类静态变量变量实现状态共享

2. 静态变量在jdk8之前存储在方法区的静态域中，以后存储在对里面这个类对应的class对象

3. 类变量是类加载就实现的，所以没用对象实例也可以访问

4. 需遵守访问权限

5. 静态方法调用静态变量

6. 静态属性是在类加载的时候加载

    

    

#### 类（静态）方法

1. 当方法中不涉及到任何对象和相关成员时，可以设置为静态方法

2. 不存在this，super

3. 静态方法只能访问静态变量和静态方法

4. 普通方法都可以访问

5. 静态方法不能被重写

    

# 代码块

#### 基本语法

```java
[修饰符]{
  代码
};
```

1. 修饰符可以加static，也可以选择为空（默认）
2. 代码块分为默认和static
3. 如果多个构造器有重复语句，可以使用代码块，提高复用性
4. 代码块的调用优先于构造器
5. static代码块叫做静态代码块，作用就说对类进行初始化，而且它随着类的加载而执行，并且只会执行一次。如果是普通代码块，每创建一个对象，就执行。
6. 普通代码块，在创建对象实例时，会被隐式调用，被创建一次，调用一次，如果只使用类的静态成员，普通代码块不会执行
7. 静态代码块只能调用静态成员

#### 类什么时候被加载

1. 创建对象实例（new）
2. 创建子类对象实例，父类也会加载
3. 使用类的静态成员

#### 创建一个对象时，在一个类调用顺序时

（super>代码块>构造器）（静态》动态）（同级按顺序）（父类>子类）

1. 调用静态代码和静态属性初始化（注意静态代码块和静态熟悉初始化的优先级一样，如果有多个静态代码块和多个静态变量初始化，则她们定义的顺序调用）
2. 调用普通代码块和普通属性的初始化（如果有多个普通代码块和多个普通属性初始化，则按定义顺序调用）
3. 调用构造方法



####   属性初始化

属性初始化在加载类已经形成

```java
class a{
  int n =get();
  public void get(){
    system.out.println(",,,");
  }
}
```



# main方法

1. main方法时虚拟机调用

2. Java虚拟机需要调用main方法，所以该方法的访问权限是public

3. Java虚拟机在执行main方法时不必创建对象，所以使用static

4. 该方法接收String类型数组参数，该数组中保存执行java命令时传递给所有的参数类型

5. java执行的程序 在命令行对 arg[]进行传参

6. main方法可以使用当前类的静态方法和属性  

   





# 单例模式

（可从Rutime类中查找）

1. 所谓类的单例设计模式，就说采取一定的方法保证在整个的软件系统中，对某个类只能存在一个对象实例，并且该类只提供一个取得对象实例的方法

2. 单例模式：饿汉式；懒汉式

3. 单例模式（Singleton Pattern）是 Java 中最简单的设计模式之一。这种类型的设计模式属于创建型模式，它提供了一种创建对象的最佳方式。

   这种模式涉及到一个单一的类，该类负责创建自己的对象，同时确保只有单个对象被创建。这个类提供了一种访问其唯一的对象的方式，可以直接访问，不需要实例化该类的对象。
   

实例测试：

1. 构造器私有化->（防止直接new）
2. 类的内部创建对象
3. 向外暴露一个静态的公共方法  getinstance
4. 代码实现



## 饿汉式

在[类加载](https://so.csdn.net/so/search?q=类加载&spm=1001.2101.3001.7020)过程中就直接创建单例

优点:
1、不需要加锁就能保证线程安全
2、类加载时就创建好了，这样程序执行效率高。性能高

缺点:
1、正是因为类加载时就已经创建好了，无论是否使用都已经创建好了，所以会浪费一定的内存。如果一个程序有大量的饿汉式单例模式，那么在类加载时，会同时创建大量单例，会浪费硬件资源。
2、可以通过反射，创建不同的实例对象。

```java
package com.demo08;public class Simple 
    
    
{    public static void main(String[] args) {        GirlFriend instance = GirlFriend.getInstance();        System.out.println(instance);   
   }}


class GirlFriend{   
    //饿汉式   
    //构造器私有化   
    //在类的内部创建对象   
    //提供一个static方法    
    private String name; 
    private  static  GirlFriend gf = new GirlFriend("xio");  
    private GirlFriend(String name)
    {        this.name = name;  
     System.out.println("构造器被调用");} 
    public static GirlFriend getInstance()
    {        return gf;    }
}
```



## 懒汉式

1. 在使用时创建对象实例 会造成资源浪费
2. 存在线程问题

```java
package com.demo08; 
public class SimpleTon02 { 
    public static void main(String[] args) { 
        System.out.println(Cat.n);    }}


class Cat{    /*    * 懒汉式  
* 构造器初始化   
* 定义一个static的静态属性 
* 提供一个public的static方法可以返回对象  
* 只有用户使用getInstance才返回对象*/   
    private String name;   
    public static int n = 100;    
    private static Cat cat;  
    private Cat(String name) {        this.name = name;    }   
    public static Cat getInstance(){ 
        if (cat == null){  
            cat = new Cat("xxx");        }   
        return cat;    }

}
```





# final关键字

1. 使用final修饰的类不能被继承

2. 使用final修饰的方法不能被重载可以继承

3. 使用final修饰的属性不能被修改

4. 使用final修饰的局部变量不能被修改

5. final修饰的属性，一般用xx_xx命名

6. final修饰的属性在定义时必须赋值，可以在构造器和代码块中以及自身复制

7. final修饰的属性为静态时只能在定义时或者静态代码块赋值

8. final的类可以实例化对象

9. 如果类已经为final类就不需要将方法修饰为final方法

10. finial和static搭配使用可以调用该属性时，不会触发类的加载，底层编译器做了优化处理

11. 包装类为final类（integer，Double等等）

    







# 抽象类（abstract)

1. 当一个类中存在抽象方法时，需要声明抽象类
2. 当父类的一些方法不能确定时，可以用abstract关键字来修饰该方法，这个方法就说抽象方法，用abstrac来修饰该类；
3. 抽象方法没有方法体，抽象类可以没有抽象方法
4. 抽象类不能被实例化
5. abstract只能修饰方法和类
6. 如果一个类继承抽象类，则它必须实现（将抽象方法重写）抽象类的所有抽象方法，除非它自己声明为抽象类；
7. 重写方法不能使用private，final，static来修饰，因为这些方法与重写相违背



# 接口（interface）

#### 定义接口

interface 接口名

#### 接口介绍

implements(实现)

```java
class A implements Usb{
//即A类需要实现usb接口规定的方法
}
```

1. 接口就说给出一些未实现的方法，封装在一起，到某个类要使用的时候，在具体情况把这些方法实现。

2. 在jdk7以前所有的方法都是抽象方法，且可以省略abstract

3. 在jdk8之后可以有方法体

4. 默认方法需要用default关键字修饰

5. ```java
   default public void say(){
      int i;
   }
   ```

6. 静态方法可直接添加

7. 在jdk8之后可以有方法体



#### 接口的应用

当开发软件时，为了控制和管理软件，项目经理可以定义一个接口，然后程序员具体实现。

当程序员编写一个类，需要和同部门的程序员调节一个方法

接口的作用是制定标准



#### 接口的注意事项和细节

1. 接口不能被实例化

2. 接口中的所有默认方法是public方法，接口中的抽象方法，可以不用abstract修饰

3. 一个普通类实现接口，就必须将该接口所有方法实现

4. 抽象类实现接口，可以不用实现（重写）该方法

5. 一个类可以实现多个接口

   例：

6. ```java
   interface Ib(){
   
   }
   interface Ic(){
   
   }
   class pig implements Ib,Ic{}
   
   ```

   

7. 接口的属性只能是final的而且是public static final 修饰符。比如 int a = 1 <=> public static final int a=1(必须初始化)

8. 接口中的属性的访问方式：接口名.属性名

9. 一个接口不能继承其他类，但是可以继承多个接口

10. 例：interface A extends B,C{}

11. 接口的修饰符号，只能是默认，这点和类的修饰符一样

12. 接口可以对单继承进行补充，主要价值在于设计规范方法，让其他类去实现方法

13. 接口在一定程度上实现代码解耦【接口规范性 +动态绑定机制】



#### 接口的多态特性

1. 多态参数，在usb案例中，可以接收手机，相机等多种现象，体现接口多态
2. 多态数组
3. 接口存在多态传递现象



### 

# 内部类

##  基本介绍

   一个类的内部又完整的嵌套另一个类的结构，被嵌套的剋称为内部类，内部类最大特点就是可以直接访问私有属

性，并且可以体现类与类之间的包含关系

类的五大属性【属性，方法，构造器，代码块，内部类】



## 内部类的分类

- 定义在外部类的位置上

  局部内部类(有类名)

  匿名内部类（无类名）

- 定义在外部类的成员的位置

​      成员内部类（没有static修饰）

​       静态内部类（使用static）



### 局部内部类

1. 可以直接访问外部类的所有成员，包含私有成员
2. 局部内部类是定义在外部类的局部位置，在方法中或者代码块中，并且有类名
3. 类名不能添加访问修饰符，因为它的地位就说局部变量，局部变量不能使用修饰符，但是可以使用final修饰，因为局部变量可以使用final
4. 作用域：仅仅在定义它的方法代码块中
5. 局部内部类----访问--->外部类的成员【访问方式：直接访问】
6. 外部类---访问--->局部内部类的成员【访问方式：创建对象，在访问（必须在作用域内）
7. 如果外部类和局部内部类的成员重名时，默认遵守就近原则，如果想访问外部类的成员，则可以使用（外部类名.this.成员）





### 匿名内部类（重点）（AnonymousInserClass）

#### 基本语法

本质是一个类，同时是个对象，匿名内部类在局部位置中，比如方法，并且没有类名【idealDmo09演示】

```java
new 类/接口(参数类表){    
   //类体
};
```



1. 可 

1. 可以直接访问外部类的所有成员，包括私有的
2. 可以添加任意访问修饰符，地位等价与成员变量
3. 作用域和外部类的其他成员一样
4. 成员内部类访问外部类【直接访问】
5. 外部类--访问-->内部类【创建对象，访问】
6. 外部其他类访问成员内部类【例：Outerclass.Inner inner = Outer.new Inner( );使用外部类new 一个内部类==outer.new.Inner(); 等价于outer.成员变量】【创建一个返回成员内部类的方法】【new   Outer().new  Inner();】
7. 没有static修饰
8. 如果外部类和内部类的成员重名，内部类访问的话，默认遵循就近原则，如果想访问外部类的成员，则可以使用（外部类名.this.成员）



### 	静态内部类

1. 静态内部类在成员内部类的基础上，存在static修饰
2. 可以添加任意访问修饰符
3. 作用域：同其他成员，为整个类体
4. 可以访问外部类的所有静态成员
5. 外部类访问静态类【创建对象再访问 与成员内部类相似 】
6. 如果外部类和静态内部类的成员重名时，静态内部类时，遵循就近原则，如果想访问外部类的成员，则可以使用（外部类名.成员） 





# 面向对象到此结束

# 枚举（enumeration）

把具体对象一个一个列举出来的类称为枚举类

1. 枚举属于一种特殊的类，里面只包含一组有限的特定对象；





## 枚举的实现方式

1.  自定义枚举
2. 使用enum关键字

###  自定义枚举（与饿汉式相似）

1. 将构造器私有化
2. 去掉setxxx方法，防止属性被修改
3. 在本类创建static ，finial固定的对象，实现底层优化
4. 命名规范枚举对象名全都用大写
5. 枚举对象可以有多个有多个属性

### 使用enum关键字

1. 使用enum代替class
2. 使用对象名.(参数列表)【注意需要定义在最前面】
3. 如果具有多个对象使用     ,     进行间隔创建





## enum细节

1. 当我们使用enum关键词开发开发一个枚举时，默认会继承Enum类，并且为final类
2. 如果使用无参构造器创建枚举对象，则实参对象和小括号可以省略
3. 枚举对象必须放在枚举类的首行
4. 使用enmu创建 类不能使用extend进行继承，因为在Java底层已经隐式继承了Enum
5. 可以使用接口





## enmu类常用方法

1. toString:Enum类已经重写过，返回当前对象名，子类可以重写该方法，用于返回对象信息
2. name:返回对象名（常量名），子类不能重写
3. ordinary：返回当前对象位置号，默认从0开始
4. values:返回当前枚举类中所有的常量
5. valueOf:将字符串转换枚举对象，要求字符串必须为已有的常量名，否则报异常
6. compareTo:比较两个枚举常量的位置号





# 注解（Annotation）

1. 注解也被称为元数据，，用于修饰解释包类，方法，属性，构造器，局部变量等数据信息
2. 和注释一样，注解不影响程序逻辑，但注释可以被编译或运行，相当于嵌入在代码中补充信息
3. 在JavaSE中，注释的使用目的比较简单，例如标记过时功能，忽略警告等，在JavaEE中注解占据了更重要的角色，例如用来配置应用程序的任何切面，代替javaEE旧版中所遗留的代码和xml配置
4. 使用注释要做前面添加@符号，并搭配修饰符号使用



## 修饰符

1. @Override:限定莫个方法，是重写父类方法，并注释只用于该方法
2. @Dprecated:用于表示某个程序元素以过时
3. @SuppressWarnings:抑制编译器警告



调用语法 ：@SuppressWarnings("all","unchecked");



# 元注解

1. Retention:指定注解的使用范围，SOURCE（编译器使用后直接丢弃的）,CLASS（编译器把注解记录在class文件中，当运行Java程序时，jvm不会保留注释，这是默认）,RUNTIME（编译器把注解记录在class文件中，jvm会保留注解，程序可以通过放射获得注释）
2. Taget:指定注解可以在哪里使用
3. Documented:指定该注解在javadoc体现
4. Inherited:子类会继承父类注释



