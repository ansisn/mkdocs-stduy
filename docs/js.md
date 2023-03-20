mkdocs gh-deploy笔记详情

我的笔记

![img](https://i1.hdslb.com/bfs/face/4a21617295f8c3ead4b64fe8c8e0e27ebf5d15f8.jpg@96w_96h_1c_1s.webp)



## 一、**JavaScript简介(JS)**

### **1、JS概述**

​	1、JavaScript是现阶段最主流的编程语言之一，是一种运行在客服端(浏览器)的**脚本**语言，同时也是一种具有函数优先的轻量级，解释型或即时编译型的编程语言。

​	2、脚本语言（Script）：不需要进行编译，运行过程中由js引擎逐行来进行解释并执行。

​	3、JS也可以基于Node.js来进行服务端(后端)编程。

### 2、**浏览器执行解释JS**

浏览器分为两部分 ：渲染引擎和JS引擎

l 渲染引擎：用于解析HTML+CSS，俗称**内核**，比如chrome浏览器的blink。

l JS引擎：也称为JS解释器。用于读取网页中的JavaScript代码，对其进行处理后运行。比如chrome浏览器的V8。

浏览器通过内置的JS引擎对JS代码**逐行进行解释**编译。

### 3、**JS的组成**

l ECMAScript(JS语法)：

​	是由ECMA国际进行标准化的一门编程语言，ECMAScript规定了JS的编程语法和基础核心知识，是所有浏览器厂商共同遵守的**一套JS语法工业标准**。

l DOM(文档对象模型):

​	Document Object Model，简称DOM。是W3C组织推荐的处理可扩展置标语言的标准编程接口，通过DOM提供的接口来对页面上的各种元素进行操作(大小、位置、颜色等)。

l BOM(浏览器对象模型):

​	Browser Object Model，简称BOM。它提供了独立于内容的、可以于浏览器窗口进行互动的对象结构。通过BOM可以操作浏览器窗口，比如弹出框、控制浏览器跳转、获取分辨率等。

 

## **二、JS基础语法**

### **1、JS输入输出函数**

方法

说明

alert(msg)

浏览器弹出警示框

console.log(msg)

浏览器控制台打印输出信息

prompt(info)

浏览器弹出输入框，用户输入

(string类型)

 

### 2、**变量**

​	变量可以理解为存放数据的容器，便于操作存放在内存中的数据。

语法：

 

 

**var** 变量名

​	 

### 3、**数据类型**

​	JavaScript 是一种拥有**动态类型**的编程语言。不同于JAVA、C#这类后端语言，需要规定具体的数据类型。JavaScript 不用声明具体的数据类型，会在程序运行中被自动确定。

**值类型**

**(基本类型)**：

字符串（String）、数字(Number)、布尔(Boolean)、空（Null）、未定义（Undefined）

**引用类型**

**(对象类型):**

对象(Object)、数组(Array)、函数(Function)，还有两个特殊的对象：正则（RegExp）和日期（Date）

​	 

​	 

#### **简单数据类型**

##### **1、string(字符串)**

###### **1）、字符串转义符 \**

转义符

解释说明

\n

换行符

\\

斜杠 \

\’

‘单引号

\”

“双引号

\t

Tab 缩进

\b

空格

 

###### **2）、字符串的长度以及拼接**

**length属性**

​	用于获取字符串或数组长度

语法：

 

 

.length --返回长度

 

###### **3）、字符串拼接**

​	多个字符串之间可以使用 + 进行拼接。

​	在拼接前，会将与字符串拼接的任何类型转换为字符串，再拼接为一个新字符串。

​	注：使用字符串进行拼接时 ‘’ 引号采用就近原则进行匹配。

​	 

​	 

##### 2、**boolean(布尔型)**

布尔类型有true 和 false。

布尔型在与数值型进行拼接时，true为(1)，false为(0)。

 

##### 3、**Undefined(未定义)**

一个声明后没有被赋值的变量会有一个默认值(Undefined)，表示未定义数据类型(基于JavaScript的变量的特性)。

##### 4、**Null(空)**

表示为空(null)，需与Undefined区别开。

#### l **Typeof 可用来获取检测变量的数据类型**

语法：

 

 

var numb = 12;

Console.log(typeof numb); // 返回结果为 number

### 4、**数据类型转换**

##### **1\转换为字符串**

 

 

 

方式

说明

.toString()

转换为字符串

String()强制转换

转换为字符串

**+ ’ ’ 加号拼接字符串**

**和字符串拼接的结果都是字符串(隐式转换)**

 

 

 

 

 

 

 

 

 

##### **2\转换为数值型**

 

 

 

方式

说明

案例

parseInt(string)函数

将string类型转换为整数数值型

parseInt(‘35’)

parseFloat(string)函数

将string类型转换为浮点数值型

parseInt(‘23.65’)

Number()强制转换函数

将string类型转换为数值型

Number(‘12’)

js隐式转换(- * /)

利用算术运算隐式转换为数值型

‘12’ - 0

 

##### **3\转换为布尔型**

 

 

 

方式

说明

案例

Boolean()函数

将其他类型转换为布尔型

Boolean(‘true’)

 

l 代表空、否定的值会被转换为false	,如： ‘ ’ 、0、NaN、null、undefined。

l 其余值都会被转换为true。 

** **

### 5、**运算符**

#### **1\算术运算符**

概率：算术运算使用的符号，用于执行两个变量或值的算术运算。

运算符

描述

实例

+

加

10 + 20 =30

\-

减

10 - 20 =-10

*

乘

10 * 20 =200

/

除

10 / 20 =0.5

%

取余数（取模）

返回出发的余数 9 % 2 =1

 

 

 

 

 

 

 

 

 

#### **2\递增和递减运算符**

递增（++）

递减（- -）

放在变量前面时，我们称为前置递增(递减)运算符

放在变量后面时，我们称为后置递增(递减)运算符

注意：递增和递减运算符必须和变量配合使用。

 

①前置递增运算符

++num   使用口诀:先自加，后返回值

②后置递增运算符

num ++   使用口诀:先返回原值，后自加

#### **3\比较运算符**

​	是两个数据进行比较时所使用的运算符，比较运算后，会返回一个布尔值(true / false)作为比较运算的结果。所以经常将使用比较运算符的表达式用到逻辑运算符的运算中。

 

**运算符**

**说 明**

== 

表示两边表达式运算的结果相等，注意是两个等号

**===**

**(全等) 要求值和数据类型都一致**

!=

表示两边表达式运算的结果不相等

\>

表示左边表达式的值大于右边表达式的值

<

表示左边表达式的值小于右边表达式的值

\>=

表示左边表达式的值大于等于右边表达式的值

<= 

表示左边表达式的值小于等于右边表达式的值

 

#### **4\逻辑运算符**

**是用来进行布尔值运算的运算符，其返回值也是布尔值。**

**逻辑运算符**

**说明**

&&

“逻辑与”两边都是 true才返回 true，否则返回 false

||

“逻辑或”两边都为 false 才返回 false，否则都为true

！

“逻辑非”（!）也叫作取反符，用来取一个布尔值相反的值，如 true 的相反值是 false

 

 

 

 

 

 

 

 

 

 

 

##### **4.1、逻辑中断**

概念：当有多个表达式（值）时,左边的表达式值可以确定结果时,就不再继续运算(执行)右边的表达式的值。

①逻辑与 &&

语法：

表达式1 && 表达式2

 

如果第一个表达式的值为true，则返回表达式2

 

如果第一个表达式的值为false，则返回表达式1

 

 

 

②逻辑或 ||

语法：

表达式1 || 表达式2

 

如果第一个表达式的值为真，则返回表达式1

 

如果第一个表达式的值为假，则返回表达式2

 

 

 

### 6、**数组**

#### 1) **、创建数组**

**JavaScript **中创建数组有两种方式：

l 利用 new 创建数组

var array = new Array();

l 利用数组字面量 [] 创建数组

var array = [];

 

#### 2) **、数组的索引(下标)**

索引 (下标) ：用来访问数组元素的序号

array[1]; // 获取array数组的第二个元素

可通过数组的索引遍历数组元素

#### 3) **、获取数组的长度length**

使用 **length**可访问数组元素的数量。

Array.length; // 获取array数组的长度

#### **4）、在数组中增加元素**

## 二、**JS函数**

### 1、**函数(function)**

l 就是封装了一段可被重复调用执行的代码块。通过此代码块可以实现大量代码的重复使用。

l 函数可以带参数也可以不带参数

l 声明函数的时候，函数名括号里面的是形参，形参的默认值为 undefined

l 调用函数的时候，函数名括号里面的是实参

l 多个参数中间用逗号分隔

l 形参的个数需与实参个数匹配

### 2、**函数的声明及调用**

​     // 带参数的函数声明

​    function 函数名(形参1, 形参2 , 形参3...) { // 可以定义任意多的参数，用逗号分隔

​    // 函数体

​    }

 

​    // 带参数的函数调用

​    函数名(实参1, 实参2, 实参3...);

 

### 3、**函数的返回值(return)**

​	在使用 return 语句时，函数会停止执行，并返回指定的值,如果函数没有 return ，返回的值是 undefined。

// 声明函数

function 函数名（）{

  ...

  return  需要返回的值;

}

// 调用函数

函数名();  // 此时调用函数就可以得到函数体内return 后面的值

**注：**

**return 语句之后的代码不被执行。**

**return 只能返回一个值。如果用逗号隔开多个值，则返回最后一个值。**

** **

#### **break、continue、return 的区别：**

**l break ： 结束当前循环体 (如 for、while)**

**l continue ：跳出本次循环，继续执行下次循环 (如for、while)**

**l return ：不仅可以退出循环，还能够返回 return 语句中的值，同时还可以结束当前的函数体内的代码**

### 4、**函数的Arguments对象**

​	JS函数都内置了一个 arguments 对象，arguments 对象中存储了传递的所有实参。

​	arguments展示形式是一个伪数组，因此可以进行遍历。

伪数组具有以下特点：

​	 ①：具有 length 属性

​	 ②：按索引方式储存数据

​	 ③：不具有数组的 push , pop 等方法

## 三、**JS作用域**

### 1、**概念**

​	一段程序代码所作用的程序范围，而限定这段程序的可用性范围就是**作用域**。

### 2、**作用域的分类**

JavaScript (ES6前) 中的作用域有两种：

l 全局作用域 (作用在script 标签范围内)

l 局部作用域 (函数作用域)

### 3、**变量的作用域**

#### 1）**、全局变量**

在全局作用域下，声明的变量叫做全局变量（在函数外部定义的变量）

l 全局变量，变量的整个<script>标签中都可以使用。

l 特殊情况下，在函数内不使用 var 声明的变量也是全局变量（不建议使用）

#### 2）**、局部变量**

在局部作用域下，声明的变量叫做局部变量（在函数内部定义的变量）

l 局部变量只能在该函数内部使用

l 函数的形参实际上就是局部变量

#### 3）**、区别**

​	全局变量：在整个<script>标签中都可以使用，只有在浏览器关闭时才会被销毁，因此比较占内存

​	局部变量：只在函数内部使用，当其所在的代码块被执行时，会被初始化；当代码块运行结束后，就会被销毁，因此更节省内存空间

### 4、**块级作用域(ES6)**

​	块作用域由 {} 包括。在 {} 里面声明的变量不能在 {} 外调用。

​	**ES6以前，JS没有块级作用域的概念。**

## 四、**JS预解析**

### 1、**概念：**

​	JavaScript 代码是由浏览器中的 JavaScript 解析器来执行的。JavaScript 解析器在运行 JavaScript 代码的时候分为两步：

​	预解析；(JS引擎会把JS里面所有的 **var** 还有 **function** 提升到当前作用域的最前面)

​	代码执行。

​	注：预解析只会发生在通过 **var** 定义的变量和 **function** 上。

### 2、**变量预解析(变量提升)**

​	 变量的声明会被提升到当前作用域的最上面，但变量的赋值不会被提升。

​     console.log(num); // 结果是多少？

​    var num = 10; 

​    // 输出返回undefined

 

​    //相当于执行了以下代码

​    var num;    // 变量声明提升到当前作用域最上面

​    console.log(num); // 输出返回undefined

​    num = 10;   // 变量的赋值不会提升

​	 

### 3、**函数预解析(函数提升)**

#### 1、**概念：**

​	函数的声明会被提升到当前作用域的最上面，但是不会调用函数。

#### 2、**函数表达式声明调用问题**

​	函数表达式调用必须写在函数声明的下面。(**因为函数表达式是通过变量的形式接收函数的，变量提升只提升变量，不提升赋值操作**)

​    // 匿名函数(函数表达式方式):若我们把函数调用放在函数声明上面

​    fn();

​    var  fn = function() {

​      console.log('22'); // 报错

​    }

 

​    //相当于执行了以下代码

​    var fn;

​    fn();   //fn没赋值，没这个，报错

​    var  fn = function() {

​      console.log('22'); //报错

​    }

​	 

​	 

​	 

 

## 五、**JS对象**

### 1、**对象的概念**

​	在 JavaScript 中，对象是一组无序的相关**属性**和**方法**的集合，所有的事物都是对象，例如字符串、数值、数组、函数等。(对象必须是具体的事物，不能是抽象的概念)

​	对象是由**属性**和**方法**组成的：

​	属性：事物的特征，在对象中用属性来表示（常用名词）

​	方法：事物的行为，在对象中用方法来表示（常用动词）

### 2、**创建对象(object)**

#### （1）**、利用字面量创建对象 {}**

​	对象字面量：就是花括号 **{ }** 里面包含了表达这个具体事物（对象）的属性和方法，**{ }** 里面采取键值对的形式表示。

​	键：相当于属性名

​	值：相当于属性值，可以是任意类型的值（数字类型、字符串类型、布尔类型，函数类型等）。

​    var star = {

​      name : 'pink', // 多个属性或者方法中间用逗号隔开

​      age : 18,

​      sex : '男',

​      sayHi : function(){ // 方法冒号后面跟的是一个匿名函数

​        alert('大家好啊~');

​      }

​    };

​	 

#### （2）**、利用 new Object 创建对象**

​	var 对象名 = new Object();

​     var obj = new Object(); //创建了一个空的对象

​    // 对象属性赋值

​    obj.name = '张三丰';

​    obj.age = 18;

​    obj.sex = '男';

 

​    // 对象方法

​    obj.sayHi = function() {

​      console.log('hi~');

​    }

​    // 调用对象的属性以及方法

​    console.log(obj.name);

​    console.log(obj['sex']);

​    obj.sayHi();

 

 

#### （3）**、利用构造函数创建对象**

##### 1）**、构造函数的概念**

​	构造函数是一种特殊的函数，主要用来初始化对象，即为对象成员变量赋初始值，它总与 new 运算符一起使用。我们可以**将对象中一些公共的属性和方法抽取出来，然后封装到这个函数里面**。

​    //构造函数的语法格式

​    function 构造函数名() {

​      this.属性 = 值;

​      this.方法 = function() {}

​    }

​    new 构造函数名();

​	** **

 

##### 2）**、通过构造函数创建对象**

​	**在 JS 中，使用构造函数要时要注意以下几点：**

**l 构造函数名字首字母要大写**

**l 构造函数不需要return就可以返回结果**

**l 调用构造函数必须使用 new**

**l 我们只要new 构造函数() 就能创建了一个对象**

**l 我们的属性和方法前面必须加this**

​     // 创建Star构造函数

​	function Star(uname,age,sex) {

​      this.name = uname;

​      this.age = age;

​      this.sex = sex;

​      this.sing = function(sang){

​        console.log(sang);

​      }

​    }

​    

​    var ldh = new Star('刘德华',18,'男'); // 创建对象，并给对象赋初始值

​    console.log(typeof ldh) // object对象，调用函数返回的是对象

 

​    console.log(ldh.name);

​    console.log(ldh['sex']);

​    ldh.sing('冰雨'); // 调用对象方法，并传递实参

 

##### 3）**、构造函数与对象**

l 构造函数，如 Stars()，抽象了对象的公共部分，封装到了函数里面，它泛指某一大类（class）

l 创建对象，如 new Stars()，特指某一个，通过 new 关键字创建对象的过程我们也称为对象实例化

##### 4）**、New关键字**

new 在执行时的四种作用:

l 在内存中创建一个新的空对象。

l 让 this 指向这个新的对象。

l 执行构造函数里面的代码，给这个新对象添加属性和方法

l 返回这个新对象（所以构造函数里面不需要return）

#### **变量、属性、函数、方法总结**

l 变量：单独声明赋值，单独存在

l 属性：对象中的变量称为属性，不需要声明，**属性用来描述该对象的特征**

l 函数：单独存在的，通过 **函数名()** 的方式就可以调用

l 方法：对象里面的函数称为方法，方法不需要声明，使用 **对象.方法名()** 的方式就可以调用，**方法用来描述对象的行为和功能**。

### 3、**对象的调用**

**l 对象属性调用** : 对象.属性名。

​    console.log(star.name)  // 调用name属性

**l 对象属性的另一种调用方式** : 对象[‘属性名’]，注意方括号里面的属性必须加引号，我们后面会用

​    console.log(star['name']) // 调用name属性

**l 对象方法调用**：对象.方法名() ，注意这个方法名字后面一定加括号

​    star.sayHi();       // 调用 sayHi 方法 (注意：方法的调用必须用 ‘()’ )

### 4、**遍历对象属性 for in**

​	用于对数组或对象的属性进行循环操作。

var

必须，指定的变量可以是数组元素，也可以是对象的属性

Object

必须。指定迭代的的对象。

​	 

   for(变量 in 对象名字){

   	// 在此执行代码

  }

 

​    // 创建对象

​    var obj = {

​      name: '秦sir',

​      age: 18,

​      sex: '男',

​      fn:function() {};

​    };

 

​    //for in 遍历obj对象

​    for(var key in obj){

​      console.log(key); // key 变量 输出的是属性名

​      console.log(obj[key]); // 通过调用对象属性的方式，得到属性值

​    }

 

## 六、**JS内置对象**

### 1、**概念**

​	内置对象就是指 JS 语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或是最基本而必要的功能。

​	JavaScript 提供了多个内置对象：Math、 Date 、Array、String等。

### 2、**MDN文档**

​	学习一个内置对象的使用，只要学会其常用成员的使用即可，我们可以通过查文档学习，可以通过MDN来查询。

​	 

### 3、**Math对象**

#### **（1）、概念**

​	Math 对象不是构造函数，它具有数学常数和函数的属性和方法。跟数学相关的运算（求绝对值，取整、最大值等）可以使用 Math 中的成员。

​	**Math 的所有属性与方法都是静态的，不需要通过New关键字进行调用。**

#### **（2）、Math的常用属性**

##### 	1）、Math.PI	-圆周率

#### **（3）、Math的常用函数**

​	描述：如果没有参数，则结果为 - Infinity；

​	如果有任一参数不能被转换为数值，则结果为 NaN。 

##### 	1）、Math.Max() - 返回最大值

##### 	2）、Math.Min() - 返回最小值

##### 	3）、Math.abs() - 返回绝对值

##### 	4）、Math.floor() - 向下取整

##### 	5）、Math.ceil() - 向上取整

##### 	6）、Math.round() - 四舍五入

##### 	7）、Math.random() - 随机数

​	 函数返回一个浮点数， 伪随机数在范围从0 到小于1，也就是说，从 0（包括 0）往上，但是不包括 1。

得到一个范围区间的随机数，参照MDN文档公式。

 

 

 

 

​    var arr = ['张杰', '李连杰', '周杰伦', '成龙', '甄子丹'];

​    // Math.random()生成随机数

​    function getRandom(min, max) {

​      return Math.floor(Math.random() * (max - min + 1)) + min; // 含最大值，含最小值

​    }

​    console.log(getRandom(1, 10));

​    console.log(arr[getRandom(0, arr.length-1)]); 

 

### 4、**Date对象**

#### （1）**、概念**

l 创建Date实例，用于处理日期和时间。Date 对象基于自 1970 年 1 月 1 日起经过的毫秒数。

l Date对象需要通过调用Date构造函数来实例化日期对象，即 new Date()。

l 若将它作为常规函数调用（即不加 new 操作符），将返回一个字符串，而非 Date 对象。

#### （2）**、创建Date对象**

##### 	1）**、获取当前时间**

​	 var date = new Date();  // 创建日期对象

##### 	2）**、new Date() 构造函数**

​	当构造函数中没有参数，返回当前时间；

​	当构造函数中存在参数，则返回对应参数的日期时间。（参数常用的写法： 数字型 2019,10,1；  字符串型 '2019-10-1 8:8:8' 时分秒）

​     // 1.如果构造函数中没有参数，返回当前系统时间

​    var now = new Date();

​    console.log(now);

 

​    // 2.如果Date()里面写参数，则返回对应参数的日期时间 

​    var data = new Date(2019,10,1);

​    console.log(data); // 返回的是11月不是10月

​    var data2 = new Date('2019-10-1 8:8:8');

​    console.log(data2);

​	 

#### （3）**、日期格式化**

##### 	1）**、方法**

​	方法名

​	说明

​	代码

​	get FullYear()

​	获取当年

​	obj.getFullYear()

​	getMonth()

​	获取当月(0-11)

​	obj.getMonth()

​	getDate()

​	获取当天日期

​	obj.getDate()

​	getDay()

​	获取星期几(周日0到周六6)

​	obj.getDay()

​	getHours()

​	获取当前小时

​	obj.getHours()

​	getMinutes()

​	获取当前小时

​	obj.getMinutes()

​	getSeconds()

​	获取当前秒钟

​	obj.gerSeconds()

 

##### 	2）**、格式化年月日**

​     // 格式化日期格式

​    var date = new Date(); // 创建当前日期对象

 

​    // 将日期格式化显示

​    var year = date.getFullYear(); // 获取年

​    var month = date.getMonth() + 1; // 获取月--返回 0-11

​    var dates = date.getDate(); // 获取天

​    var intDay = date.getDay(); // 获取星期--返回0-6

 

​    // 将getDay返回的数值转换为星期

​    var strDay = ["星期日","星期一","星期二","星期三","星期四","星期五","星期六"]

​    var strDate = year + '年' + month + '月' + dates + '号' + strDay[intDay];

 

​    console.log(strDate);

##### 	3）**格式化时分秒**

​	// 将时间格式化显示

​    var h = date.getHours(); // 时

​    var m = date.getMinutes(); // 分

​    var s = date.getSeconds(); // 秒

 

​    // 时分秒小于10时，前面加上0

​    h = h < 10 ? '0' + h : h;

​    m = m < 10 ? '0' + m : m;

​    s = s < 10 ? '0' + s : s;

​    var strTime = h + ':' + m + ':' + s;

​    console.log(strTime);

** **

** **

#### （4）**、时间戳**

##### 	1）**、概述**

​	时间戳是指格林威治时间自1970年1月1日（00:00:00 GMT）至当前时间的总秒数。

##### 	2）**、获取当前时间总的毫秒数**

l date.valueOf() ：得到date时间对象距离1970年1月1日（08:00:00 GMT+8）总的毫秒数

l date.getTime() ：得到date时间对象距离1970年1月1日（08:00:00 GMT+8）总的毫秒数

​    // 实例化Date对象

​    var date = new Date();

 

​    // 1 .通过 valueOf() getTime() 用于获取Date对象的原始值

​    console.log(date.valueOf()); // 得到现在时间距离1970.1.1总的毫秒数

​    console.log(date.getTime());

​    // 2.简单的写法

​    var date1 = +new Date(); // +new Date()返回的就是总的毫秒数，

​    console.log(date1);

l Date.now(); 得到当前时间距离1970年1月1日（08:00:00 GMT+8）总的毫秒数

​	now() 是 Date 的一个静态函数，所以必须以 Date.now() 的形式来使用。

#### （5）**、倒计时-算法**

​	// 倒计时

​    function conutDown(dateTimes) {

​      var datetime = new Date(dates);

​      var times = (datetime.getTime() - Date.now()) / 1000; // 将开始时间与当前时间转换为秒进行计算

 

​      // 计算倒计时 天-时-分-秒

​      var day = Math.floor(times / 60 / 60 / 24);

​      var hours = Math.floor(times / 60 / 60 % 24);

​      var minutes = Math.floor(times / 60 % 60);

​      var seconds = Math.floor(times % 60);

​      var strTimes = day + '天' + hours + ':' + minutes + ':' + seconds;

​      return console.log(strTimes);

​    }

​    conutDown("2022-10-29 0:0:0");

 

### 5、**Array对象**

#### （1）**、概述**

参见文档-数组

#### （2）**、判断是否为Array**

##### 	**1)、Array.isArray(**value**); -方法**

##### 	**2)、instanceof -运算符**

当检测 Array 实例时，Array.isArray 优于 instanceof，因为 Array.isArray 能检测 iframes。

​    // 判断是否为数组类型 -Array

​    // Array.isArray(); -Array方法

​    var arr = new Array();

​    Array.isArray(arr); // true

 

​    // instanceof -运算符

​    arr instanceof Array; // true

 

#### （3）**、添加数组元素**

##### **①、unshift()函数**

在数组开头插入元素，该函数能够把一个或多个参数值附加到数组的头部

array.unshift(元素1, 元素2, ..., 元素X)

##### **②、push()函数**

把一个或多个参数值附加到数组的尾部，并返回添加元素后的数组长度

 array.push(元素1, 元素2, ..., 元素X)

 

##### **③、concat() 函数**

也可以插入给定的一个或多个元素，能够把传递的所有参数按顺序添加到数组的尾部。

​	var array1 = [1,2,3,4,5]; //定义数组

 

​	var array2 = array1.concat(6,7,8); //为数组a连接3个元素

说明：concat() 方法将创建并返回一个新数组，而不是在原来的基础上添加新元素。

##### **④、splice() 函数**

在指定下标位置插入一个或多个元素。

函数参数说明：

​	第1个参数index为指定起始下标位置；

​	第2个参数howmany指定应该删除的元素数目，当值设置为0时，就会不执行删除操作；

​	这样就可以通过第3个及后面参数item1,.....,itemX来插入一个或多个元素。

 array.splice(index,howmany,item1,.....,itemX)

#### （4）**、删除数组元素**

##### **①、delete**

 var arr = [1,true,{},"a"]; // 定义数组

 delete arr[0]; // 删除索引为 ’0’ 的数组元素

用delete删除后，数组的长度length不会发生变化，此时arr[x]变为undefined。

##### **②、pop()函数**

  var arr = [1,true,{},"a"]; // 定义数组

​     arr.pop(); // 删除数组中最后一个元素

删除数组中**最后一个**元素，并返回该元素的值。此方法会更改数组的长度。

##### **③、shift()函数**

​    var arr = [1,true,{},"a"]; // 定义数组

​     arr.shift(); // 删除数组中第一个元素

删除数组中**第一个**元素，并返回该元素的值。此方法更改数组的长度。

#### （5）**、筛选数组-算法**

​    // 筛选数组，将数组[2000, 1500, 5000, 600]中大于2000的添加到新数组中

​    var array = [2000, 1500, 5000, 600];

​    var newArr = new Array();

​    for (let index = 0; index < array.length; index++) {

​      // 大于2000添加到newArr数组中

​      if (array[index] > 2000) {

​        newArr.push(array[index]);  

​      }

​    }

​    console.log(newArr);

#### （6）**、数组排序**

##### **①、reverse()函数**

​     var array = [2000, 1500, 5000, 600];

​    array.reverse(); // [600, 5000, 1500, 2000]

将数组中元素的位置反转，并返回该数组。

##### **②、sort()函数**

​    // 数组排序(冒泡排序)

​    var array = [2, 1, 5, 6];

​    array.sort();

​    console.log(array); // [1, 2, 5, 6]

 

​    // 对于双位数

​    var arr = [1,64,9,61];

​    arr.sort(function(a,b) {

​      return b - a; //降序的排列

​      return a - b; //升序

​      }

​    )

 

​	将数组中元素进行排序，排序顺序是在将元素转换为字符串，然后比较它们的** UTF-16 **代码单元值序列时构建的。（可以比较字符串）

​	于具体实现，因此无法保证排序的时间和空间复杂性。

#### （7）**、获取Array元素索引**

##### **①、indexOf()函数**

​    var array = [2000, 1500, 5000, 600, 2000];

​    array.indexOf(2000); // 返回数组元素的索引: 1

返回在数组中可以找到指定元素的第一个索引（可能存在该元素在数组中重复出现），如果不存在，则返回 -1。

##### **②、lastIndexOf()函数**

​       var array = [2000, 1500, 5000, 600, 2000];

​    array.lastIndexOf(2000); // 返回数组元素的索引: 4

返回指定元素在数组中的最后一个的索引，如果不存在则返回 -1。从数组的后面向前查找

## 七、**JS的事件函数**

### 1、**Is NaN();**

​	用于判断一个变量是否为非数值，返回布尔型。

- **14
- **60
- **86


- [首页](https://www.bilibili.com/)
- [番剧](https://www.bilibili.com/anime/)
- [直播](https://live.bilibili.com/)
- [游戏中心](https://game.bilibili.com/platform)
- [会员购](https://show.bilibili.com/platform/home.html?msource=pc_web)
- [漫画](https://manga.bilibili.com/?from=bill_top_mnav)
- [赛事](https://www.bilibili.com/match/home/)
- [下载客户端](https://app.bilibili.com/)


- [![img](https://i2.hdslb.com/bfs/face/077ab2fc52c91d11effdb4eecc31a476c8de2d74.jpg@120w_120h_1c)](https://space.bilibili.com/159940583)
- [大会员](https://account.bilibili.com/account/big)
- [消息](https://message.bilibili.com/)
- [动态](https://t.bilibili.com/)
- [收藏](https://space.bilibili.com/159940583/favlist)
- [历史](https://www.bilibili.com/account/history)
- [创作中心](https://member.bilibili.com/platform/home)
- ​
- [投稿](https://member.bilibili.com/platform/upload/video/frame)

# JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续

![img](https://s1.hdslb.com/bfs/static/jinkela/video/asserts/view.svg)634.3万![img](https://s1.hdslb.com/bfs/static/jinkela/video/asserts/dm.svg)21.4万![img](data:image/svg+xml;base64,PHN2ZyB0PSIxNjQyNTg4MTEzODk5IiBjbGFzcz0iaWNvbiIgdmlld0JveD0iMCAwIDEwMjQgMTAyNCIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHAtaWQ9IjY4MjciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCI+PGRlZnM+PC9kZWZzPjxwYXRoIGQ9Ik0xNjcuMDI0IDUxMmEzNDQuOTc2IDM0NC45NzYgMCAxIDEgNjg5Ljk1MiAwIDM0NC45NzYgMzQ0Ljk3NiAwIDAgMS02OTAgMHpNNTEyIDEwNi45NzZhNDA1LjAyNCA0MDUuMDI0IDAgMSAwIDAgODEwLjA0OCA0MDUuMDI0IDQwNS4wMjQgMCAwIDAgMC04MTB6IG0zMCAyMzUuMDA4YTMwIDMwIDAgMSAwLTYwIDBWNTEyYzAgNy45NjggMy4xNjggMTUuNiA4Ljc4NCAyMS4yMTZsMTIwIDEyMGEzMCAzMCAwIDEgMCA0Mi40MzItNDIuNDMyTDU0MiA0OTkuNTJWMzQxLjk4NHoiIGZpbGw9IiM5NDk5QTAiIHAtaWQ9IjY4MjgiPjwvcGF0aD48L3N2Zz4=) 2020-09-01 18:09:44**未经作者授权，禁止转载


6.0万6.0万13.2万2.7万

稿件投诉

50 篇笔记

素材大全：https://gitee.com/xiaoqiang001/java-script.gitPPT 在我账号专栏里面网盘地址1.JavaScript基础从变量的定义与使用、流程控制语句、数组、函数、构造函数、内置对象以及对象等2.web API 讲解如何获取DOM元素，如何操作DOM 元素，BOM操作 移动端制作网页特效3. 后面还会有js高级，ES6类面向对象语法，面向对象案例，原型和原型链等等。4. 还有会jquery 综合 + echarts数据可视化

展开更多

- [科技](https://www.bilibili.com/v/tech/)
- [计算机技术](https://www.bilibili.com/v/tech/computer_tech)
- [视频教程](https://search.bilibili.com/all?keyword=%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B&from_source=video_tag)
- [js入门视频](https://search.bilibili.com/all?keyword=js%E5%85%A5%E9%97%A8%E8%A7%86%E9%A2%91&from_source=video_tag)
- [JavaScript](https://search.bilibili.com/all?keyword=JavaScript&from_source=video_tag)
- [WEB前端开发](https://search.bilibili.com/all?keyword=WEB%E5%89%8D%E7%AB%AF%E5%BC%80%E5%8F%91&from_source=video_tag)
- [前端入门视频](https://search.bilibili.com/all?keyword=%E5%89%8D%E7%AB%AF%E5%85%A5%E9%97%A8%E8%A7%86%E9%A2%91&from_source=video_tag)
- [pink老师](https://search.bilibili.com/all?keyword=pink%E8%80%81%E5%B8%88&from_source=video_tag)


- ​

  ​

  最新

发布

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

黑马前端

*置顶*全套配套资料教程，关注微信公众号：黑马程序员，回复：领取资源02
2022版前端最新最全学习路线图
![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[2023年web前端开发学习路线图]()
资源下载问题
![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[黑马程序员教程资源下载指南]()
web入门
H5C3+移动布局 ：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程]()
JavaScript系列：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续]()
技术进阶
[jQuery]()**：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员前端基础教程|jQuery网页开发案例精讲]()
Ajax：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员AJAX零基础到精通_整合Git核心内容全套教程（2022年已更新优化）]()
Vue开发
Node.js: ![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员Node.js全套入门教程，nodejs新教程含es6模块化+npm+express+webpack+promise等_Nodejs实战案例详解]()   
Vue2+Vue3全套：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员Vue全套视频教程，从vue2.0到vue3.0一套全覆盖，前端学习核心框架教程]()
React&小程序开发
React：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员前端React视频教程，react零基础入门原理详解到好客租房项目实战]()
零基础玩转微信小程序：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员前端微信小程序开发教程，微信小程序从基础到发布全流程_企业级商城实战(含uni-app项目多端部署)]()
教程学习可能遇到的问题答疑（非技术型）：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[黑马程序员学习常见问题答疑]()

2021-12-27 15:04**839**回复

共103条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

黑马前端

pink账号学习路线：
\1. H5C3+移动布局 ![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程]()
\2. [JavaScript]()**系列 ![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续]()

2020-09-04 15:14**1590**回复

![img](https://i1.hdslb.com/bfs/face/798c5b85e849b8b37da772589b8362a16f554580.jpg@160w_160h_1c_1s.webp)

帅气的蠢脸

推荐最新 高口碑的2022年web前端教程：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[求知讲堂web前端 96天完整版 学完可就业]()

2023-01-05 15:28

**11

**

回复

**

共176条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/168bc915f4b5cb809088e2942b57dc594a568476.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

太空浪子1900

变量：P11～19
数据类型：P20～40
运算符：P41～54
流程控制分支结构：P55～68
循环：P69～95
数组：P96～112
函数：P113～133
作用域：P134～139
JS预解析：P140～142
对象：P143～153
内置对象：P155～186
简单数据类型和复杂数据类型：P187～190
DOM：P194～265
事件高级：P247～265
BOM：P266～286
PC端网页特效：P287～329
移动端网页特效：P331～353
本地存储：P354～357
jQuery：P358～[442]()**
数据可视化：P443～473

2021-10-20 15:34**2464**回复

![img](https://i2.hdslb.com/bfs/face/066d7fb216ffaad2ef3ba468d3873272367eea0d.jpg@160w_160h_1c_1s.webp)

小杨苏西138

![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[2023年最新前端零基础入门资料(资料+视频+训练项目）]()

4小时前

**5

**

回复

**

共107条回复, 点击查看

![img](https://i0.hdslb.com/bfs/face/aaccce8d0a9a3a2d915d2fcdb00be7943bcfafaa.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

aaaaaaabbbccooo

pink圈

1

[Pink老师]()**，我们全寝都看你的视频！

2020-09-01 21:09**455**回复

热评

UP主觉得很赞

![img](https://i0.hdslb.com/bfs/face/3263a42a11d6156d22e4baebfdca44aeb19e257e.jpg@160w_160h_1c_1s.webp)

我以灬不为

这套课程哪里是讲es6的？

2022-11-18 10:19

**5

**

回复

**

共25条回复, 点击查看

![img](https://i0.hdslb.com/bfs/face/7328c2ceff43106b77803137647e243af218ea07.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

Candy_leee

从今年三月开始，跟随pink老师学习到现在，今天把B站pink老师更新的所有视频看完了，回顾这一路上的坚持，很感谢自己也很感谢pink老师，从最初的标签，到后面的样式，以及js，pink老师讲的都十分细腻，后面还有许多东西需要学习，[node]()**，ajax，vue等框架，相信自己，坚持就是胜利，再次感谢pink老师，愿大家都能在学习的过程中找到自己的方向，实现自己的梦想！![[惊喜]](https://i0.hdslb.com/bfs/emote/0afecaf3a3499479af946f29749e1a6c285b6f65.png@24w_24h.webp)

2021-06-02 16:48**710**回复

热评

UP主觉得很赞

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

黑马前端

真棒哈~~  不过刚更新了js，记得随时去看看有没有更新哈

2021-06-02 16:53

**52

**

回复

**

![img](https://i0.hdslb.com/bfs/face/7328c2ceff43106b77803137647e243af218ea07.jpg@160w_160h_1c_1s.webp)

Candy_leee

回复 @黑马程序员pink老师 :好的pink老师![[给心心]](https://i0.hdslb.com/bfs/emote/1597302b98827463f5b75c7cac1f29ea6ce572c4.png@24w_24h.webp)，受宠若惊哈哈，现在还在学习jQuery，先问一下以后jQuery的运用还多吗

2021-06-02 16:59

**20

**

回复

**

共68条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

黑马前端

小伙伴们，里面包含 视频，源码笔记甚至作业哦，你们懂得，该一键三连啦，这样可以提高视频的排名，可以让更多的人看到这个视频哈~~ 还是那句话，[pink老师]()**还能火一把吗？？

2020-09-01 18:24**1972**回复

![img](https://i1.hdslb.com/bfs/face/5096f966bd4c087089f23dd9a7c1f6f1b5fe2065.jpg@160w_160h_1c_1s.webp)

放剁椒的麻辣小龙虾

感谢

2021-05-17 14:23

**

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

账号已注销

梦开始的地方![[吃瓜]](https://i0.hdslb.com/bfs/emote/4191ce3c44c2b3df8fd97c33f85d3ab15f4f3c84.png@24w_24h.webp)

2021-06-02 10:00

**

**

回复

**

![img](https://i0.hdslb.com/bfs/face/1151fa7251c378b9d36f491ad2062d4b78404192.jpg@160w_160h_1c_1s.webp)

Warmgzy

感谢pink老师，受益匪浅

2021-08-04 14:42

**11

**

回复

**

共135条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/8eaba7b514a10293c791149b6ee5ab54f379a9d6.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

烟掩嫣颜淹眼檐

兄弟们我找了好久终于找到后续啦：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员JavaScript核心教程，前端基础教程，JS的DOM BOM操作教程]() 接71p
然后可以去看看ES6的教程：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[2019全新javaScript进阶面向对象ES6]()

2020-11-07 00:51**866**回复

![img](https://i0.hdslb.com/bfs/face/55fdec9ef1fb4d2fc32a3082decb59cccda4f4cb.jpg@160w_160h_1c_1s.webp)

DayDayON99

今天是2021年2月24日，年十三，祝大家新年快乐，身体健康，早日找到心仪的工作。
到今日为止，pink老师本系列更新到第328集。接下去的内容在![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员JavaScript核心教程，前端基础教程，JS的DOM BOM操作教程]() 第139集开始。
顶我上去啊~~~![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)

2021-02-24 17:33

**113

**

回复

**

![img](https://i0.hdslb.com/bfs/face/2fc5e388c6fbf34ad1ece7e64929f97f1ac5eacd.jpg@160w_160h_1c_1s.webp)

小林小林小林丶

插

2022-05-29 17:46

**11

**

回复

**

![img](https://i1.hdslb.com/bfs/face/39cbf4ff394df4801d13b2cc40f8c79ba3a13d8e.jpg@160w_160h_1c_1s.webp)

梭_影

cy

2022-06-01 23:07

**9

**

回复

**

共84条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/4a21617295f8c3ead4b64fe8c8e0e27ebf5d15f8.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

学呢

笔记

一、JavaScript简介(JS)1、JS概述	1、JavaScript是现阶段最主流的编程语言之一，是一种运行在客服端(浏览器)的脚本语言，同时也... 展开 

2022-10-20**86**回复

![img](https://i0.hdslb.com/bfs/face/23dd230aa0ad2bde480517d20f42bceea046cb3b.jpg@160w_160h_1c_1s.webp)

沙漠之花的

好银，这些

2022-11-06 22:33

**2

**

回复

**

![img](https://i2.hdslb.com/bfs/face/b863304fc9c244b53d32bb98ae95a43b45cc3547.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

bili-首席管理员

JS结束！Pink老师yyds
JavaScript基础大总结(一)：https://blog.csdn.net/Augenstern_QXL/article/details/119249534
JavaScript基础之函数与作用域(二)：https://blog.csdn.net/Augenstern_QXL/article/details/119250991
JavaScript基础之对象与内置对象(三)：https://blog.csdn.net/Augenstern_QXL/article/details/119250137
JavaScript进阶之[DOM]()**技术(四)：https://blog.csdn.net/Augenstern_QXL/article/details/115416921
JavaScript进阶之BOM技术(五)：https://blog.csdn.net/Augenstern_QXL/article/details/115406408
JavaScript提高之面向对象(六)：https://blog.csdn.net/Augenstern_QXL/article/details/115219073
JavaScript提高之ES6(七)：https://blog.csdn.net/Augenstern_QXL/article/details/115344398

2021-08-03 20:38**262**回复

![img](https://i1.hdslb.com/bfs/face/7e846fe040fc5af61f1779c43402680ce3ebffa9.jpg@160w_160h_1c_1s.webp)

谁尚能饭否

大佬好强
你的csdn让我膜拜

2022-01-05 15:36

**12

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

WileyWon

在

2022-08-07 14:34

**7

**

回复

**

共11条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/1a696e914fbe3c6fb3e0eecd35b64127a1c49bc7.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

七喜紅茶

今年二月份到现今，在B站与pink老师相伴快一百多个小时，html到js再到jq，收获颇丰。敲了很多感谢词，想来又不合适，或许在旁人看来过于矫情。反复修改之后。我最想说的是一句“老师，谢谢您！”

2021-05-30 20:42**262**回复

UP主觉得很赞

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

黑马前端

看到你的留言暖暖的

2021-05-30 23:51

**59

**

回复

**

共15条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/2243a5175bd92b370f5a1fb7b2b3e933f49c2078.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

Best_08

// A T M 
​        var money = 100;
​        var price = 0;
​        while (num != 4) {
​            var num = [prompt]()**('请输入你要的操作:\n1.存钱\n2.取钱\n3.显示余额\n4.退出')
​            switch (num) {
​                case '1':
​                    price = prompt('输入要存的钱数；');
​                    money = money + parseFloat(price);
​                    alert('您的余额；' + money);
​                    continue;
​                case '2':
​                    price = prompt('输入你要取出的钱: ');
​                    money = money - parseFloat(price);
​                    alert('您的余额' + money);
​                    continue;
​                case '3':
​                    alert('您的余额：' + money);
​                    continue;
​                case '4':
​                    alert('正在退出...')
​                    break;
​            }
P 95 ATM 作业。

2021-01-26 17:37**147**回复

![img](https://i0.hdslb.com/bfs/face/135dd693c422659ad293a42c62fb00680518bbae.jpg@160w_160h_1c_1s.webp)

丶Jns

是不是可以取钱取成负数

2021-07-18 23:32

**10

**

回复

**

![img](https://i2.hdslb.com/bfs/face/325d4e1c87566b947cc36dfe004555df4f65efbf.jpg@160w_160h_1c_1s.webp)

那年メ

回复 [@丶Jns]() :  var monye = 100;
​        //计数
​        var count = 0;
​        while (num != 4) {
​            var num = prompt('请输入你要的操作: \n1.存钱\n2.取钱\n3.显示余额\n4.退出')
​            switch (num) {
​                case '1':
​                    count = prompt('你要纯多少钱')
​                    monye += parseFloat(count)
​                    alert('你的余额为' + monye)
​                    continue
​                case '2':
​                    count = prompt('你要取多少钱')
​                    if (count > monye) {
​                        alert('对不起当前你的余额不足')
​                    } else {
​                        monye -= parseFloat(count)
​                    }
​                    alert('你的余额为' + monye)
​                    continue
​                case '3':
​                    alert('当前你的余额剩余' + monye)
​                    continue
​                case '4':
​                    alert('退出成功')
​                    break;
​                default:
​                    alert('没有此操作')
​            }
​        }

2021-10-16 23:33

**29

**

回复

**

共36条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/d27799455e4b10c0397efc7f8fd65276f9da477a.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

西巴西巴p

我们线下经常看到pink老师呦

2020-09-03 00:14**181**回复

热评

UP主觉得很赞

![img](https://i1.hdslb.com/bfs/face/61446c17b10d99636ab0463125a4921f4c2dff27.jpg@160w_160h_1c_1s.webp)

minecraft_-

帅？

2021-09-10 07:03

**7

**

回复

**

![img](https://i1.hdslb.com/bfs/face/fa48ac10818c4519a3733ba82e3ccc7118281d04.jpg@160w_160h_1c_1s.webp)

清风雅雨

pink老师在哪里人呀？

2021-12-09 14:33

**11

**

回复

**

![img](https://i1.hdslb.com/bfs/face/0b21b2693434264de9df96c023a94ba397fd0da4.jpg@160w_160h_1c_1s.webp)

B站小王o

回复 [@清风雅雨]() :武汉

2022-01-24 17:09

**10

**

回复

**

共10条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/ca639d37ad807f049f6c9005056167283232946b.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

100KCAL

虽然[黑马程序]()**员有，但就是想来pink老师这里看

2020-09-14 05:54**163**回复

UP主觉得很赞

![img](https://i2.hdslb.com/bfs/face/ca639d37ad807f049f6c9005056167283232946b.jpg@160w_160h_1c_1s.webp)

100KCAL

别忘了点赞，投币

2020-09-14 05:55

**26

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

Goencc

回复 [@100KCAL]() :阿噗主觉得很淦

2021-04-28 14:35

**12

**

回复

**

![img](https://i0.hdslb.com/bfs/face/2dec25896ef4a3f22ae4bf61a1b0a64ecb12aa0f.jpg@160w_160h_1c_1s.webp)

Polarisss----

请问数据可视化那部分是不是不完全呢

2022-01-05 21:21

**8

**

回复

**

共10条回复, 点击查看

![img](https://i0.hdslb.com/bfs/face/d20e15f14148cebc6d60af8496ae0d29d2c761cd.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

奇葩小白羊

125作业计算器
function getResult([num]()**1, sign, num2) {
​            var result;
​            while (true) {
​                switch (sign) {
​                    case '+':
​                        result = num1 + num2;
​                        return result;
​                    case '-':
​                        result = num1 - num2;
​                        return result;
​                    case '*':
​                        result = num1 * num2;
​                        return result;
​                    case '/':
​                        result = num1 / num2;
​                        return result;
​                    default:
​                        alert('输入有误，请重新输入！')
​                        return result;
​                }
​            }
​        }
​        var re = getResult(parseFloat(prompt('请输入数字：')), prompt('请输入操作符：'), parseFloat(prompt('请输入数字：')));
​        console.log(re);

2021-01-30 14:06**104**回复

![img](https://i0.hdslb.com/bfs/face/f08dbd64aebad299246e918a36bc8e36544e9339.jpg@160w_160h_1c_1s.webp)

annnez

这个不是P154的吗，不过为什么这个封装函数的作业会放在这里。。。

2021-04-19 15:13

**10

**

回复

**

![img](https://i0.hdslb.com/bfs/face/518213cc130761a6f3fd4b9752d2a5236ec312a3.jpg@160w_160h_1c_1s.webp)

LilllHumBro

补充一下，case后面的运算符应该加引号包含，不然的话数据类型和switch里面的不一样，运行不了，我也是想了好一会才解决的![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)希望对大家有帮助

2021-09-16 16:54

**9

**

回复

**

![img](https://i0.hdslb.com/bfs/face/518213cc130761a6f3fd4b9752d2a5236ec312a3.jpg@160w_160h_1c_1s.webp)

LilllHumBro

回复 @LilllHumBro :可能是我太菜了，想了很久才发现问题，求轻喷![[doge]](https://i0.hdslb.com/bfs/emote/3087d273a78ccaff4bb1e9972e2ba2a7583c9f11.png@24w_24h.webp)![[微笑]](https://i0.hdslb.com/bfs/emote/685612eadc33f6bc233776c6241813385844f182.png@24w_24h.webp)

2021-09-16 16:56

**8

**

回复

**

共11条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/7622fe500d64cac1ba2b7311a25ef904d2311551.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

垰萨

变量：P11～19
数据类型：P20～40
运算符：[P41]()**～54
流程控制分支结构：P55～68
循环：P69～95
数组：P96～112
函数：P113～133
作用域：P134～139
JS预解析：P140～142
对象：P143～153
内置对象：P155～186
简单数据类型和复杂数据类型：P187～190
DOM：P194～265
事件高级：P247～265
BOM：P266～286
PC端网页特效：P287～329
移动端网页特效：P331～353
本地存储：P354～357
jQuery：P358～442
数据可视化：P443～473

2021-12-21 10:10**63**回复

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

酷酷的琪67

大哥，这里面应该学哪些内容？

2022-05-22 19:30

**6

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

不吃土豆粉吃土豆

回复 [@酷酷的琪67]() :除了jQuery都得学啊

2022-05-23 16:59

**6

**

回复

**

共6条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/405a0d641f57713928303147ddcb8d4db17b3e2d.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

南枝向北

跪求pink老师的vue视频，硬币三连已经饥渴难耐了![[保佑]](https://i0.hdslb.com/bfs/emote/fafe8d3de0dc139ebe995491d2dac458a865fb30.png@24w_24h.webp)

2020-09-11 11:03**200**回复

![img](https://i1.hdslb.com/bfs/face/8328f9435c7ffa49c7672ba7e68909066708b9cf.jpg@160w_160h_1c_1s.webp)

粉色程序员

尚硅谷刘天宇Vue可以去看看，绝对是全站最好的Vue

2022-01-16 16:00

**12

**

回复

**

![img](https://i0.hdslb.com/bfs/face/cdd020f3fafadc89d7f92af69a6071cb11c52527.jpg@160w_160h_1c_1s.webp)

向全栈努力

回复 [@粉色程序员]() :那个打扰一下，那个人是不是可能原名叫张天禹呢

2022-02-22 10:32

**28

**

回复

**

共15条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/9017a35530592a34183871304a0e10d2d7900dd3.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

47794696794_bili

课程资料 链接：https://pan.baidu.com/s/1guj_XDKRMvk2T0Xmdfj0yw 
提取码：6nkw

2020-11-03 15:20**122**回复

![img](https://i1.hdslb.com/bfs/face/aa9d9a10b2714d8e64f22f2d5c8e5f7c2df52bce.jpg@160w_160h_1c_1s.webp)

爱学习的喜哥哥

兄弟，有API的ppt吗

2021-01-15 20:37

**18

**

回复

**

![img](https://i2.hdslb.com/bfs/face/b863304fc9c244b53d32bb98ae95a43b45cc3547.jpg@160w_160h_1c_1s.webp)

bili-首席管理员

跟着pink老师做的在线笔记文档复习使用![[doge]](https://i0.hdslb.com/bfs/emote/3087d273a78ccaff4bb1e9972e2ba2a7583c9f11.png@24w_24h.webp)
HTML部分
HTML(一)：https://blog.csdn.net/Augenstern_QXL/article/details/115419453
HTML5(二)：https://blog.csdn.net/Augenstern_QXL/article/details/115599059
\---------------------------------------------------------------------------------
CSS部分：
CSS(一)：https://blog.csdn.net/Augenstern_QXL/article/details/115560532
CSS三大特性(二)：https://blog.csdn.net/Augenstern_QXL/article/details/115560502
CSS3(三)进阶：https://blog.csdn.net/Augenstern_QXL/article/details/115726577
CSS3(四)高级：https://blog.csdn.net/Augenstern_QXL/article/details/119172527
\----------------------------------------------------------------------------------
JS部分
JavaScript基础班ES6（一）：https://blog.csdn.net/Augenstern_QXL/article/details/115219073
JavaScript基础班ES6（二）：https://blog.csdn.net/Augenstern_QXL/article/details/115344398
JavaScript之DOM(三)（一）：https://blog.csdn.net/Augenstern_QXL/article/details/115416921
JavaScript之BOM（四）：https://blog.csdn.net/Augenstern_QXL/article/details/115406408

2021-07-28 10:31

**77

**

回复

**

![img](https://i1.hdslb.com/bfs/face/a57e2fe80c0bfee7f1188eb2d2b088b5ef513585.jpg@160w_160h_1c_1s.webp)

阿阿阿吳

回复 [@爱学习的喜哥哥]() :能发我一份吗谢谢

2021-08-11 11:12

**8

**

回复

**

共22条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/1076e90f1f91bac861b40d654c9998698b94ae74.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

handsome-安卿尘

pink老师怎么不更新了

2020-10-19 21:26**47**回复

![img](https://i2.hdslb.com/bfs/face/077ab2fc52c91d11effdb4eecc31a476c8de2d74.jpg@160w_160h_1c_1s.webp)

发布

[![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@96w_96h_1c_1s.webp)](https://space.bilibili.com/415434293)

[黑马前端](https://space.bilibili.com/415434293)[** 发消息](https://message.bilibili.com/#whisper/mid415434293)

学习就要拼命克服，相信自己，必会学有所成！

为TA充电

已关注 47.3万

弹幕列表 

![img](https://i0.hdslb.com/bfs/sycp/creative_img/202203/4ba3ceca66686956cc8970a12f54af35.jpg@336w_190h_!web-video-ad-cover.webp)【挑战】每天建模一小时，副业接单养活自己！点击免费领取课程

### 视频选集

(248/473)

**

自动连播 

- [P101-计算机基础导读01:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=1)
- [P202-编程语言09:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=2)
- [P303-计算机基础09:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=3)
- [P404-JavaScript初识导读00:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=4)
- [P505-初始JavaScript07:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=5)
- [P606-浏览器执行JS过程03:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=6)
- [P707-JS三部分组成03:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=7)
- [P808-JS三种书写位置06:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=8)
- [P909-JS注释03:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=9)
- [P1010-JS输入输出语句04:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=10)
- [P1111-变量导读00:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=11)
- [P1212-什么是变量04:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=12)
- [P1313-变量的使用06:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=13)
- [P1414-变量案例03:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=14)
- [P1515-变量案例弹出用户名03:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=15)
- [P1616-变量语法扩展08:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=16)
- [P1717-变量的命名规范09:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=17)
- [P1818-交换2个变量的值07:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=18)
- [P1919-变量小结02:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=19)
- [P2020-数据类型导读00:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=20)
- [P2121-数据类型简介06:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=21)
- [P2222-数字型Number11:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=22)
- [P2323-isNaN02:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=23)
- [P2424-字符串型String07:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=24)
- [P2525-弹出网页警示框02:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=25)
- [P2626-字符串长度以及拼接07:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=26)
- [P2727-字符串拼接加强05:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=27)
- [P2828-显示年龄案例04:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=28)
- [P2929-boolean以及undefined和null07:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=29)
- [P3030-typeof检测变量数据类型05:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=30)
- [P3131-字面量02:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=31)
- [P3232-转换为字符串类型07:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=32)
- [P3333-转换为数字型parseInt和parseFloat07:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=33)
- [P3434-转换为数字型Number和隐式转换03:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=34)
- [P3535-计算年龄案例04:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=35)
- [P3636-简单加法器案例04:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=36)
- [P3737-转换为布尔型02:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=37)
- [P3838-拓展阅读之编译和解释语言的区别03:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=38)
- [P3939-拓展阅读之标识符关键字保留字02:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=39)
- [P4040-课后作业00:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=40)
- [P4101-运算符导读00:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=41)
- [P4202-算数运算符09:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=42)
- [P4303-表达式和返回值03:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=43)
- [P4404-前置递增运算符06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=44)
- [P4505-后置递增运算符03:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=45)
- [P4606-递增运算符练习05:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=46)
- [P4707-前置递增和后置递增小结03:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=47)
- [P4808-比较运算符06:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=48)
- [P4909-逻辑运算符06:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=49)
- [P5010-逻辑运算符练习02:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=50)
- [P5111-逻辑中断逻辑与06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=51)
- [P5212-逻辑中断逻辑或04:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=52)
- [P5313-赋值运算符03:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=53)
- [P5414-运算符优先级07:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=54)
- [P5515-流程控制分支结构导读00:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=55)
- [P5616-流程控制02:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=56)
- [P5717-if分支语句06:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=57)
- [P5818-进入网吧案例02:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=58)
- [P5919-ifelse双分支语句06:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=59)
- [P6020-判断闰年案例06:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=60)
- [P6121-if else if多分支语句07:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=61)
- [P6222-判断成绩案例08:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=62)
- [P6323-三元表达式05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=63)
- [P6424-数字补0案例05:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=64)
- [P6525-switch语句09:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=65)
- [P6626-switch 注意事项05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=66)
- [P6727-查询水果案例04:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=67)
- [P6828-switch和ifelseif 区别05:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=68)
- [P6901-循环导读01:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=69)
- [P7002-循环的目的03:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=70)
- [P7103-for循环语法结构08:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=71)
- [P7204-for循环执行过程06:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=72)
- [P7305-断点调试06:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=73)
- [P7406-for循环重复执行相同代码02:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=74)
- [P7507-for循环重复执行不同代码04:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=75)
- [P7608-for循环重复某些操作05:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=76)
- [P7709-for循环案例07:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=77)
- [P7810-求学生成绩案例（上）06:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=78)
- [P7911-求学生成绩案例（下）05:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=79)
- [P8012-一行打印五颗星星05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=80)
- [P8113-双重for循环执行过程07:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=81)
- [P8214-打印5行5列的星星04:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=82)
- [P8315-打印n行n列的星星02:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=83)
- [P8416-打印倒三角形案例06:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=84)
- [P8517-九九乘法表09:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=85)
- [P8618-for循环小结02:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=86)
- [P8718-while循环06:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=87)
- [P8819-while案例05:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=88)
- [P8920-do while循环04:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=89)
- [P9021-do while案例04:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=90)
- [P9122-循环小结01:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=91)
- [P9223-continue关键字06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=92)
- [P9324-break关键字02:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=93)
- [P9425-命名规范以及语法格式02:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=94)
- [P9526-循环作业02:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=95)
- [P9601-数组导读00:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=96)
- [P9702-什么是数组以及创建方式08:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=97)
- [P9803-访问数组元素06:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=98)
- [P9904-遍历数组05:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=99)
- [P10005-数组长度03:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=100)
- [P10106-计算数组的和以及平均值06:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=101)
- [P10207-求数组中的最大值06:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=102)
- [P10308-数组转换为字符串04:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=103)
- [P10409-数组新增元素07:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=104)
- [P10510-数组存放1~10个值04:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=105)
- [P10611-筛选数组方法106:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=106)
- [P10712-筛选数组方法204:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=107)
- [P10813-删除数组指定元素(数组去重）03:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=108)
- [P10914-翻转数组06:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=109)
- [P11015-复习交换两个变量值02:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=110)
- [P11116-冒泡排序原理04:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=111)
- [P11217-冒泡排序12:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=112)
- [P11318-函数导读00:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=113)
- [P11419-为什么需要函数05:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=114)
- [P11520-函数的使用05:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=115)
- [P11621-利用函数求1~100累加和02:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=116)
- [P11722-函数的参数08:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=117)
- [P11823-利用函数求任意两个数的和以及累加和04:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=118)
- [P11924-函数形参和实参匹配问题06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=119)
- [P12025-函数的返回值return08:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=120)
- [P12126-利用函数求两个数的最大值02:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=121)
- [P12227-利用函数求数组中的最大值05:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=122)
- [P12328-return终止函数并且只能返回一个值06:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=123)
- [P12429-函数返回值2个注意事项02:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=124)
- [P12530-通过榨汁机看透函数02:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=125)
- [P12601-arguments使用08:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=126)
- [P12702-利用函数求任意个数的最大值02:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=127)
- [P12803-利用函数翻转数组03:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=128)
- [P12904-函数封装冒泡排序03:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=129)
- [P13005-利用函数判断闰年03:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=130)
- [P13106-函数可以调用另外一个函数05:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=131)
- [P13207-输出2月份天数06:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=132)
- [P13308-函数的两种声明方式05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=133)
- [P13409-作用域导读00:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=134)
- [P13510-JavaScript作用域07:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=135)
- [P13611-全局变量和局部变量07:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=136)
- [P13712-JavaScript没有块级作用域就02:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=137)
- [P13813-作用域链04:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=138)
- [P13914-作用域链案例05:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=139)
- [P14015-JavaScript预解析导读00:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=140)
- [P14116-预解析13:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=141)
- [P14217-预解析案例12:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=142)
- [P14318-对象导读00:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=143)
- [P14419-什么是对象以及为什么需要对象07:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=144)
- [P14520-利用对象字面量创建对象10:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=145)
- [P14621-变量属性函数方法的区别05:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=146)
- [P14722-利用new Object创建对象04:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=147)
- [P14823-我们为什么需要构造函数04:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=148)
- [P14924-构造函数创建对象（上）10:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=149)
- [P15025-构造函数创建对象（下）05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=150)
- [P15126-构造函数和对象区别03:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=151)
- [P15227-new关键字执行过程03:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=152)
- [P15328-遍历对象05:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=153)
- [P15429-小结和作业01:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=154)
- [P15501-内置对象导读01:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=155)
- [P15602-什么是内置对象03:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=156)
- [P15703-学会查阅MDN文档06:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=157)
- [P15804-数学对象Math最大值方法06:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=158)
- [P15905-封装自己的数学对象04:41](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=159)
- [P16006-Math绝对值和三个取整方法07:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=160)
- [P16107-Math随机数方法10:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=161)
- [P16208-猜数字游戏06:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=162)
- [P16309-Date日期对象的使用08:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=163)
- [P16410-格式化日期年月日星期10:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=164)
- [P16511-格式化日期时分秒06:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=165)
- [P16612-Date总的毫秒数（时间戳）06:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=166)
- [P16713-倒计时（上）07:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=167)
- [P16814-倒计时（下）05:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=168)
- [P16915-数组创建的两种方式04:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=169)
- [P17016-检测是否为数组两种方式06:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=170)
- [P17117-添加数组元素06:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=171)
- [P17218-删除数组元素03:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=172)
- [P17319-筛选数组02:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=173)
- [P17420-数组排序（放到冒泡排序之后讲解）05:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=174)
- [P17521-获取数组元素索引05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=175)
- [P17622-数组去重案例07:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=176)
- [P17723-数组转换为字符串03:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=177)
- [P17824-基本包装类型04:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=178)
- [P17925-字符串不可变04:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=179)
- [P18026-根据字符返回位置03:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=180)
- [P18127-求某个字符出现的位置以及次数06:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=181)
- [P18228-根据位置返回字符04:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=182)
- [P18329-统计出现次数最多的字符（上）09:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=183)
- [P18430-统计出现次数最多的字符（下）03:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=184)
- [P18531-拼接以及截取字符串03:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=185)
- [P18632-替换字符串以及转换为数组06:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=186)
- [P18733-简单数据类型和复杂数据类型导读00:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=187)
- [P18834-数据类型内存分配08:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=188)
- [P18935-简单数据类型传参03:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=189)
- [P19036-复杂数据类型传参05:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=190)
- [P19101-Web APIs简介导读00:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=191)
- [P19202-js基础和Web APIs两个阶段的关联性03:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=192)
- [P19303-API 和 Web API05:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=193)
- [P19404-DOM导读01:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=194)
- [P19505-DOM简介04:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=195)
- [P19606-getElementById获取元素08:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=196)
- [P19707-getElementsByTagName获取某类标签元素11:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=197)
- [P19808-H5新增获取元素方式08:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=198)
- [P19909-获取body和html元素02:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=199)
- [P20010-事件三要素06:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=200)
- [P20111-执行事件过程04:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=201)
- [P20212-操作元素-修改元素内容08:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=202)
- [P20313-innerText和innerHTML的区别06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=203)
- [P20414-操作元素-修改元素属性05:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=204)
- [P20515-分时问候案例06:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=205)
- [P20616-操作元素-修改表单属性06:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=206)
- [P20717-仿京东显示隐藏密码明文案例（上）07:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=207)
- [P20818-仿京东显示隐藏密码明文案例（下）08:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=208)
- [P20919-操作元素-修改样式属性05:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=209)
- [P21020-仿淘宝关闭二维码案例05:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=210)
- [P21121-循环精灵图08:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=211)
- [P21222-显示隐藏文本框内容10:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=212)
- [P21323-使用className修改样式属性09:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=213)
- [P21424-密码框验证信息09:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=214)
- [P21525-操作元素总结以及作业03:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=215)
- [P21601-排他思想（算法）09:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=216)
- [P21702-百度换肤效果08:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=217)
- [P21803-表格隔行变色效果07:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=218)
- [P21904-表单全选取消全选（上）07:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=219)
- [P22005-表单全选取消全选（下）09:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=220)
- [P22106-获取自定义属性值05:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=221)
- [P22207-设置移除自定义属性04:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=222)
- [P22308-tab栏切换布局分析（重要）04:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=223)
- [P22409-tab栏切换制作（上）04:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=224)
- [P22510-tab栏切换制作（下）09:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=225)
- [P22611-H5自定义属性10:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=226)
- [P22712-为什么学习节点操作以及节点简介07:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=227)
- [P22813-节点操作之父节点04:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=228)
- [P22914-节点操作之子节点06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=229)
- [P23015-节点操作之第一个子元素和最后一个子元素06:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=230)
- [P23116-新浪下拉菜单06:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=231)
- [P23217-节点操作之兄弟节点05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=232)
- [P23318-节点操作之创建和添加节点08:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=233)
- [P23419-简单版发布留言案例08:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=234)
- [P23501-节点操作-删除节点05:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=235)
- [P23602-删除留言案例08:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=236)
- [P23703-节点操作-复制节点04:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=237)
- [P23804-动态生成表格-创建学生数据05:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=238)
- [P23905-动态生成表格-创建行03:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=239)
- [P24006-动态生成表格-创建单元格05:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=240)
- [P24107-动态生成表格-单元格填充数据03:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=241)
- [P24208-动态生成表格-创建删除单元格03:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=242)
- [P24309-动态生成表格-添加删除操作04:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=243)
- [P24410-document.write创建元素（了解）04:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=244)
- [P24511-innerHTML和createElement效率对比07:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=245)
- [P24612-DOM重点核心06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=246)
- [P24713-事件高级导读01:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=247)
- [![img](https://s1.hdslb.com/bfs/static/jinkela/video/asserts/playing.gif)P24814-注册事件两种方式08:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248)
- [P24915-attachEvent注册事件05:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=249)
- [P25016-删除事件08:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=250)
- [P25117-DOM事件流理论04:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=251)
- [P25218-DOM事件流代码验证07:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=252)
- [P25319-什么是事件对象08:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=253)
- [P25420-e.target和this区别08:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=254)
- [P25521-阻止默认行为06:35](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=255)
- [P25622-阻止事件冒泡04:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=256)
- [P25723-事件委托06:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=257)
- [P25824-禁止选中文字和禁止右键菜单04:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=258)
- [P25925-获得鼠标在页面中的坐标07:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=259)
- [P26026-跟随鼠标的天使07:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=260)
- [P26101-常用的键盘事件06:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=261)
- [P26202-keyCode判断用户按下哪个键07:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=262)
- [P26303-模拟京东按键输入内容案例05:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=263)
- [P26404-模拟京东快递单号查询（上）07:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=264)
- [P26505-模拟京东快递单号查询（下）06:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=265)
- [P26606-BOM导读00:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=266)
- [P26707-BOM概述08:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=267)
- [P26809-页面加载事件08:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=268)
- [P26910-调整窗口大小事件05:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=269)
- [P27011-定时器之setTimeout07:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=270)
- [P27112-回调函数以及5秒之后自动关闭的广告04:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=271)
- [P27213-清除定时器clearTimeout03:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=272)
- [P27314-定时器之setInterval03:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=273)
- [P27415-倒计时效果08:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=274)
- [P27516-清除定时器clearInterval04:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=275)
- [P27617-发送短信案例07:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=276)
- [P27718-this指向问题07:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=277)
- [P27819-js 同步和异步04:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=278)
- [P27920-同步任务和异步任务执行过程06:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=279)
- [P28021-js执行机制06:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=280)
- [P28122-location对象常见属性06:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=281)
- [P28223-5秒钟之后跳转页面06:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=282)
- [P28324-获取URL参数11:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=283)
- [P28425-location常见方法04:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=284)
- [P28526-navigator对象04:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=285)
- [P28627-history对象04:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=286)
- [P28701-PC端网页特效导读00:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=287)
- [P28802-offsetLeft和offsetTop获取元素偏移04:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=288)
- [P28903-offsetWidth和offsetHeight获取元素大小05:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=289)
- [P29004-offset与style区别03:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=290)
- [P29105-获取鼠标在盒子内的坐标06:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=291)
- [P29206-拖动模态框（上）06:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=292)
- [P29307-拖动模态框（中）09:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=293)
- [P29408-拖动模态框（下）02:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=294)
- [P29509-仿京东放大镜效果页面结构搭建06:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=295)
- [P29610-仿京东放大镜效果显示隐藏遮挡层和大盒子05:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=296)
- [P29711-仿京东放大镜效果遮挡层跟随鼠标08:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=297)
- [P29812-仿京东放大镜效果限制遮挡层移动范围07:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=298)
- [P29913-仿京东放大镜效果大图片移动08:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=299)
- [P30014-client系列02:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=300)
- [P30115-立即执行函数08:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=301)
- [P30216-淘宝flexibleJS源码分析之核心原理07:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=302)
- [P30317-淘宝flexibleJS源码分析之pageshow事件07:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=303)
- [P30418-scroll系列05:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=304)
- [P30519-仿淘宝固定侧边栏（上）08:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=305)
- [P30620-仿淘宝固定侧边栏（下）10:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=306)
- [P30721-三大系列总结01:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=307)
- [P30822-mouseover和mouseenter区别02:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=308)
- [P30923-动画原理06:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=309)
- [P31024-简单动画函数封装04:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=310)
- [P31125-动画函数-给不同元素记录不同定时器08:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=311)
- [P31201-缓动动画原理05:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=312)
- [P31302-缓动动画基本代码实现04:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=313)
- [P31403-缓动动画多个目标值之间移动07:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=314)
- [P31504-缓动动画添加回调函数05:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=315)
- [P31605-动画函数的使用08:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=316)
- [P31706-网页轮播图-结构搭建06:41](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=317)
- [P31807-网页轮播图-鼠标经过显示隐藏左右按钮06:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=318)
- [P31908-网页轮播图-动态生成小圆圈07:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=319)
- [P32009-网页轮播图-小圆圈排他思想03:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=320)
- [P32110-网页轮播图-点击小圆圈滚动图片09:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=321)
- [P32211-网页轮播图-右侧按钮无缝滚动11:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=322)
- [P32312-网页轮播图-克隆第一张图片03:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=323)
- [P32413-网页轮播图小圆圈跟随右侧按钮一起变化05:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=324)
- [P32514-网页轮播图-两个小bug解决方案05:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=325)
- [P32615-网页轮播图-左侧按钮功能制作07:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=326)
- [P32716-网页轮播图-自动播放功能04:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=327)
- [P32817-节流阀以及逻辑中断应用07:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=328)
- [P32918-带有动画的返回顶部10:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=329)
- [P33019-筋斗云案例10:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=330)
- [P33120-移动端网页特效导读01:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=331)
- [P33221-移动端touch触摸事件04:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=332)
- [P33322-移动端TouchEvent触摸事件对象11:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=333)
- [P33423-移动端拖动元素10:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=334)
- [P33501-移动端轮播图-结构搭建05:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=335)
- [P33602-移动端轮播图-布局分析07:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=336)
- [P33703-移动端轮播图-滚动图片08:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=337)
- [P33804-移动端轮播图-无缝滚动08:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=338)
- [P33905-classList类名操作08:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=339)
- [P34006-移动端轮播图-小圆点跟随变化05:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=340)
- [P34107-移动端轮播图-手指拖动轮播图07:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=341)
- [P34208-移动端轮播图-手指滑动播放上一张下一张图片07:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=342)
- [P34309-移动端轮播图-回弹效果05:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=343)
- [P34410-返回顶部模块制作07:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=344)
- [P34511-移动端click事件300ms延时问题解决方案05:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=345)
- [P34612-fastclick插件使用06:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=346)
- [P34713-swiper插件使用-引入相关文件06:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=347)
- [P34814-移动端轮播图-按照语法规范使用07:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=348)
- [P34915-swiper插件使用-参数更改04:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=349)
- [P35016-移动端其他插件以及使用总结03:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=350)
- [P35117-视频插件zy.media.js的使用07:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=351)
- [P35218-bootstrap轮播图10:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=352)
- [P35319-阿里百秀轮播图制作09:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=353)
- [P35420-本地存储导读00:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=354)
- [P35521-本地存储之sessionStorage11:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=355)
- [P35622-本地存储之localStorage05:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=356)
- [P35723-记住用户名案例05:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=357)
- [P35801-jQuery入门导读00:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=358)
- [P35902-JavaScript库03:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=359)
- [P36003-jQuery概述03:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=360)
- [P36104-jQuery基本使用-入口函数07:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=361)
- [P36205-jQuery顶级对象$03:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=362)
- [P36306-DOM对象和jQuery对象05:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=363)
- [P36407-DOM对象和jQuery对象相互转换06:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=364)
- [P36508-jQuery常用API导读01:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=365)
- [P36609-jQuery基本和层级选择器04:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=366)
- [P36710-jQuery隐式迭代05:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=367)
- [P36811-jQuery筛选选择器03:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=368)
- [P36912-jQuery筛选方法-选取父子元素05:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=369)
- [P37013-新浪下拉菜单05:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=370)
- [P37114-jQuery其他筛选方法07:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=371)
- [P37215-jQuery排他思想03:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=372)
- [P37316-淘宝服饰精品案例07:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=373)
- [P37417-jQuery链式编程07:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=374)
- [P37518-jQuery修改样式css方法06:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=375)
- [P37619-jQuery修改样式操作类05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=376)
- [P37720-tab栏切换案例07:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=377)
- [P37821-jQuery类操作和className区别02:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=378)
- [P37922-jQuery显示与隐藏效果08:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=379)
- [P38023-jQuery滑动效果以及事件切换08:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=380)
- [P38124-jQuery停止动画排队stop03:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=381)
- [P38225-jQuery淡入淡出以及突出显示案例07:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=382)
- [P38326-jQuery自定义动画animate方法03:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=383)
- [P38427-王者荣耀手风琴案例布局分析03:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=384)
- [P38528-王者荣耀手风琴案例制作08:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=385)
- [P38601-jQuery属性操作10:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=386)
- [P38702-购物车模块-全选（上）09:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=387)
- [P38803-购物车模块-全选（下）06:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=388)
- [P38904-jQuery内容文本值04:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=389)
- [P39005-购物车模块-增减商品数量07:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=390)
- [P39106-购物车模块-修改商品小计（上）08:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=391)
- [P39207-购物车模块-修改商品小计（中）06:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=392)
- [P39308-购物车模块-修改商品小计（下）03:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=393)
- [P39409-jQuery遍历对象each方法09:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=394)
- [P39510-jQuery遍历数据$.each03:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=395)
- [P39611-购物车模块-计算总件数和总额09:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=396)
- [P39712-创建、添加、删除元素08:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=397)
- [P39813-购物车模块-清理购物车07:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=398)
- [P39914-购物车模块-选中商品添加背景颜色04:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=399)
- [P40015-jQuery尺寸方法04:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=400)
- [P40116-jQuery位置方法06:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=401)
- [P40217-jQuery被卷去头部方法06:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=402)
- [P40318-带有动画的返回顶部03:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=403)
- [P40419-电梯导航案例-显示隐藏电梯导航04:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=404)
- [P40520-电梯导航案例-点击滚动目标位置08:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=405)
- [P40621-电梯导航案例-点击当前li添加current类03:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=406)
- [P40722-电梯导航案例-滑动页面电梯导航自动添加current类05:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=407)
- [P40823-电梯导航案例节流阀(互斥锁)06:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=408)
- [P40901-jQuery事件导读00:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=409)
- [P41002-事件处理on绑定一个或者多个事件06:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=410)
- [P41103-on实现事件委派和给动态元素绑定事件06:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=411)
- [P41204-微博发布案例10:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=412)
- [P41305-off解绑事件05:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=413)
- [P41406-jQuery自动触发事件05:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=414)
- [P41507-jQuery事件对象02:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=415)
- [P41608-jQuery其他方法导读00:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=416)
- [P41709-jQuery对象拷贝extend（选放）11:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=417)
- [P41810-jQuery多库共存05:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=418)
- [P41911-瀑布流插件使用09:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=419)
- [P42012-图片懒加载技术10:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=420)
- [P42113-全屏滚动插件使用（选放）11:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=421)
- [P42214-bootstrap组件05:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=422)
- [P42315-bootstrapJS插件10:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=423)
- [P42416-阿里百秀10:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=424)
- [P42517-todolist布局功能需求分析06:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=425)
- [P42618-todolist核心思路以及本地存储格式10:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=426)
- [P42719-todolist按下回车读取本地存储数据08:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=427)
- [P42820-todolist按下回车保存最新数据到本地存储06:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=428)
- [P42921-todolist本地存储数据渲染加载到页面中10:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=429)
- [P43022-todolist点击删除按钮获取当前索引号08:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=430)
- [P43123-todolist点击删除按钮完成删除操作04:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=431)
- [P43224-点击复选框修改相应数据done属性08:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=432)
- [P43325-todolist正在进行和已经完成事项制作05:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=433)
- [P43426-todolist统计正在进行和已经完成事项个数05:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=434)
- [P43501-录制视频作用介绍01:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=435)
- [P43602-点位区域布局样式10:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=436)
- [P43703-地图区域布局样式06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=437)
- [P43804-用户区域布局样式07:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=438)
- [P43905-订单区域布局样式08:41](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=439)
- [P44006-销售区域布局样式11:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=440)
- [P44107-渠道与季度布局样式22:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=441)
- [P44208-排行区域布局样式-参考32:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=442)
- [P44301-数据可视化项目导读01:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=443)
- [P44402-什么是数据可视化05:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=444)
- [P44503-数据可视化项目概述04:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=445)
- [P44604-ECharts简介04:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=446)
- [P44705-ECharts基本使用11:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=447)
- [P44806-选择不同类型图表05:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=448)
- [P44907-ECharts相关配置（上）10:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=449)
- [P45008-ECharts-grid配置08:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=450)
- [P45109-ECharts相关配置（中）10:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=451)
- [P45210-ECharts相关配置（下）series11:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=452)
- [P45311-折线图生成以及配置项总结05:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=453)
- [P45412-数据可视化项目适配方案分析05:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=454)
- [P45513-数据可视化项目适配方案08:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=455)
- [P45614-项目准备以及按照自动刷新浏览器插件04:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=456)
- [P45715-可视化项目-body和viewport制作09:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=457)
- [P45816-可视化项目column列容器03:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=458)
- [P45917-边框图片使用场景以及切割原理08:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=459)
- [P46018-边框图片使用语法09:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=460)
- [P46119-公共面板样式制作（上）08:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=461)
- [P46220-公共面板样式制作（下）09:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=462)
- [P46321-通过类名调用字体图标06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=463)
- [P46422-数据可视化项目-概览区域模块制作12:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=464)
- [P46523-数据可视化项目-监控区域布局分析05:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=465)
- [P46624-数据可视化项目-监控区域tab栏切换分析11:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=466)
- [P46725-数据可视化项目-监控区域无缝滚动11:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=467)
- [P46801-点位分布point模块-布局05:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=468)
- [P46902-点位分布point-引入图表08:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=469)
- [P47003-ECharts饼形图-tooltip参数含义08:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=470)
- [P47104-ECharts饼形图-series参数含义06:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=471)
- [P47205-点位分布模块-定制配置(上)06:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=472)
- [P47306-点位分布模块-定制配置(下)07:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=473)

![审美佳，技术强，脾气好，是哪个程序员这么宝藏？](https://i0.hdslb.com/bfs/feed-admin/276af9a950a93889be31c698a8fdfd5add8b2b82.jpg@336w_190h_!web-video-rcmd-cover.webp)

审美佳，技术强，脾气好，是哪个程序员这么宝藏？

bilibili课堂

[![【血泪建议】自学前端越早知道越好的事情!](https://i1.hdslb.com/bfs/archive/1845e6f24b6a0547fad96de181b45fa323bcd25b.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1WF41137fe/?spm_id_from=333.788.recommend_more_video.0)

01:55

【血泪建议】自学前端越早知道越好的事情!

[2次元诺诺](https://space.bilibili.com/1837989886/)

2.7万165

[![黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程](https://i2.hdslb.com/bfs/archive/8a334edc5a07afef88d62e8c938682a03e2f695d.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV14J4114768/?spm_id_from=333.788.recommend_more_video.1)

56:03:20

黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程

[黑马前端](https://space.bilibili.com/415434293/)

1399.6万46.4万

[![前端大神尤雨溪授权的HTML+Vue+JS全套教程，整整600集，学完即可就业](https://i2.hdslb.com/bfs/archive/84f32865ed15a77f0e952ec006c106f2b5f2d600.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Ka411o7xR/?spm_id_from=333.788.recommend_more_video.2)

12:06:55

前端大神尤雨溪授权的HTML+Vue+JS全套教程，整整600集，学完即可就业

[头顶猫的美少女](https://space.bilibili.com/1807606680/)

3.3万177

[![每次我撑不下去的时候，都会打开这个视频，要是在学前端之前能知道这些就好了](https://i0.hdslb.com/bfs/archive/c52dc2c963a02e43800027cd93ad633018215673.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV16W4y1r75v/?spm_id_from=333.788.recommend_more_video.3)

02:39

每次我撑不下去的时候，都会打开这个视频，要是在学前端之前能知道这些就好了

[草莓蛋糕来了](https://space.bilibili.com/2074760195/)

6.2万158

[![【前端教程】JavaScript入门，94集完整版教程（JS核心语法 、DOM、BOM 、 ES6语法）](https://i2.hdslb.com/bfs/archive/bc771c492575a79bc58c6a54ed66e4df67fa09fd.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1bB4y1t7c5/?spm_id_from=333.788.recommend_more_video.4)

40:09:13

【前端教程】JavaScript入门，94集完整版教程（JS核心语法 、DOM、BOM 、 ES6语法）

[前端易学](https://space.bilibili.com/1663033972/)

1.0万11

[![自学前端半年，只会html、css、js、vue就找到了一份还不错的工作！](https://i0.hdslb.com/bfs/archive/a8dae1268fcbd76ca7c4d999200ab9d58f3bb597.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV15R4y1P7pR/?spm_id_from=333.788.recommend_more_video.5)

02:37

自学前端半年，只会html、css、js、vue就找到了一份还不错的工作！

[前端最后的希望](https://space.bilibili.com/1629753361/)

5.2万234

[![【2022最新版】JavaScript入门到精通全套教程（BOM_DOM_ES6_JS）](https://i0.hdslb.com/bfs/archive/1758c709e5bae9b32be814f8df7c45d18d5b5670.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV193411P76J/?spm_id_from=333.788.recommend_more_video.6)

40:35:01

【2022最新版】JavaScript入门到精通全套教程（BOM_DOM_ES6_JS）

[写网页的叮叮](https://space.bilibili.com/1712879676/)

1.8万199

[![黑马前端jquery-pink老师](https://i1.hdslb.com/bfs/archive/197612d24fc8db1a4253654ef70717ac5726b833.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1wo4y1R7t6/?spm_id_from=333.788.recommend_more_video.7)

8:06:03

黑马前端jquery-pink老师

[LaiDiang](https://space.bilibili.com/17187427/)

4.2万324

[![2022最新完整版，HTML+CSS+js教程95集完全入门达到web前端工程师水平，7天轻松搞定，堪称入门级神作](https://i2.hdslb.com/bfs/archive/e5e303009563927365c467fd08a4460a4cde6456.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Er4y1V7KA/?spm_id_from=333.788.recommend_more_video.8)

16:13:10

2022最新完整版，HTML+CSS+js教程95集完全入门达到web前端工程师水平，7天轻松搞定，堪称入门级神作

[百事可瑶_](https://space.bilibili.com/1830568085/)

7.8万989

[![前端 JavaScript基础入学从入门到精通 2023新 js教程含实战 项目 网页设计 轮播图 程序员编程新手入门必看高级完整版视频【渡一教育】](https://i2.hdslb.com/bfs/archive/3e884a22e164aa208b011faa84fefb2c34f2dcb8.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1f4411R7M5/?spm_id_from=333.788.recommend_more_video.9)

54:15:12

前端 JavaScript基础入学从入门到精通 2023新 js教程含实战 项目 网页设计 轮播图 程序员编程新手入门必看高级完整版视频【渡一教育】

[渡一教育-Web前端开发](https://space.bilibili.com/384876532/)

23.3万7526

[![推荐一个练习事件循环的网站，好    用     ！！](https://i0.hdslb.com/bfs/archive/8e9f23e57704da00f2156d24a5a465d4069e8c1b.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Zg411z7cv/?spm_id_from=333.788.recommend_more_video.10)

04:03

推荐一个练习事件循环的网站，好 用 ！！

[黑马前端](https://space.bilibili.com/415434293/)

1.5万3

[![尚硅谷JavaScript基础&实战丨JS入门到精通全套完整版](https://i2.hdslb.com/bfs/archive/41254610da8626866a1e879c8f57f59167fd2fae.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1YW411T7GX/?spm_id_from=333.788.recommend_more_video.11)

39:39:21

尚硅谷JavaScript基础&实战丨JS入门到精通全套完整版

[尚硅谷](https://space.bilibili.com/302417610/)

541.9万15.9万

[![前端学到什么程度就可以找工作了](https://i0.hdslb.com/bfs/archive/9a1688e169eb07cd11de45000812456a84dce7ae.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1xh411s71M/?spm_id_from=333.788.recommend_more_video.12)

02:09

前端学到什么程度就可以找工作了

[小鹿线前端胡老师](https://space.bilibili.com/609838079/)

13.2万84

[![当男程序员和女程序员开始交往后.....](https://i1.hdslb.com/bfs/archive/c5a404441be8fc652a71cd3b4a368baf49dc1257.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1qK4y1r713/?spm_id_from=333.788.recommend_more_video.13)

00:28

当男程序员和女程序员开始交往后.....

[佐玄先生](https://space.bilibili.com/152315179/)

514.9万419

[![2022最新版JavaScript入门到精通，前端js全套基础&实战教程](https://i0.hdslb.com/bfs/archive/0035660795e1456fae0249e8b0ab8950e8b5fc65.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Kq4y1e7d2/?spm_id_from=333.788.recommend_more_video.14)

18:15:28

2022最新版JavaScript入门到精通，前端js全套基础&实战教程

[黑马前端教程](https://space.bilibili.com/513719037/)

28.9万9099

[![这三种人，千万别学前端开发](https://i1.hdslb.com/bfs/archive/d3b617b983d6dfa8ddf2cf17c494e57eca2da438.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1P54y1k7sa/?spm_id_from=333.788.recommend_more_video.15)

06:17

这三种人，千万别学前端开发

[老尚带你学前端](https://space.bilibili.com/405768506/)

9.8万155

[![(资料私信关注)黑马前端就业班(pink老师)第二部分](https://i1.hdslb.com/bfs/archive/65e85b5ec05e159b9c9ab31e743a7e6b5b739697.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1hy4y187zi/?spm_id_from=333.788.recommend_more_video.16)

20:59:04

(资料私信关注)黑马前端就业班(pink老师)第二部分

[GrayCoder](https://space.bilibili.com/1255330937/)

1.1万7

[![【前端小技巧】纯css实现电梯导航](https://i1.hdslb.com/bfs/archive/f9c33811b591a2f822320676565ac373b0e372a0.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1YR4y1y7mk/?spm_id_from=333.788.recommend_more_video.17)

02:52

【前端小技巧】纯css实现电梯导航

[黑马前端](https://space.bilibili.com/415434293/)

3.0万15

[![黑马WEB前端PINK老师全系列JavaScript 篇](https://i0.hdslb.com/bfs/archive/f313bcc9089bc140e55ee77466d14f4a0d0194c4.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV11t4y1i7ht/?spm_id_from=333.788.recommend_more_video.18)

52:15:56

黑马WEB前端PINK老师全系列JavaScript 篇

[一朵小红花emm](https://space.bilibili.com/254046664/)

12.1万1722

[![jQuery不要学](https://i0.hdslb.com/bfs/archive/0bf17262c272b1fab233da0713c7e0ad240a2653.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1bf4y1T7Ss/?spm_id_from=333.788.recommend_more_video.19)

02:08

jQuery不要学

[沉浸式编程教学](https://space.bilibili.com/325887266/)

3.3万33

展开

![img](https://i0.hdslb.com/bfs/banner/374857eaf50a1bf7a3d56b24e2953467da50652f.png@700w_350h_!web-video-right-bottom-ad.webp)热点大放送，投稿赢奖金！

小窗

客服

顶部

![img](https://downloads.xinrern.cn/close_sqoxk.png)

![img](https://downloads.xinrern.cn/dsgdY1_dzcbt.gif)笔记详情

我的笔记

![img](https://i1.hdslb.com/bfs/face/4a21617295f8c3ead4b64fe8c8e0e27ebf5d15f8.jpg@96w_96h_1c_1s.webp)

学呢

关注

2022-10-20 19:25

10粉丝

## 一、**JavaScript简介(JS)**

### **1、JS概述**

​	1、JavaScript是现阶段最主流的编程语言之一，是一种运行在客服端(浏览器)的**脚本**语言，同时也是一种具有函数优先的轻量级，解释型或即时编译型的编程语言。

​	2、脚本语言（Script）：不需要进行编译，运行过程中由js引擎逐行来进行解释并执行。

​	3、JS也可以基于Node.js来进行服务端(后端)编程。

### 2、**浏览器执行解释JS**

浏览器分为两部分 ：渲染引擎和JS引擎

l 渲染引擎：用于解析HTML+CSS，俗称**内核**，比如chrome浏览器的blink。

l JS引擎：也称为JS解释器。用于读取网页中的JavaScript代码，对其进行处理后运行。比如chrome浏览器的V8。

浏览器通过内置的JS引擎对JS代码**逐行进行解释**编译。

### 3、**JS的组成**

l ECMAScript(JS语法)：

​	是由ECMA国际进行标准化的一门编程语言，ECMAScript规定了JS的编程语法和基础核心知识，是所有浏览器厂商共同遵守的**一套JS语法工业标准**。

l DOM(文档对象模型):

​	Document Object Model，简称DOM。是W3C组织推荐的处理可扩展置标语言的标准编程接口，通过DOM提供的接口来对页面上的各种元素进行操作(大小、位置、颜色等)。

l BOM(浏览器对象模型):

​	Browser Object Model，简称BOM。它提供了独立于内容的、可以于浏览器窗口进行互动的对象结构。通过BOM可以操作浏览器窗口，比如弹出框、控制浏览器跳转、获取分辨率等。

 

## **二、JS基础语法**

### **1、JS输入输出函数**

方法

说明

alert(msg)

浏览器弹出警示框

console.log(msg)

浏览器控制台打印输出信息

prompt(info)

浏览器弹出输入框，用户输入

(string类型)

 

### 2、**变量**

​	变量可以理解为存放数据的容器，便于操作存放在内存中的数据。

语法：

 

 

**var** 变量名

​	 

### 3、**数据类型**

​	JavaScript 是一种拥有**动态类型**的编程语言。不同于JAVA、C#这类后端语言，需要规定具体的数据类型。JavaScript 不用声明具体的数据类型，会在程序运行中被自动确定。

**值类型**

**(基本类型)**：

字符串（String）、数字(Number)、布尔(Boolean)、空（Null）、未定义（Undefined）

**引用类型**

**(对象类型):**

对象(Object)、数组(Array)、函数(Function)，还有两个特殊的对象：正则（RegExp）和日期（Date）

​	 

​	 

#### **简单数据类型**

##### **1、string(字符串)**

###### **1）、字符串转义符 \**

转义符

解释说明

\n

换行符

\\

斜杠 \

\’

‘单引号

\”

“双引号

\t

Tab 缩进

\b

空格

 

###### **2）、字符串的长度以及拼接**

**length属性**

​	用于获取字符串或数组长度

语法：

 

 

.length --返回长度

 

###### **3）、字符串拼接**

​	多个字符串之间可以使用 + 进行拼接。

​	在拼接前，会将与字符串拼接的任何类型转换为字符串，再拼接为一个新字符串。

​	注：使用字符串进行拼接时 ‘’ 引号采用就近原则进行匹配。

​	 

​	 

##### 2、**boolean(布尔型)**

布尔类型有true 和 false。

布尔型在与数值型进行拼接时，true为(1)，false为(0)。

 

##### 3、**Undefined(未定义)**

一个声明后没有被赋值的变量会有一个默认值(Undefined)，表示未定义数据类型(基于JavaScript的变量的特性)。

##### 4、**Null(空)**

表示为空(null)，需与Undefined区别开。

#### l **Typeof 可用来获取检测变量的数据类型**

语法：

 

 

var numb = 12;

Console.log(typeof numb); // 返回结果为 number

### 4、**数据类型转换**

##### **1\转换为字符串**

 

 

 

方式

说明

.toString()

转换为字符串

String()强制转换

转换为字符串

**+ ’ ’ 加号拼接字符串**

**和字符串拼接的结果都是字符串(隐式转换)**

 

 

 

 

 

 

 

 

 

##### **2\转换为数值型**

 

 

 

方式

说明

案例

parseInt(string)函数

将string类型转换为整数数值型

parseInt(‘35’)

parseFloat(string)函数

将string类型转换为浮点数值型

parseInt(‘23.65’)

Number()强制转换函数

将string类型转换为数值型

Number(‘12’)

js隐式转换(- * /)

利用算术运算隐式转换为数值型

‘12’ - 0

 

##### **3\转换为布尔型**

 

 

 

方式

说明

案例

Boolean()函数

将其他类型转换为布尔型

Boolean(‘true’)

 

l 代表空、否定的值会被转换为false	,如： ‘ ’ 、0、NaN、null、undefined。

l 其余值都会被转换为true。 

** **

### 5、**运算符**

#### **1\算术运算符**

概率：算术运算使用的符号，用于执行两个变量或值的算术运算。

运算符

描述

实例

+

加

10 + 20 =30

\-

减

10 - 20 =-10

*

乘

10 * 20 =200

/

除

10 / 20 =0.5

%

取余数（取模）

返回出发的余数 9 % 2 =1

 

 

 

 

 

 

 

 

 

#### **2\递增和递减运算符**

递增（++）

递减（- -）

放在变量前面时，我们称为前置递增(递减)运算符

放在变量后面时，我们称为后置递增(递减)运算符

注意：递增和递减运算符必须和变量配合使用。

 

①前置递增运算符

++num   使用口诀:先自加，后返回值

②后置递增运算符

num ++   使用口诀:先返回原值，后自加

#### **3\比较运算符**

​	是两个数据进行比较时所使用的运算符，比较运算后，会返回一个布尔值(true / false)作为比较运算的结果。所以经常将使用比较运算符的表达式用到逻辑运算符的运算中。

 

**运算符**

**说 明**

== 

表示两边表达式运算的结果相等，注意是两个等号

**===**

**(全等) 要求值和数据类型都一致**

!=

表示两边表达式运算的结果不相等

\>

表示左边表达式的值大于右边表达式的值

<

表示左边表达式的值小于右边表达式的值

\>=

表示左边表达式的值大于等于右边表达式的值

<= 

表示左边表达式的值小于等于右边表达式的值

 

#### **4\逻辑运算符**

**是用来进行布尔值运算的运算符，其返回值也是布尔值。**

**逻辑运算符**

**说明**

&&

“逻辑与”两边都是 true才返回 true，否则返回 false

||

“逻辑或”两边都为 false 才返回 false，否则都为true

！

“逻辑非”（!）也叫作取反符，用来取一个布尔值相反的值，如 true 的相反值是 false

 

 

 

 

 

 

 

 

 

 

 

##### **4.1、逻辑中断**

概念：当有多个表达式（值）时,左边的表达式值可以确定结果时,就不再继续运算(执行)右边的表达式的值。

①逻辑与 &&

语法：

表达式1 && 表达式2

 

如果第一个表达式的值为true，则返回表达式2

 

如果第一个表达式的值为false，则返回表达式1

 

 

 

②逻辑或 ||

语法：

表达式1 || 表达式2

 

如果第一个表达式的值为真，则返回表达式1

 

如果第一个表达式的值为假，则返回表达式2

 

 

 

### 6、**数组**

#### 1) **、创建数组**

**JavaScript **中创建数组有两种方式：

l 利用 new 创建数组

var array = new Array();

l 利用数组字面量 [] 创建数组

var array = [];

 

#### 2) **、数组的索引(下标)**

索引 (下标) ：用来访问数组元素的序号

array[1]; // 获取array数组的第二个元素

可通过数组的索引遍历数组元素

#### 3) **、获取数组的长度length**

使用 **length**可访问数组元素的数量。

Array.length; // 获取array数组的长度

#### **4）、在数组中增加元素**

## 二、**JS函数**

### 1、**函数(function)**

l 就是封装了一段可被重复调用执行的代码块。通过此代码块可以实现大量代码的重复使用。

l 函数可以带参数也可以不带参数

l 声明函数的时候，函数名括号里面的是形参，形参的默认值为 undefined

l 调用函数的时候，函数名括号里面的是实参

l 多个参数中间用逗号分隔

l 形参的个数需与实参个数匹配

### 2、**函数的声明及调用**

​     // 带参数的函数声明

​    function 函数名(形参1, 形参2 , 形参3...) { // 可以定义任意多的参数，用逗号分隔

​    // 函数体

​    }

 

​    // 带参数的函数调用

​    函数名(实参1, 实参2, 实参3...);

 

### 3、**函数的返回值(return)**

​	在使用 return 语句时，函数会停止执行，并返回指定的值,如果函数没有 return ，返回的值是 undefined。

// 声明函数

function 函数名（）{

  ...

  return  需要返回的值;

}

// 调用函数

函数名();  // 此时调用函数就可以得到函数体内return 后面的值

**注：**

**return 语句之后的代码不被执行。**

**return 只能返回一个值。如果用逗号隔开多个值，则返回最后一个值。**

** **

#### **break、continue、return 的区别：**

**l break ： 结束当前循环体 (如 for、while)**

**l continue ：跳出本次循环，继续执行下次循环 (如for、while)**

**l return ：不仅可以退出循环，还能够返回 return 语句中的值，同时还可以结束当前的函数体内的代码**

### 4、**函数的Arguments对象**

​	JS函数都内置了一个 arguments 对象，arguments 对象中存储了传递的所有实参。

​	arguments展示形式是一个伪数组，因此可以进行遍历。

伪数组具有以下特点：

​	 ①：具有 length 属性

​	 ②：按索引方式储存数据

​	 ③：不具有数组的 push , pop 等方法

## 三、**JS作用域**

### 1、**概念**

​	一段程序代码所作用的程序范围，而限定这段程序的可用性范围就是**作用域**。

### 2、**作用域的分类**

JavaScript (ES6前) 中的作用域有两种：

l 全局作用域 (作用在script 标签范围内)

l 局部作用域 (函数作用域)

### 3、**变量的作用域**

#### 1）**、全局变量**

在全局作用域下，声明的变量叫做全局变量（在函数外部定义的变量）

l 全局变量，变量的整个<script>标签中都可以使用。

l 特殊情况下，在函数内不使用 var 声明的变量也是全局变量（不建议使用）

#### 2）**、局部变量**

在局部作用域下，声明的变量叫做局部变量（在函数内部定义的变量）

l 局部变量只能在该函数内部使用

l 函数的形参实际上就是局部变量

#### 3）**、区别**

​	全局变量：在整个<script>标签中都可以使用，只有在浏览器关闭时才会被销毁，因此比较占内存

​	局部变量：只在函数内部使用，当其所在的代码块被执行时，会被初始化；当代码块运行结束后，就会被销毁，因此更节省内存空间

### 4、**块级作用域(ES6)**

​	块作用域由 {} 包括。在 {} 里面声明的变量不能在 {} 外调用。

​	**ES6以前，JS没有块级作用域的概念。**

## 四、**JS预解析**

### 1、**概念：**

​	JavaScript 代码是由浏览器中的 JavaScript 解析器来执行的。JavaScript 解析器在运行 JavaScript 代码的时候分为两步：

​	预解析；(JS引擎会把JS里面所有的 **var** 还有 **function** 提升到当前作用域的最前面)

​	代码执行。

​	注：预解析只会发生在通过 **var** 定义的变量和 **function** 上。

### 2、**变量预解析(变量提升)**

​	 变量的声明会被提升到当前作用域的最上面，但变量的赋值不会被提升。

​     console.log(num); // 结果是多少？

​    var num = 10; 

​    // 输出返回undefined

 

​    //相当于执行了以下代码

​    var num;    // 变量声明提升到当前作用域最上面

​    console.log(num); // 输出返回undefined

​    num = 10;   // 变量的赋值不会提升

​	 

### 3、**函数预解析(函数提升)**

#### 1、**概念：**

​	函数的声明会被提升到当前作用域的最上面，但是不会调用函数。

#### 2、**函数表达式声明调用问题**

​	函数表达式调用必须写在函数声明的下面。(**因为函数表达式是通过变量的形式接收函数的，变量提升只提升变量，不提升赋值操作**)

​    // 匿名函数(函数表达式方式):若我们把函数调用放在函数声明上面

​    fn();

​    var  fn = function() {

​      console.log('22'); // 报错

​    }

 

​    //相当于执行了以下代码

​    var fn;

​    fn();   //fn没赋值，没这个，报错

​    var  fn = function() {

​      console.log('22'); //报错

​    }

​	 

​	 

​	 

 

## 五、**JS对象**

### 1、**对象的概念**

​	在 JavaScript 中，对象是一组无序的相关**属性**和**方法**的集合，所有的事物都是对象，例如字符串、数值、数组、函数等。(对象必须是具体的事物，不能是抽象的概念)

​	对象是由**属性**和**方法**组成的：

​	属性：事物的特征，在对象中用属性来表示（常用名词）

​	方法：事物的行为，在对象中用方法来表示（常用动词）

### 2、**创建对象(object)**

#### （1）**、利用字面量创建对象 {}**

​	对象字面量：就是花括号 **{ }** 里面包含了表达这个具体事物（对象）的属性和方法，**{ }** 里面采取键值对的形式表示。

​	键：相当于属性名

​	值：相当于属性值，可以是任意类型的值（数字类型、字符串类型、布尔类型，函数类型等）。

​    var star = {

​      name : 'pink', // 多个属性或者方法中间用逗号隔开

​      age : 18,

​      sex : '男',

​      sayHi : function(){ // 方法冒号后面跟的是一个匿名函数

​        alert('大家好啊~');

​      }

​    };

​	 

#### （2）**、利用 new Object 创建对象**

​	var 对象名 = new Object();

​     var obj = new Object(); //创建了一个空的对象

​    // 对象属性赋值

​    obj.name = '张三丰';

​    obj.age = 18;

​    obj.sex = '男';

 

​    // 对象方法

​    obj.sayHi = function() {

​      console.log('hi~');

​    }

​    // 调用对象的属性以及方法

​    console.log(obj.name);

​    console.log(obj['sex']);

​    obj.sayHi();

 

 

#### （3）**、利用构造函数创建对象**

##### 1）**、构造函数的概念**

​	构造函数是一种特殊的函数，主要用来初始化对象，即为对象成员变量赋初始值，它总与 new 运算符一起使用。我们可以**将对象中一些公共的属性和方法抽取出来，然后封装到这个函数里面**。

​    //构造函数的语法格式

​    function 构造函数名() {

​      this.属性 = 值;

​      this.方法 = function() {}

​    }

​    new 构造函数名();

​	** **

 

##### 2）**、通过构造函数创建对象**

​	**在 JS 中，使用构造函数要时要注意以下几点：**

**l 构造函数名字首字母要大写**

**l 构造函数不需要return就可以返回结果**

**l 调用构造函数必须使用 new**

**l 我们只要new 构造函数() 就能创建了一个对象**

**l 我们的属性和方法前面必须加this**

​     // 创建Star构造函数

​	function Star(uname,age,sex) {

​      this.name = uname;

​      this.age = age;

​      this.sex = sex;

​      this.sing = function(sang){

​        console.log(sang);

​      }

​    }

​    

​    var ldh = new Star('刘德华',18,'男'); // 创建对象，并给对象赋初始值

​    console.log(typeof ldh) // object对象，调用函数返回的是对象

 

​    console.log(ldh.name);

​    console.log(ldh['sex']);

​    ldh.sing('冰雨'); // 调用对象方法，并传递实参

 

##### 3）**、构造函数与对象**

l 构造函数，如 Stars()，抽象了对象的公共部分，封装到了函数里面，它泛指某一大类（class）

l 创建对象，如 new Stars()，特指某一个，通过 new 关键字创建对象的过程我们也称为对象实例化

##### 4）**、New关键字**

new 在执行时的四种作用:

l 在内存中创建一个新的空对象。

l 让 this 指向这个新的对象。

l 执行构造函数里面的代码，给这个新对象添加属性和方法

l 返回这个新对象（所以构造函数里面不需要return）

#### **变量、属性、函数、方法总结**

l 变量：单独声明赋值，单独存在

l 属性：对象中的变量称为属性，不需要声明，**属性用来描述该对象的特征**

l 函数：单独存在的，通过 **函数名()** 的方式就可以调用

l 方法：对象里面的函数称为方法，方法不需要声明，使用 **对象.方法名()** 的方式就可以调用，**方法用来描述对象的行为和功能**。

### 3、**对象的调用**

**l 对象属性调用** : 对象.属性名。

​    console.log(star.name)  // 调用name属性

**l 对象属性的另一种调用方式** : 对象[‘属性名’]，注意方括号里面的属性必须加引号，我们后面会用

​    console.log(star['name']) // 调用name属性

**l 对象方法调用**：对象.方法名() ，注意这个方法名字后面一定加括号

​    star.sayHi();       // 调用 sayHi 方法 (注意：方法的调用必须用 ‘()’ )

### 4、**遍历对象属性 for in**

​	用于对数组或对象的属性进行循环操作。

var

必须，指定的变量可以是数组元素，也可以是对象的属性

Object

必须。指定迭代的的对象。

​	 

   for(变量 in 对象名字){

   	// 在此执行代码

  }

 

​    // 创建对象

​    var obj = {

​      name: '秦sir',

​      age: 18,

​      sex: '男',

​      fn:function() {};

​    };

 

​    //for in 遍历obj对象

​    for(var key in obj){

​      console.log(key); // key 变量 输出的是属性名

​      console.log(obj[key]); // 通过调用对象属性的方式，得到属性值

​    }

 

## 六、**JS内置对象**

### 1、**概念**

​	内置对象就是指 JS 语言自带的一些对象，这些对象供开发者使用，并提供了一些常用的或是最基本而必要的功能。

​	JavaScript 提供了多个内置对象：Math、 Date 、Array、String等。

### 2、**MDN文档**

​	学习一个内置对象的使用，只要学会其常用成员的使用即可，我们可以通过查文档学习，可以通过MDN来查询。

​	 

### 3、**Math对象**

#### **（1）、概念**

​	Math 对象不是构造函数，它具有数学常数和函数的属性和方法。跟数学相关的运算（求绝对值，取整、最大值等）可以使用 Math 中的成员。

​	**Math 的所有属性与方法都是静态的，不需要通过New关键字进行调用。**

#### **（2）、Math的常用属性**

##### 	1）、Math.PI	-圆周率

#### **（3）、Math的常用函数**

​	描述：如果没有参数，则结果为 - Infinity；

​	如果有任一参数不能被转换为数值，则结果为 NaN。 

##### 	1）、Math.Max() - 返回最大值

##### 	2）、Math.Min() - 返回最小值

##### 	3）、Math.abs() - 返回绝对值

##### 	4）、Math.floor() - 向下取整

##### 	5）、Math.ceil() - 向上取整

##### 	6）、Math.round() - 四舍五入

##### 	7）、Math.random() - 随机数

​	 函数返回一个浮点数， 伪随机数在范围从0 到小于1，也就是说，从 0（包括 0）往上，但是不包括 1。

得到一个范围区间的随机数，参照MDN文档公式。

 

 

 

 

​    var arr = ['张杰', '李连杰', '周杰伦', '成龙', '甄子丹'];

​    // Math.random()生成随机数

​    function getRandom(min, max) {

​      return Math.floor(Math.random() * (max - min + 1)) + min; // 含最大值，含最小值

​    }

​    console.log(getRandom(1, 10));

​    console.log(arr[getRandom(0, arr.length-1)]); 

 

### 4、**Date对象**

#### （1）**、概念**

l 创建Date实例，用于处理日期和时间。Date 对象基于自 1970 年 1 月 1 日起经过的毫秒数。

l Date对象需要通过调用Date构造函数来实例化日期对象，即 new Date()。

l 若将它作为常规函数调用（即不加 new 操作符），将返回一个字符串，而非 Date 对象。

#### （2）**、创建Date对象**

##### 	1）**、获取当前时间**

​	 var date = new Date();  // 创建日期对象

##### 	2）**、new Date() 构造函数**

​	当构造函数中没有参数，返回当前时间；

​	当构造函数中存在参数，则返回对应参数的日期时间。（参数常用的写法： 数字型 2019,10,1；  字符串型 '2019-10-1 8:8:8' 时分秒）

​     // 1.如果构造函数中没有参数，返回当前系统时间

​    var now = new Date();

​    console.log(now);

 

​    // 2.如果Date()里面写参数，则返回对应参数的日期时间 

​    var data = new Date(2019,10,1);

​    console.log(data); // 返回的是11月不是10月

​    var data2 = new Date('2019-10-1 8:8:8');

​    console.log(data2);

​	 

#### （3）**、日期格式化**

##### 	1）**、方法**

​	方法名

​	说明

​	代码

​	get FullYear()

​	获取当年

​	obj.getFullYear()

​	getMonth()

​	获取当月(0-11)

​	obj.getMonth()

​	getDate()

​	获取当天日期

​	obj.getDate()

​	getDay()

​	获取星期几(周日0到周六6)

​	obj.getDay()

​	getHours()

​	获取当前小时

​	obj.getHours()

​	getMinutes()

​	获取当前小时

​	obj.getMinutes()

​	getSeconds()

​	获取当前秒钟

​	obj.gerSeconds()

 

##### 	2）**、格式化年月日**

​     // 格式化日期格式

​    var date = new Date(); // 创建当前日期对象

 

​    // 将日期格式化显示

​    var year = date.getFullYear(); // 获取年

​    var month = date.getMonth() + 1; // 获取月--返回 0-11

​    var dates = date.getDate(); // 获取天

​    var intDay = date.getDay(); // 获取星期--返回0-6

 

​    // 将getDay返回的数值转换为星期

​    var strDay = ["星期日","星期一","星期二","星期三","星期四","星期五","星期六"]

​    var strDate = year + '年' + month + '月' + dates + '号' + strDay[intDay];

 

​    console.log(strDate);

##### 	3）**格式化时分秒**

​	// 将时间格式化显示

​    var h = date.getHours(); // 时

​    var m = date.getMinutes(); // 分

​    var s = date.getSeconds(); // 秒

 

​    // 时分秒小于10时，前面加上0

​    h = h < 10 ? '0' + h : h;

​    m = m < 10 ? '0' + m : m;

​    s = s < 10 ? '0' + s : s;

​    var strTime = h + ':' + m + ':' + s;

​    console.log(strTime);

** **

** **

#### （4）**、时间戳**

##### 	1）**、概述**

​	时间戳是指格林威治时间自1970年1月1日（00:00:00 GMT）至当前时间的总秒数。

##### 	2）**、获取当前时间总的毫秒数**

l date.valueOf() ：得到date时间对象距离1970年1月1日（08:00:00 GMT+8）总的毫秒数

l date.getTime() ：得到date时间对象距离1970年1月1日（08:00:00 GMT+8）总的毫秒数

​    // 实例化Date对象

​    var date = new Date();

 

​    // 1 .通过 valueOf() getTime() 用于获取Date对象的原始值

​    console.log(date.valueOf()); // 得到现在时间距离1970.1.1总的毫秒数

​    console.log(date.getTime());

​    // 2.简单的写法

​    var date1 = +new Date(); // +new Date()返回的就是总的毫秒数，

​    console.log(date1);

l Date.now(); 得到当前时间距离1970年1月1日（08:00:00 GMT+8）总的毫秒数

​	now() 是 Date 的一个静态函数，所以必须以 Date.now() 的形式来使用。

#### （5）**、倒计时-算法**

​	// 倒计时

​    function conutDown(dateTimes) {

​      var datetime = new Date(dates);

​      var times = (datetime.getTime() - Date.now()) / 1000; // 将开始时间与当前时间转换为秒进行计算

 

​      // 计算倒计时 天-时-分-秒

​      var day = Math.floor(times / 60 / 60 / 24);

​      var hours = Math.floor(times / 60 / 60 % 24);

​      var minutes = Math.floor(times / 60 % 60);

​      var seconds = Math.floor(times % 60);

​      var strTimes = day + '天' + hours + ':' + minutes + ':' + seconds;

​      return console.log(strTimes);

​    }

​    conutDown("2022-10-29 0:0:0");

 

### 5、**Array对象**

#### （1）**、概述**

参见文档-数组

#### （2）**、判断是否为Array**

##### 	**1)、Array.isArray(**value**); -方法**

##### 	**2)、instanceof -运算符**

当检测 Array 实例时，Array.isArray 优于 instanceof，因为 Array.isArray 能检测 iframes。

​    // 判断是否为数组类型 -Array

​    // Array.isArray(); -Array方法

​    var arr = new Array();

​    Array.isArray(arr); // true

 

​    // instanceof -运算符

​    arr instanceof Array; // true

 

#### （3）**、添加数组元素**

##### **①、unshift()函数**

在数组开头插入元素，该函数能够把一个或多个参数值附加到数组的头部

array.unshift(元素1, 元素2, ..., 元素X)

##### **②、push()函数**

把一个或多个参数值附加到数组的尾部，并返回添加元素后的数组长度

 array.push(元素1, 元素2, ..., 元素X)

 

##### **③、concat() 函数**

也可以插入给定的一个或多个元素，能够把传递的所有参数按顺序添加到数组的尾部。

​	var array1 = [1,2,3,4,5]; //定义数组

 

​	var array2 = array1.concat(6,7,8); //为数组a连接3个元素

说明：concat() 方法将创建并返回一个新数组，而不是在原来的基础上添加新元素。

##### **④、splice() 函数**

在指定下标位置插入一个或多个元素。

函数参数说明：

​	第1个参数index为指定起始下标位置；

​	第2个参数howmany指定应该删除的元素数目，当值设置为0时，就会不执行删除操作；

​	这样就可以通过第3个及后面参数item1,.....,itemX来插入一个或多个元素。

 array.splice(index,howmany,item1,.....,itemX)

#### （4）**、删除数组元素**

##### **①、delete**

 var arr = [1,true,{},"a"]; // 定义数组

 delete arr[0]; // 删除索引为 ’0’ 的数组元素

用delete删除后，数组的长度length不会发生变化，此时arr[x]变为undefined。

##### **②、pop()函数**

  var arr = [1,true,{},"a"]; // 定义数组

​     arr.pop(); // 删除数组中最后一个元素

删除数组中**最后一个**元素，并返回该元素的值。此方法会更改数组的长度。

##### **③、shift()函数**

​    var arr = [1,true,{},"a"]; // 定义数组

​     arr.shift(); // 删除数组中第一个元素

删除数组中**第一个**元素，并返回该元素的值。此方法更改数组的长度。

#### （5）**、筛选数组-算法**

​    // 筛选数组，将数组[2000, 1500, 5000, 600]中大于2000的添加到新数组中

​    var array = [2000, 1500, 5000, 600];

​    var newArr = new Array();

​    for (let index = 0; index < array.length; index++) {

​      // 大于2000添加到newArr数组中

​      if (array[index] > 2000) {

​        newArr.push(array[index]);  

​      }

​    }

​    console.log(newArr);

#### （6）**、数组排序**

##### **①、reverse()函数**

​     var array = [2000, 1500, 5000, 600];

​    array.reverse(); // [600, 5000, 1500, 2000]

将数组中元素的位置反转，并返回该数组。

##### **②、sort()函数**

​    // 数组排序(冒泡排序)

​    var array = [2, 1, 5, 6];

​    array.sort();

​    console.log(array); // [1, 2, 5, 6]

 

​    // 对于双位数

​    var arr = [1,64,9,61];

​    arr.sort(function(a,b) {

​      return b - a; //降序的排列

​      return a - b; //升序

​      }

​    )

 

​	将数组中元素进行排序，排序顺序是在将元素转换为字符串，然后比较它们的** UTF-16 **代码单元值序列时构建的。（可以比较字符串）

​	于具体实现，因此无法保证排序的时间和空间复杂性。

#### （7）**、获取Array元素索引**

##### **①、indexOf()函数**

​    var array = [2000, 1500, 5000, 600, 2000];

​    array.indexOf(2000); // 返回数组元素的索引: 1

返回在数组中可以找到指定元素的第一个索引（可能存在该元素在数组中重复出现），如果不存在，则返回 -1。

##### **②、lastIndexOf()函数**

​       var array = [2000, 1500, 5000, 600, 2000];

​    array.lastIndexOf(2000); // 返回数组元素的索引: 4

返回指定元素在数组中的最后一个的索引，如果不存在则返回 -1。从数组的后面向前查找

## 七、**JS的事件函数**

### 1、**Is NaN();**

​	用于判断一个变量是否为非数值，返回布尔型。

- **14
- **60
- **86


- [首页](https://www.bilibili.com/)
- [番剧](https://www.bilibili.com/anime/)
- [直播](https://live.bilibili.com/)
- [游戏中心](https://game.bilibili.com/platform)
- [会员购](https://show.bilibili.com/platform/home.html?msource=pc_web)
- [漫画](https://manga.bilibili.com/?from=bill_top_mnav)
- [赛事](https://www.bilibili.com/match/home/)
- [下载客户端](https://app.bilibili.com/)


- [![img](https://i2.hdslb.com/bfs/face/077ab2fc52c91d11effdb4eecc31a476c8de2d74.jpg@120w_120h_1c)](https://space.bilibili.com/159940583)
- [大会员](https://account.bilibili.com/account/big)
- [消息](https://message.bilibili.com/)
- [动态](https://t.bilibili.com/)
- [收藏](https://space.bilibili.com/159940583/favlist)
- [历史](https://www.bilibili.com/account/history)
- [创作中心](https://member.bilibili.com/platform/home)
- ​
- [投稿](https://member.bilibili.com/platform/upload/video/frame)

# JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续

![img](https://s1.hdslb.com/bfs/static/jinkela/video/asserts/view.svg)634.3万![img](https://s1.hdslb.com/bfs/static/jinkela/video/asserts/dm.svg)21.4万![img](data:image/svg+xml;base64,PHN2ZyB0PSIxNjQyNTg4MTEzODk5IiBjbGFzcz0iaWNvbiIgdmlld0JveD0iMCAwIDEwMjQgMTAyNCIgdmVyc2lvbj0iMS4xIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHAtaWQ9IjY4MjciIHhtbG5zOnhsaW5rPSJodHRwOi8vd3d3LnczLm9yZy8xOTk5L3hsaW5rIiB3aWR0aD0iMjAwIiBoZWlnaHQ9IjIwMCI+PGRlZnM+PC9kZWZzPjxwYXRoIGQ9Ik0xNjcuMDI0IDUxMmEzNDQuOTc2IDM0NC45NzYgMCAxIDEgNjg5Ljk1MiAwIDM0NC45NzYgMzQ0Ljk3NiAwIDAgMS02OTAgMHpNNTEyIDEwNi45NzZhNDA1LjAyNCA0MDUuMDI0IDAgMSAwIDAgODEwLjA0OCA0MDUuMDI0IDQwNS4wMjQgMCAwIDAgMC04MTB6IG0zMCAyMzUuMDA4YTMwIDMwIDAgMSAwLTYwIDBWNTEyYzAgNy45NjggMy4xNjggMTUuNiA4Ljc4NCAyMS4yMTZsMTIwIDEyMGEzMCAzMCAwIDEgMCA0Mi40MzItNDIuNDMyTDU0MiA0OTkuNTJWMzQxLjk4NHoiIGZpbGw9IiM5NDk5QTAiIHAtaWQ9IjY4MjgiPjwvcGF0aD48L3N2Zz4=) 2020-09-01 18:09:44**未经作者授权，禁止转载


6.0万6.0万13.2万2.7万

稿件投诉

50 篇笔记

素材大全：https://gitee.com/xiaoqiang001/java-script.gitPPT 在我账号专栏里面网盘地址1.JavaScript基础从变量的定义与使用、流程控制语句、数组、函数、构造函数、内置对象以及对象等2.web API 讲解如何获取DOM元素，如何操作DOM 元素，BOM操作 移动端制作网页特效3. 后面还会有js高级，ES6类面向对象语法，面向对象案例，原型和原型链等等。4. 还有会jquery 综合 + echarts数据可视化

展开更多

- [科技](https://www.bilibili.com/v/tech/)
- [计算机技术](https://www.bilibili.com/v/tech/computer_tech)
- [视频教程](https://search.bilibili.com/all?keyword=%E8%A7%86%E9%A2%91%E6%95%99%E7%A8%8B&from_source=video_tag)
- [js入门视频](https://search.bilibili.com/all?keyword=js%E5%85%A5%E9%97%A8%E8%A7%86%E9%A2%91&from_source=video_tag)
- [JavaScript](https://search.bilibili.com/all?keyword=JavaScript&from_source=video_tag)
- [WEB前端开发](https://search.bilibili.com/all?keyword=WEB%E5%89%8D%E7%AB%AF%E5%BC%80%E5%8F%91&from_source=video_tag)
- [前端入门视频](https://search.bilibili.com/all?keyword=%E5%89%8D%E7%AB%AF%E5%85%A5%E9%97%A8%E8%A7%86%E9%A2%91&from_source=video_tag)
- [pink老师](https://search.bilibili.com/all?keyword=pink%E8%80%81%E5%B8%88&from_source=video_tag)

![img](https://i0.hdslb.com/bfs/sycp/creative_img/202210/a0552f3d0199dd0c1d8544af198a6bcf.jpg@!web-video.webp)![img](https://s1.hdslb.com/bfs/static/jinkela/long/images/eva.png)

- 评论6112

- 最热

  ​

  最新

![img](https://i2.hdslb.com/bfs/face/077ab2fc52c91d11effdb4eecc31a476c8de2d74.jpg@160w_160h_1c_1s.webp)

发布

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

黑马前端

*置顶*全套配套资料教程，关注微信公众号：黑马程序员，回复：领取资源02
2022版前端最新最全学习路线图
![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[2023年web前端开发学习路线图]()
资源下载问题
![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[黑马程序员教程资源下载指南]()
web入门
H5C3+移动布局 ：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程]()
JavaScript系列：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续]()
技术进阶
[jQuery]()**：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员前端基础教程|jQuery网页开发案例精讲]()
Ajax：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员AJAX零基础到精通_整合Git核心内容全套教程（2022年已更新优化）]()
Vue开发
Node.js: ![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员Node.js全套入门教程，nodejs新教程含es6模块化+npm+express+webpack+promise等_Nodejs实战案例详解]()   
Vue2+Vue3全套：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员Vue全套视频教程，从vue2.0到vue3.0一套全覆盖，前端学习核心框架教程]()
React&小程序开发
React：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员前端React视频教程，react零基础入门原理详解到好客租房项目实战]()
零基础玩转微信小程序：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员前端微信小程序开发教程，微信小程序从基础到发布全流程_企业级商城实战(含uni-app项目多端部署)]()
教程学习可能遇到的问题答疑（非技术型）：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[黑马程序员学习常见问题答疑]()

2021-12-27 15:04**839**回复

共103条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

黑马前端

pink账号学习路线：
\1. H5C3+移动布局 ![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程]()
\2. [JavaScript]()**系列 ![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[JavaScript基础语法-dom-bom-js-es6新语法-jQuery-数据可视化echarts黑马pink老师前端入门基础视频教程(500多集)持续]()

2020-09-04 15:14**1590**回复

![img](https://i1.hdslb.com/bfs/face/798c5b85e849b8b37da772589b8362a16f554580.jpg@160w_160h_1c_1s.webp)

帅气的蠢脸

推荐最新 高口碑的2022年web前端教程：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[求知讲堂web前端 96天完整版 学完可就业]()

2023-01-05 15:28

**11

**

回复

**

共176条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/168bc915f4b5cb809088e2942b57dc594a568476.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

太空浪子1900

变量：P11～19
数据类型：P20～40
运算符：P41～54
流程控制分支结构：P55～68
循环：P69～95
数组：P96～112
函数：P113～133
作用域：P134～139
JS预解析：P140～142
对象：P143～153
内置对象：P155～186
简单数据类型和复杂数据类型：P187～190
DOM：P194～265
事件高级：P247～265
BOM：P266～286
PC端网页特效：P287～329
移动端网页特效：P331～353
本地存储：P354～357
jQuery：P358～[442]()**
数据可视化：P443～473

2021-10-20 15:34**2464**回复

![img](https://i2.hdslb.com/bfs/face/066d7fb216ffaad2ef3ba468d3873272367eea0d.jpg@160w_160h_1c_1s.webp)

小杨苏西138

![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/6BO9VeUCy.png@.webp)[2023年最新前端零基础入门资料(资料+视频+训练项目）]()

4小时前

**5

**

回复

**

共107条回复, 点击查看

![img](https://i0.hdslb.com/bfs/face/aaccce8d0a9a3a2d915d2fcdb00be7943bcfafaa.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

aaaaaaabbbccooo

pink圈

1

[Pink老师]()**，我们全寝都看你的视频！

2020-09-01 21:09**455**回复

热评

UP主觉得很赞

![img](https://i0.hdslb.com/bfs/face/3263a42a11d6156d22e4baebfdca44aeb19e257e.jpg@160w_160h_1c_1s.webp)

我以灬不为

这套课程哪里是讲es6的？

2022-11-18 10:19

**5

**

回复

**

共25条回复, 点击查看

![img](https://i0.hdslb.com/bfs/face/7328c2ceff43106b77803137647e243af218ea07.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

Candy_leee

从今年三月开始，跟随pink老师学习到现在，今天把B站pink老师更新的所有视频看完了，回顾这一路上的坚持，很感谢自己也很感谢pink老师，从最初的标签，到后面的样式，以及js，pink老师讲的都十分细腻，后面还有许多东西需要学习，[node]()**，ajax，vue等框架，相信自己，坚持就是胜利，再次感谢pink老师，愿大家都能在学习的过程中找到自己的方向，实现自己的梦想！![[惊喜]](https://i0.hdslb.com/bfs/emote/0afecaf3a3499479af946f29749e1a6c285b6f65.png@24w_24h.webp)

2021-06-02 16:48**710**回复

热评

UP主觉得很赞

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

黑马前端

真棒哈~~  不过刚更新了js，记得随时去看看有没有更新哈

2021-06-02 16:53

**52

**

回复

**

![img](https://i0.hdslb.com/bfs/face/7328c2ceff43106b77803137647e243af218ea07.jpg@160w_160h_1c_1s.webp)

Candy_leee

回复 @黑马程序员pink老师 :好的pink老师![[给心心]](https://i0.hdslb.com/bfs/emote/1597302b98827463f5b75c7cac1f29ea6ce572c4.png@24w_24h.webp)，受宠若惊哈哈，现在还在学习jQuery，先问一下以后jQuery的运用还多吗

2021-06-02 16:59

**20

**

回复

**

共68条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

黑马前端

小伙伴们，里面包含 视频，源码笔记甚至作业哦，你们懂得，该一键三连啦，这样可以提高视频的排名，可以让更多的人看到这个视频哈~~ 还是那句话，[pink老师]()**还能火一把吗？？

2020-09-01 18:24**1972**回复

![img](https://i1.hdslb.com/bfs/face/5096f966bd4c087089f23dd9a7c1f6f1b5fe2065.jpg@160w_160h_1c_1s.webp)

放剁椒的麻辣小龙虾

感谢

2021-05-17 14:23

**

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

账号已注销

梦开始的地方![[吃瓜]](https://i0.hdslb.com/bfs/emote/4191ce3c44c2b3df8fd97c33f85d3ab15f4f3c84.png@24w_24h.webp)

2021-06-02 10:00

**

**

回复

**

![img](https://i0.hdslb.com/bfs/face/1151fa7251c378b9d36f491ad2062d4b78404192.jpg@160w_160h_1c_1s.webp)

Warmgzy

感谢pink老师，受益匪浅

2021-08-04 14:42

**11

**

回复

**

共135条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/8eaba7b514a10293c791149b6ee5ab54f379a9d6.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

烟掩嫣颜淹眼檐

兄弟们我找了好久终于找到后续啦：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员JavaScript核心教程，前端基础教程，JS的DOM BOM操作教程]() 接71p
然后可以去看看ES6的教程：![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[2019全新javaScript进阶面向对象ES6]()

2020-11-07 00:51**866**回复

![img](https://i0.hdslb.com/bfs/face/55fdec9ef1fb4d2fc32a3082decb59cccda4f4cb.jpg@160w_160h_1c_1s.webp)

DayDayON99

今天是2021年2月24日，年十三，祝大家新年快乐，身体健康，早日找到心仪的工作。
到今日为止，pink老师本系列更新到第328集。接下去的内容在![img](https://i0.hdslb.com/bfs/activity-plat/static/20201110/4c8b2dbaded282e67c9a31daa4297c3c/AeQJlYP7e.png@.webp)[黑马程序员JavaScript核心教程，前端基础教程，JS的DOM BOM操作教程]() 第139集开始。
顶我上去啊~~~![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)

2021-02-24 17:33

**113

**

回复

**

![img](https://i0.hdslb.com/bfs/face/2fc5e388c6fbf34ad1ece7e64929f97f1ac5eacd.jpg@160w_160h_1c_1s.webp)

小林小林小林丶

插

2022-05-29 17:46

**11

**

回复

**

![img](https://i1.hdslb.com/bfs/face/39cbf4ff394df4801d13b2cc40f8c79ba3a13d8e.jpg@160w_160h_1c_1s.webp)

梭_影

cy

2022-06-01 23:07

**9

**

回复

**

共84条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/4a21617295f8c3ead4b64fe8c8e0e27ebf5d15f8.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

学呢

笔记

一、JavaScript简介(JS)1、JS概述	1、JavaScript是现阶段最主流的编程语言之一，是一种运行在客服端(浏览器)的脚本语言，同时也... 展开 

2022-10-20**86**回复

![img](https://i0.hdslb.com/bfs/face/23dd230aa0ad2bde480517d20f42bceea046cb3b.jpg@160w_160h_1c_1s.webp)

沙漠之花的

好银，这些

2022-11-06 22:33

**2

**

回复

**

![img](https://i2.hdslb.com/bfs/face/b863304fc9c244b53d32bb98ae95a43b45cc3547.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

bili-首席管理员

JS结束！Pink老师yyds
JavaScript基础大总结(一)：https://blog.csdn.net/Augenstern_QXL/article/details/119249534
JavaScript基础之函数与作用域(二)：https://blog.csdn.net/Augenstern_QXL/article/details/119250991
JavaScript基础之对象与内置对象(三)：https://blog.csdn.net/Augenstern_QXL/article/details/119250137
JavaScript进阶之[DOM]()**技术(四)：https://blog.csdn.net/Augenstern_QXL/article/details/115416921
JavaScript进阶之BOM技术(五)：https://blog.csdn.net/Augenstern_QXL/article/details/115406408
JavaScript提高之面向对象(六)：https://blog.csdn.net/Augenstern_QXL/article/details/115219073
JavaScript提高之ES6(七)：https://blog.csdn.net/Augenstern_QXL/article/details/115344398

2021-08-03 20:38**262**回复

![img](https://i1.hdslb.com/bfs/face/7e846fe040fc5af61f1779c43402680ce3ebffa9.jpg@160w_160h_1c_1s.webp)

谁尚能饭否

大佬好强
你的csdn让我膜拜

2022-01-05 15:36

**12

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

WileyWon

在

2022-08-07 14:34

**7

**

回复

**

共11条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/1a696e914fbe3c6fb3e0eecd35b64127a1c49bc7.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

七喜紅茶

今年二月份到现今，在B站与pink老师相伴快一百多个小时，html到js再到jq，收获颇丰。敲了很多感谢词，想来又不合适，或许在旁人看来过于矫情。反复修改之后。我最想说的是一句“老师，谢谢您！”

2021-05-30 20:42**262**回复

UP主觉得很赞

![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@160w_160h_1c_1s.webp)

黑马前端

看到你的留言暖暖的

2021-05-30 23:51

**59

**

回复

**

共15条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/2243a5175bd92b370f5a1fb7b2b3e933f49c2078.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

Best_08

// A T M 
​        var money = 100;
​        var price = 0;
​        while (num != 4) {
​            var num = [prompt]()**('请输入你要的操作:\n1.存钱\n2.取钱\n3.显示余额\n4.退出')
​            switch (num) {
​                case '1':
​                    price = prompt('输入要存的钱数；');
​                    money = money + parseFloat(price);
​                    alert('您的余额；' + money);
​                    continue;
​                case '2':
​                    price = prompt('输入你要取出的钱: ');
​                    money = money - parseFloat(price);
​                    alert('您的余额' + money);
​                    continue;
​                case '3':
​                    alert('您的余额：' + money);
​                    continue;
​                case '4':
​                    alert('正在退出...')
​                    break;
​            }
P 95 ATM 作业。

2021-01-26 17:37**147**回复

![img](https://i0.hdslb.com/bfs/face/135dd693c422659ad293a42c62fb00680518bbae.jpg@160w_160h_1c_1s.webp)

丶Jns

是不是可以取钱取成负数

2021-07-18 23:32

**10

**

回复

**

![img](https://i2.hdslb.com/bfs/face/325d4e1c87566b947cc36dfe004555df4f65efbf.jpg@160w_160h_1c_1s.webp)

那年メ

回复 [@丶Jns]() :  var monye = 100;
​        //计数
​        var count = 0;
​        while (num != 4) {
​            var num = prompt('请输入你要的操作: \n1.存钱\n2.取钱\n3.显示余额\n4.退出')
​            switch (num) {
​                case '1':
​                    count = prompt('你要纯多少钱')
​                    monye += parseFloat(count)
​                    alert('你的余额为' + monye)
​                    continue
​                case '2':
​                    count = prompt('你要取多少钱')
​                    if (count > monye) {
​                        alert('对不起当前你的余额不足')
​                    } else {
​                        monye -= parseFloat(count)
​                    }
​                    alert('你的余额为' + monye)
​                    continue
​                case '3':
​                    alert('当前你的余额剩余' + monye)
​                    continue
​                case '4':
​                    alert('退出成功')
​                    break;
​                default:
​                    alert('没有此操作')
​            }
​        }

2021-10-16 23:33

**29

**

回复

**

共36条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/d27799455e4b10c0397efc7f8fd65276f9da477a.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

西巴西巴p

我们线下经常看到pink老师呦

2020-09-03 00:14**181**回复

热评

UP主觉得很赞

![img](https://i1.hdslb.com/bfs/face/61446c17b10d99636ab0463125a4921f4c2dff27.jpg@160w_160h_1c_1s.webp)

minecraft_-

帅？

2021-09-10 07:03

**7

**

回复

**

![img](https://i1.hdslb.com/bfs/face/fa48ac10818c4519a3733ba82e3ccc7118281d04.jpg@160w_160h_1c_1s.webp)

清风雅雨

pink老师在哪里人呀？

2021-12-09 14:33

**11

**

回复

**

![img](https://i1.hdslb.com/bfs/face/0b21b2693434264de9df96c023a94ba397fd0da4.jpg@160w_160h_1c_1s.webp)

B站小王o

回复 [@清风雅雨]() :武汉

2022-01-24 17:09

**10

**

回复

**

共10条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/ca639d37ad807f049f6c9005056167283232946b.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

100KCAL

虽然[黑马程序]()**员有，但就是想来pink老师这里看

2020-09-14 05:54**163**回复

UP主觉得很赞

![img](https://i2.hdslb.com/bfs/face/ca639d37ad807f049f6c9005056167283232946b.jpg@160w_160h_1c_1s.webp)

100KCAL

别忘了点赞，投币

2020-09-14 05:55

**26

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

Goencc

回复 [@100KCAL]() :阿噗主觉得很淦

2021-04-28 14:35

**12

**

回复

**

![img](https://i0.hdslb.com/bfs/face/2dec25896ef4a3f22ae4bf61a1b0a64ecb12aa0f.jpg@160w_160h_1c_1s.webp)

Polarisss----

请问数据可视化那部分是不是不完全呢

2022-01-05 21:21

**8

**

回复

**

共10条回复, 点击查看

![img](https://i0.hdslb.com/bfs/face/d20e15f14148cebc6d60af8496ae0d29d2c761cd.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

奇葩小白羊

125作业计算器
function getResult([num]()**1, sign, num2) {
​            var result;
​            while (true) {
​                switch (sign) {
​                    case '+':
​                        result = num1 + num2;
​                        return result;
​                    case '-':
​                        result = num1 - num2;
​                        return result;
​                    case '*':
​                        result = num1 * num2;
​                        return result;
​                    case '/':
​                        result = num1 / num2;
​                        return result;
​                    default:
​                        alert('输入有误，请重新输入！')
​                        return result;
​                }
​            }
​        }
​        var re = getResult(parseFloat(prompt('请输入数字：')), prompt('请输入操作符：'), parseFloat(prompt('请输入数字：')));
​        console.log(re);

2021-01-30 14:06**104**回复

![img](https://i0.hdslb.com/bfs/face/f08dbd64aebad299246e918a36bc8e36544e9339.jpg@160w_160h_1c_1s.webp)

annnez

这个不是P154的吗，不过为什么这个封装函数的作业会放在这里。。。

2021-04-19 15:13

**10

**

回复

**

![img](https://i0.hdslb.com/bfs/face/518213cc130761a6f3fd4b9752d2a5236ec312a3.jpg@160w_160h_1c_1s.webp)

LilllHumBro

补充一下，case后面的运算符应该加引号包含，不然的话数据类型和switch里面的不一样，运行不了，我也是想了好一会才解决的![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)![[笑哭]](https://i0.hdslb.com/bfs/emote/c3043ba94babf824dea03ce500d0e73763bf4f40.png@24w_24h.webp)希望对大家有帮助

2021-09-16 16:54

**9

**

回复

**

![img](https://i0.hdslb.com/bfs/face/518213cc130761a6f3fd4b9752d2a5236ec312a3.jpg@160w_160h_1c_1s.webp)

LilllHumBro

回复 @LilllHumBro :可能是我太菜了，想了很久才发现问题，求轻喷![[doge]](https://i0.hdslb.com/bfs/emote/3087d273a78ccaff4bb1e9972e2ba2a7583c9f11.png@24w_24h.webp)![[微笑]](https://i0.hdslb.com/bfs/emote/685612eadc33f6bc233776c6241813385844f182.png@24w_24h.webp)

2021-09-16 16:56

**8

**

回复

**

共11条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/7622fe500d64cac1ba2b7311a25ef904d2311551.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

垰萨

变量：P11～19
数据类型：P20～40
运算符：[P41]()**～54
流程控制分支结构：P55～68
循环：P69～95
数组：P96～112
函数：P113～133
作用域：P134～139
JS预解析：P140～142
对象：P143～153
内置对象：P155～186
简单数据类型和复杂数据类型：P187～190
DOM：P194～265
事件高级：P247～265
BOM：P266～286
PC端网页特效：P287～329
移动端网页特效：P331～353
本地存储：P354～357
jQuery：P358～442
数据可视化：P443～473

2021-12-21 10:10**63**回复

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

酷酷的琪67

大哥，这里面应该学哪些内容？

2022-05-22 19:30

**6

**

回复

**

![img](https://i0.hdslb.com/bfs/face/member/noface.jpg@160w_160h_1c_1s.webp)

不吃土豆粉吃土豆

回复 [@酷酷的琪67]() :除了jQuery都得学啊

2022-05-23 16:59

**6

**

回复

**

共6条回复, 点击查看

![img](https://i1.hdslb.com/bfs/face/405a0d641f57713928303147ddcb8d4db17b3e2d.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

南枝向北

跪求pink老师的vue视频，硬币三连已经饥渴难耐了![[保佑]](https://i0.hdslb.com/bfs/emote/fafe8d3de0dc139ebe995491d2dac458a865fb30.png@24w_24h.webp)

2020-09-11 11:03**200**回复

![img](https://i1.hdslb.com/bfs/face/8328f9435c7ffa49c7672ba7e68909066708b9cf.jpg@160w_160h_1c_1s.webp)

粉色程序员

尚硅谷刘天宇Vue可以去看看，绝对是全站最好的Vue

2022-01-16 16:00

**12

**

回复

**

![img](https://i0.hdslb.com/bfs/face/cdd020f3fafadc89d7f92af69a6071cb11c52527.jpg@160w_160h_1c_1s.webp)

向全栈努力

回复 [@粉色程序员]() :那个打扰一下，那个人是不是可能原名叫张天禹呢

2022-02-22 10:32

**28

**

回复

**

共15条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/9017a35530592a34183871304a0e10d2d7900dd3.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

47794696794_bili

课程资料 链接：https://pan.baidu.com/s/1guj_XDKRMvk2T0Xmdfj0yw 
提取码：6nkw

2020-11-03 15:20**122**回复

![img](https://i1.hdslb.com/bfs/face/aa9d9a10b2714d8e64f22f2d5c8e5f7c2df52bce.jpg@160w_160h_1c_1s.webp)

爱学习的喜哥哥

兄弟，有API的ppt吗

2021-01-15 20:37

**18

**

回复

**

![img](https://i2.hdslb.com/bfs/face/b863304fc9c244b53d32bb98ae95a43b45cc3547.jpg@160w_160h_1c_1s.webp)

bili-首席管理员

跟着pink老师做的在线笔记文档复习使用![[doge]](https://i0.hdslb.com/bfs/emote/3087d273a78ccaff4bb1e9972e2ba2a7583c9f11.png@24w_24h.webp)
HTML部分
HTML(一)：https://blog.csdn.net/Augenstern_QXL/article/details/115419453
HTML5(二)：https://blog.csdn.net/Augenstern_QXL/article/details/115599059
\---------------------------------------------------------------------------------
CSS部分：
CSS(一)：https://blog.csdn.net/Augenstern_QXL/article/details/115560532
CSS三大特性(二)：https://blog.csdn.net/Augenstern_QXL/article/details/115560502
CSS3(三)进阶：https://blog.csdn.net/Augenstern_QXL/article/details/115726577
CSS3(四)高级：https://blog.csdn.net/Augenstern_QXL/article/details/119172527
\----------------------------------------------------------------------------------
JS部分
JavaScript基础班ES6（一）：https://blog.csdn.net/Augenstern_QXL/article/details/115219073
JavaScript基础班ES6（二）：https://blog.csdn.net/Augenstern_QXL/article/details/115344398
JavaScript之DOM(三)（一）：https://blog.csdn.net/Augenstern_QXL/article/details/115416921
JavaScript之BOM（四）：https://blog.csdn.net/Augenstern_QXL/article/details/115406408

2021-07-28 10:31

**77

**

回复

**

![img](https://i1.hdslb.com/bfs/face/a57e2fe80c0bfee7f1188eb2d2b088b5ef513585.jpg@160w_160h_1c_1s.webp)

阿阿阿吳

回复 [@爱学习的喜哥哥]() :能发我一份吗谢谢

2021-08-11 11:12

**8

**

回复

**

共22条回复, 点击查看

![img](https://i2.hdslb.com/bfs/face/1076e90f1f91bac861b40d654c9998698b94ae74.jpg@160w_160h_1c_1s.webp)

![img](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248&spm_id_from=pageDriver&vd_source=2f56f6b382b21a9da12a1f5b716a139f)

handsome-安卿尘

pink老师怎么不更新了

2020-10-19 21:26**47**回复

![img](https://i2.hdslb.com/bfs/face/077ab2fc52c91d11effdb4eecc31a476c8de2d74.jpg@160w_160h_1c_1s.webp)

发布

[![img](https://i2.hdslb.com/bfs/face/834d4a76eedabf7221ceff15c1d207698cdc0fd4.jpg@96w_96h_1c_1s.webp)](https://space.bilibili.com/415434293)

[黑马前端](https://space.bilibili.com/415434293)[** 发消息](https://message.bilibili.com/#whisper/mid415434293)

学习就要拼命克服，相信自己，必会学有所成！

为TA充电

已关注 47.3万

弹幕列表 

![img](https://i0.hdslb.com/bfs/sycp/creative_img/202203/4ba3ceca66686956cc8970a12f54af35.jpg@336w_190h_!web-video-ad-cover.webp)【挑战】每天建模一小时，副业接单养活自己！点击免费领取课程

### 视频选集

(248/473)

**

自动连播 

- [P101-计算机基础导读01:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=1)
- [P202-编程语言09:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=2)
- [P303-计算机基础09:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=3)
- [P404-JavaScript初识导读00:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=4)
- [P505-初始JavaScript07:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=5)
- [P606-浏览器执行JS过程03:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=6)
- [P707-JS三部分组成03:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=7)
- [P808-JS三种书写位置06:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=8)
- [P909-JS注释03:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=9)
- [P1010-JS输入输出语句04:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=10)
- [P1111-变量导读00:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=11)
- [P1212-什么是变量04:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=12)
- [P1313-变量的使用06:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=13)
- [P1414-变量案例03:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=14)
- [P1515-变量案例弹出用户名03:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=15)
- [P1616-变量语法扩展08:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=16)
- [P1717-变量的命名规范09:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=17)
- [P1818-交换2个变量的值07:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=18)
- [P1919-变量小结02:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=19)
- [P2020-数据类型导读00:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=20)
- [P2121-数据类型简介06:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=21)
- [P2222-数字型Number11:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=22)
- [P2323-isNaN02:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=23)
- [P2424-字符串型String07:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=24)
- [P2525-弹出网页警示框02:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=25)
- [P2626-字符串长度以及拼接07:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=26)
- [P2727-字符串拼接加强05:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=27)
- [P2828-显示年龄案例04:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=28)
- [P2929-boolean以及undefined和null07:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=29)
- [P3030-typeof检测变量数据类型05:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=30)
- [P3131-字面量02:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=31)
- [P3232-转换为字符串类型07:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=32)
- [P3333-转换为数字型parseInt和parseFloat07:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=33)
- [P3434-转换为数字型Number和隐式转换03:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=34)
- [P3535-计算年龄案例04:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=35)
- [P3636-简单加法器案例04:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=36)
- [P3737-转换为布尔型02:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=37)
- [P3838-拓展阅读之编译和解释语言的区别03:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=38)
- [P3939-拓展阅读之标识符关键字保留字02:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=39)
- [P4040-课后作业00:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=40)
- [P4101-运算符导读00:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=41)
- [P4202-算数运算符09:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=42)
- [P4303-表达式和返回值03:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=43)
- [P4404-前置递增运算符06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=44)
- [P4505-后置递增运算符03:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=45)
- [P4606-递增运算符练习05:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=46)
- [P4707-前置递增和后置递增小结03:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=47)
- [P4808-比较运算符06:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=48)
- [P4909-逻辑运算符06:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=49)
- [P5010-逻辑运算符练习02:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=50)
- [P5111-逻辑中断逻辑与06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=51)
- [P5212-逻辑中断逻辑或04:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=52)
- [P5313-赋值运算符03:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=53)
- [P5414-运算符优先级07:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=54)
- [P5515-流程控制分支结构导读00:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=55)
- [P5616-流程控制02:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=56)
- [P5717-if分支语句06:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=57)
- [P5818-进入网吧案例02:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=58)
- [P5919-ifelse双分支语句06:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=59)
- [P6020-判断闰年案例06:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=60)
- [P6121-if else if多分支语句07:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=61)
- [P6222-判断成绩案例08:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=62)
- [P6323-三元表达式05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=63)
- [P6424-数字补0案例05:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=64)
- [P6525-switch语句09:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=65)
- [P6626-switch 注意事项05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=66)
- [P6727-查询水果案例04:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=67)
- [P6828-switch和ifelseif 区别05:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=68)
- [P6901-循环导读01:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=69)
- [P7002-循环的目的03:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=70)
- [P7103-for循环语法结构08:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=71)
- [P7204-for循环执行过程06:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=72)
- [P7305-断点调试06:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=73)
- [P7406-for循环重复执行相同代码02:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=74)
- [P7507-for循环重复执行不同代码04:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=75)
- [P7608-for循环重复某些操作05:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=76)
- [P7709-for循环案例07:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=77)
- [P7810-求学生成绩案例（上）06:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=78)
- [P7911-求学生成绩案例（下）05:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=79)
- [P8012-一行打印五颗星星05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=80)
- [P8113-双重for循环执行过程07:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=81)
- [P8214-打印5行5列的星星04:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=82)
- [P8315-打印n行n列的星星02:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=83)
- [P8416-打印倒三角形案例06:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=84)
- [P8517-九九乘法表09:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=85)
- [P8618-for循环小结02:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=86)
- [P8718-while循环06:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=87)
- [P8819-while案例05:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=88)
- [P8920-do while循环04:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=89)
- [P9021-do while案例04:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=90)
- [P9122-循环小结01:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=91)
- [P9223-continue关键字06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=92)
- [P9324-break关键字02:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=93)
- [P9425-命名规范以及语法格式02:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=94)
- [P9526-循环作业02:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=95)
- [P9601-数组导读00:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=96)
- [P9702-什么是数组以及创建方式08:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=97)
- [P9803-访问数组元素06:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=98)
- [P9904-遍历数组05:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=99)
- [P10005-数组长度03:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=100)
- [P10106-计算数组的和以及平均值06:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=101)
- [P10207-求数组中的最大值06:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=102)
- [P10308-数组转换为字符串04:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=103)
- [P10409-数组新增元素07:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=104)
- [P10510-数组存放1~10个值04:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=105)
- [P10611-筛选数组方法106:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=106)
- [P10712-筛选数组方法204:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=107)
- [P10813-删除数组指定元素(数组去重）03:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=108)
- [P10914-翻转数组06:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=109)
- [P11015-复习交换两个变量值02:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=110)
- [P11116-冒泡排序原理04:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=111)
- [P11217-冒泡排序12:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=112)
- [P11318-函数导读00:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=113)
- [P11419-为什么需要函数05:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=114)
- [P11520-函数的使用05:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=115)
- [P11621-利用函数求1~100累加和02:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=116)
- [P11722-函数的参数08:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=117)
- [P11823-利用函数求任意两个数的和以及累加和04:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=118)
- [P11924-函数形参和实参匹配问题06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=119)
- [P12025-函数的返回值return08:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=120)
- [P12126-利用函数求两个数的最大值02:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=121)
- [P12227-利用函数求数组中的最大值05:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=122)
- [P12328-return终止函数并且只能返回一个值06:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=123)
- [P12429-函数返回值2个注意事项02:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=124)
- [P12530-通过榨汁机看透函数02:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=125)
- [P12601-arguments使用08:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=126)
- [P12702-利用函数求任意个数的最大值02:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=127)
- [P12803-利用函数翻转数组03:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=128)
- [P12904-函数封装冒泡排序03:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=129)
- [P13005-利用函数判断闰年03:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=130)
- [P13106-函数可以调用另外一个函数05:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=131)
- [P13207-输出2月份天数06:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=132)
- [P13308-函数的两种声明方式05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=133)
- [P13409-作用域导读00:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=134)
- [P13510-JavaScript作用域07:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=135)
- [P13611-全局变量和局部变量07:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=136)
- [P13712-JavaScript没有块级作用域就02:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=137)
- [P13813-作用域链04:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=138)
- [P13914-作用域链案例05:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=139)
- [P14015-JavaScript预解析导读00:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=140)
- [P14116-预解析13:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=141)
- [P14217-预解析案例12:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=142)
- [P14318-对象导读00:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=143)
- [P14419-什么是对象以及为什么需要对象07:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=144)
- [P14520-利用对象字面量创建对象10:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=145)
- [P14621-变量属性函数方法的区别05:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=146)
- [P14722-利用new Object创建对象04:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=147)
- [P14823-我们为什么需要构造函数04:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=148)
- [P14924-构造函数创建对象（上）10:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=149)
- [P15025-构造函数创建对象（下）05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=150)
- [P15126-构造函数和对象区别03:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=151)
- [P15227-new关键字执行过程03:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=152)
- [P15328-遍历对象05:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=153)
- [P15429-小结和作业01:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=154)
- [P15501-内置对象导读01:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=155)
- [P15602-什么是内置对象03:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=156)
- [P15703-学会查阅MDN文档06:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=157)
- [P15804-数学对象Math最大值方法06:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=158)
- [P15905-封装自己的数学对象04:41](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=159)
- [P16006-Math绝对值和三个取整方法07:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=160)
- [P16107-Math随机数方法10:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=161)
- [P16208-猜数字游戏06:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=162)
- [P16309-Date日期对象的使用08:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=163)
- [P16410-格式化日期年月日星期10:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=164)
- [P16511-格式化日期时分秒06:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=165)
- [P16612-Date总的毫秒数（时间戳）06:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=166)
- [P16713-倒计时（上）07:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=167)
- [P16814-倒计时（下）05:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=168)
- [P16915-数组创建的两种方式04:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=169)
- [P17016-检测是否为数组两种方式06:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=170)
- [P17117-添加数组元素06:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=171)
- [P17218-删除数组元素03:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=172)
- [P17319-筛选数组02:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=173)
- [P17420-数组排序（放到冒泡排序之后讲解）05:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=174)
- [P17521-获取数组元素索引05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=175)
- [P17622-数组去重案例07:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=176)
- [P17723-数组转换为字符串03:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=177)
- [P17824-基本包装类型04:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=178)
- [P17925-字符串不可变04:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=179)
- [P18026-根据字符返回位置03:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=180)
- [P18127-求某个字符出现的位置以及次数06:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=181)
- [P18228-根据位置返回字符04:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=182)
- [P18329-统计出现次数最多的字符（上）09:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=183)
- [P18430-统计出现次数最多的字符（下）03:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=184)
- [P18531-拼接以及截取字符串03:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=185)
- [P18632-替换字符串以及转换为数组06:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=186)
- [P18733-简单数据类型和复杂数据类型导读00:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=187)
- [P18834-数据类型内存分配08:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=188)
- [P18935-简单数据类型传参03:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=189)
- [P19036-复杂数据类型传参05:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=190)
- [P19101-Web APIs简介导读00:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=191)
- [P19202-js基础和Web APIs两个阶段的关联性03:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=192)
- [P19303-API 和 Web API05:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=193)
- [P19404-DOM导读01:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=194)
- [P19505-DOM简介04:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=195)
- [P19606-getElementById获取元素08:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=196)
- [P19707-getElementsByTagName获取某类标签元素11:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=197)
- [P19808-H5新增获取元素方式08:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=198)
- [P19909-获取body和html元素02:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=199)
- [P20010-事件三要素06:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=200)
- [P20111-执行事件过程04:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=201)
- [P20212-操作元素-修改元素内容08:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=202)
- [P20313-innerText和innerHTML的区别06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=203)
- [P20414-操作元素-修改元素属性05:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=204)
- [P20515-分时问候案例06:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=205)
- [P20616-操作元素-修改表单属性06:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=206)
- [P20717-仿京东显示隐藏密码明文案例（上）07:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=207)
- [P20818-仿京东显示隐藏密码明文案例（下）08:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=208)
- [P20919-操作元素-修改样式属性05:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=209)
- [P21020-仿淘宝关闭二维码案例05:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=210)
- [P21121-循环精灵图08:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=211)
- [P21222-显示隐藏文本框内容10:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=212)
- [P21323-使用className修改样式属性09:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=213)
- [P21424-密码框验证信息09:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=214)
- [P21525-操作元素总结以及作业03:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=215)
- [P21601-排他思想（算法）09:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=216)
- [P21702-百度换肤效果08:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=217)
- [P21803-表格隔行变色效果07:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=218)
- [P21904-表单全选取消全选（上）07:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=219)
- [P22005-表单全选取消全选（下）09:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=220)
- [P22106-获取自定义属性值05:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=221)
- [P22207-设置移除自定义属性04:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=222)
- [P22308-tab栏切换布局分析（重要）04:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=223)
- [P22409-tab栏切换制作（上）04:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=224)
- [P22510-tab栏切换制作（下）09:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=225)
- [P22611-H5自定义属性10:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=226)
- [P22712-为什么学习节点操作以及节点简介07:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=227)
- [P22813-节点操作之父节点04:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=228)
- [P22914-节点操作之子节点06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=229)
- [P23015-节点操作之第一个子元素和最后一个子元素06:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=230)
- [P23116-新浪下拉菜单06:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=231)
- [P23217-节点操作之兄弟节点05:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=232)
- [P23318-节点操作之创建和添加节点08:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=233)
- [P23419-简单版发布留言案例08:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=234)
- [P23501-节点操作-删除节点05:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=235)
- [P23602-删除留言案例08:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=236)
- [P23703-节点操作-复制节点04:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=237)
- [P23804-动态生成表格-创建学生数据05:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=238)
- [P23905-动态生成表格-创建行03:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=239)
- [P24006-动态生成表格-创建单元格05:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=240)
- [P24107-动态生成表格-单元格填充数据03:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=241)
- [P24208-动态生成表格-创建删除单元格03:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=242)
- [P24309-动态生成表格-添加删除操作04:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=243)
- [P24410-document.write创建元素（了解）04:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=244)
- [P24511-innerHTML和createElement效率对比07:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=245)
- [P24612-DOM重点核心06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=246)
- [P24713-事件高级导读01:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=247)
- [![img](https://s1.hdslb.com/bfs/static/jinkela/video/asserts/playing.gif)P24814-注册事件两种方式08:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=248)
- [P24915-attachEvent注册事件05:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=249)
- [P25016-删除事件08:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=250)
- [P25117-DOM事件流理论04:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=251)
- [P25218-DOM事件流代码验证07:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=252)
- [P25319-什么是事件对象08:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=253)
- [P25420-e.target和this区别08:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=254)
- [P25521-阻止默认行为06:35](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=255)
- [P25622-阻止事件冒泡04:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=256)
- [P25723-事件委托06:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=257)
- [P25824-禁止选中文字和禁止右键菜单04:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=258)
- [P25925-获得鼠标在页面中的坐标07:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=259)
- [P26026-跟随鼠标的天使07:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=260)
- [P26101-常用的键盘事件06:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=261)
- [P26202-keyCode判断用户按下哪个键07:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=262)
- [P26303-模拟京东按键输入内容案例05:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=263)
- [P26404-模拟京东快递单号查询（上）07:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=264)
- [P26505-模拟京东快递单号查询（下）06:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=265)
- [P26606-BOM导读00:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=266)
- [P26707-BOM概述08:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=267)
- [P26809-页面加载事件08:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=268)
- [P26910-调整窗口大小事件05:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=269)
- [P27011-定时器之setTimeout07:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=270)
- [P27112-回调函数以及5秒之后自动关闭的广告04:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=271)
- [P27213-清除定时器clearTimeout03:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=272)
- [P27314-定时器之setInterval03:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=273)
- [P27415-倒计时效果08:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=274)
- [P27516-清除定时器clearInterval04:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=275)
- [P27617-发送短信案例07:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=276)
- [P27718-this指向问题07:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=277)
- [P27819-js 同步和异步04:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=278)
- [P27920-同步任务和异步任务执行过程06:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=279)
- [P28021-js执行机制06:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=280)
- [P28122-location对象常见属性06:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=281)
- [P28223-5秒钟之后跳转页面06:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=282)
- [P28324-获取URL参数11:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=283)
- [P28425-location常见方法04:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=284)
- [P28526-navigator对象04:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=285)
- [P28627-history对象04:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=286)
- [P28701-PC端网页特效导读00:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=287)
- [P28802-offsetLeft和offsetTop获取元素偏移04:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=288)
- [P28903-offsetWidth和offsetHeight获取元素大小05:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=289)
- [P29004-offset与style区别03:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=290)
- [P29105-获取鼠标在盒子内的坐标06:04](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=291)
- [P29206-拖动模态框（上）06:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=292)
- [P29307-拖动模态框（中）09:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=293)
- [P29408-拖动模态框（下）02:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=294)
- [P29509-仿京东放大镜效果页面结构搭建06:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=295)
- [P29610-仿京东放大镜效果显示隐藏遮挡层和大盒子05:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=296)
- [P29711-仿京东放大镜效果遮挡层跟随鼠标08:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=297)
- [P29812-仿京东放大镜效果限制遮挡层移动范围07:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=298)
- [P29913-仿京东放大镜效果大图片移动08:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=299)
- [P30014-client系列02:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=300)
- [P30115-立即执行函数08:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=301)
- [P30216-淘宝flexibleJS源码分析之核心原理07:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=302)
- [P30317-淘宝flexibleJS源码分析之pageshow事件07:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=303)
- [P30418-scroll系列05:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=304)
- [P30519-仿淘宝固定侧边栏（上）08:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=305)
- [P30620-仿淘宝固定侧边栏（下）10:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=306)
- [P30721-三大系列总结01:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=307)
- [P30822-mouseover和mouseenter区别02:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=308)
- [P30923-动画原理06:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=309)
- [P31024-简单动画函数封装04:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=310)
- [P31125-动画函数-给不同元素记录不同定时器08:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=311)
- [P31201-缓动动画原理05:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=312)
- [P31302-缓动动画基本代码实现04:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=313)
- [P31403-缓动动画多个目标值之间移动07:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=314)
- [P31504-缓动动画添加回调函数05:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=315)
- [P31605-动画函数的使用08:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=316)
- [P31706-网页轮播图-结构搭建06:41](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=317)
- [P31807-网页轮播图-鼠标经过显示隐藏左右按钮06:59](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=318)
- [P31908-网页轮播图-动态生成小圆圈07:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=319)
- [P32009-网页轮播图-小圆圈排他思想03:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=320)
- [P32110-网页轮播图-点击小圆圈滚动图片09:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=321)
- [P32211-网页轮播图-右侧按钮无缝滚动11:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=322)
- [P32312-网页轮播图-克隆第一张图片03:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=323)
- [P32413-网页轮播图小圆圈跟随右侧按钮一起变化05:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=324)
- [P32514-网页轮播图-两个小bug解决方案05:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=325)
- [P32615-网页轮播图-左侧按钮功能制作07:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=326)
- [P32716-网页轮播图-自动播放功能04:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=327)
- [P32817-节流阀以及逻辑中断应用07:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=328)
- [P32918-带有动画的返回顶部10:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=329)
- [P33019-筋斗云案例10:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=330)
- [P33120-移动端网页特效导读01:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=331)
- [P33221-移动端touch触摸事件04:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=332)
- [P33322-移动端TouchEvent触摸事件对象11:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=333)
- [P33423-移动端拖动元素10:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=334)
- [P33501-移动端轮播图-结构搭建05:42](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=335)
- [P33602-移动端轮播图-布局分析07:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=336)
- [P33703-移动端轮播图-滚动图片08:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=337)
- [P33804-移动端轮播图-无缝滚动08:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=338)
- [P33905-classList类名操作08:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=339)
- [P34006-移动端轮播图-小圆点跟随变化05:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=340)
- [P34107-移动端轮播图-手指拖动轮播图07:46](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=341)
- [P34208-移动端轮播图-手指滑动播放上一张下一张图片07:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=342)
- [P34309-移动端轮播图-回弹效果05:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=343)
- [P34410-返回顶部模块制作07:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=344)
- [P34511-移动端click事件300ms延时问题解决方案05:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=345)
- [P34612-fastclick插件使用06:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=346)
- [P34713-swiper插件使用-引入相关文件06:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=347)
- [P34814-移动端轮播图-按照语法规范使用07:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=348)
- [P34915-swiper插件使用-参数更改04:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=349)
- [P35016-移动端其他插件以及使用总结03:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=350)
- [P35117-视频插件zy.media.js的使用07:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=351)
- [P35218-bootstrap轮播图10:34](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=352)
- [P35319-阿里百秀轮播图制作09:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=353)
- [P35420-本地存储导读00:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=354)
- [P35521-本地存储之sessionStorage11:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=355)
- [P35622-本地存储之localStorage05:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=356)
- [P35723-记住用户名案例05:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=357)
- [P35801-jQuery入门导读00:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=358)
- [P35902-JavaScript库03:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=359)
- [P36003-jQuery概述03:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=360)
- [P36104-jQuery基本使用-入口函数07:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=361)
- [P36205-jQuery顶级对象$03:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=362)
- [P36306-DOM对象和jQuery对象05:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=363)
- [P36407-DOM对象和jQuery对象相互转换06:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=364)
- [P36508-jQuery常用API导读01:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=365)
- [P36609-jQuery基本和层级选择器04:10](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=366)
- [P36710-jQuery隐式迭代05:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=367)
- [P36811-jQuery筛选选择器03:55](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=368)
- [P36912-jQuery筛选方法-选取父子元素05:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=369)
- [P37013-新浪下拉菜单05:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=370)
- [P37114-jQuery其他筛选方法07:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=371)
- [P37215-jQuery排他思想03:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=372)
- [P37316-淘宝服饰精品案例07:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=373)
- [P37417-jQuery链式编程07:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=374)
- [P37518-jQuery修改样式css方法06:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=375)
- [P37619-jQuery修改样式操作类05:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=376)
- [P37720-tab栏切换案例07:07](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=377)
- [P37821-jQuery类操作和className区别02:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=378)
- [P37922-jQuery显示与隐藏效果08:08](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=379)
- [P38023-jQuery滑动效果以及事件切换08:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=380)
- [P38124-jQuery停止动画排队stop03:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=381)
- [P38225-jQuery淡入淡出以及突出显示案例07:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=382)
- [P38326-jQuery自定义动画animate方法03:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=383)
- [P38427-王者荣耀手风琴案例布局分析03:33](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=384)
- [P38528-王者荣耀手风琴案例制作08:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=385)
- [P38601-jQuery属性操作10:14](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=386)
- [P38702-购物车模块-全选（上）09:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=387)
- [P38803-购物车模块-全选（下）06:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=388)
- [P38904-jQuery内容文本值04:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=389)
- [P39005-购物车模块-增减商品数量07:37](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=390)
- [P39106-购物车模块-修改商品小计（上）08:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=391)
- [P39207-购物车模块-修改商品小计（中）06:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=392)
- [P39308-购物车模块-修改商品小计（下）03:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=393)
- [P39409-jQuery遍历对象each方法09:00](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=394)
- [P39510-jQuery遍历数据$.each03:40](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=395)
- [P39611-购物车模块-计算总件数和总额09:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=396)
- [P39712-创建、添加、删除元素08:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=397)
- [P39813-购物车模块-清理购物车07:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=398)
- [P39914-购物车模块-选中商品添加背景颜色04:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=399)
- [P40015-jQuery尺寸方法04:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=400)
- [P40116-jQuery位置方法06:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=401)
- [P40217-jQuery被卷去头部方法06:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=402)
- [P40318-带有动画的返回顶部03:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=403)
- [P40419-电梯导航案例-显示隐藏电梯导航04:44](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=404)
- [P40520-电梯导航案例-点击滚动目标位置08:53](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=405)
- [P40621-电梯导航案例-点击当前li添加current类03:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=406)
- [P40722-电梯导航案例-滑动页面电梯导航自动添加current类05:52](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=407)
- [P40823-电梯导航案例节流阀(互斥锁)06:27](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=408)
- [P40901-jQuery事件导读00:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=409)
- [P41002-事件处理on绑定一个或者多个事件06:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=410)
- [P41103-on实现事件委派和给动态元素绑定事件06:13](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=411)
- [P41204-微博发布案例10:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=412)
- [P41305-off解绑事件05:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=413)
- [P41406-jQuery自动触发事件05:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=414)
- [P41507-jQuery事件对象02:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=415)
- [P41608-jQuery其他方法导读00:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=416)
- [P41709-jQuery对象拷贝extend（选放）11:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=417)
- [P41810-jQuery多库共存05:43](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=418)
- [P41911-瀑布流插件使用09:19](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=419)
- [P42012-图片懒加载技术10:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=420)
- [P42113-全屏滚动插件使用（选放）11:16](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=421)
- [P42214-bootstrap组件05:02](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=422)
- [P42315-bootstrapJS插件10:29](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=423)
- [P42416-阿里百秀10:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=424)
- [P42517-todolist布局功能需求分析06:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=425)
- [P42618-todolist核心思路以及本地存储格式10:17](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=426)
- [P42719-todolist按下回车读取本地存储数据08:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=427)
- [P42820-todolist按下回车保存最新数据到本地存储06:31](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=428)
- [P42921-todolist本地存储数据渲染加载到页面中10:38](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=429)
- [P43022-todolist点击删除按钮获取当前索引号08:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=430)
- [P43123-todolist点击删除按钮完成删除操作04:49](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=431)
- [P43224-点击复选框修改相应数据done属性08:23](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=432)
- [P43325-todolist正在进行和已经完成事项制作05:01](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=433)
- [P43426-todolist统计正在进行和已经完成事项个数05:48](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=434)
- [P43501-录制视频作用介绍01:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=435)
- [P43602-点位区域布局样式10:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=436)
- [P43703-地图区域布局样式06:39](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=437)
- [P43804-用户区域布局样式07:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=438)
- [P43905-订单区域布局样式08:41](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=439)
- [P44006-销售区域布局样式11:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=440)
- [P44107-渠道与季度布局样式22:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=441)
- [P44208-排行区域布局样式-参考32:56](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=442)
- [P44301-数据可视化项目导读01:03](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=443)
- [P44402-什么是数据可视化05:25](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=444)
- [P44503-数据可视化项目概述04:24](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=445)
- [P44604-ECharts简介04:18](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=446)
- [P44705-ECharts基本使用11:20](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=447)
- [P44806-选择不同类型图表05:58](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=448)
- [P44907-ECharts相关配置（上）10:05](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=449)
- [P45008-ECharts-grid配置08:54](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=450)
- [P45109-ECharts相关配置（中）10:21](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=451)
- [P45210-ECharts相关配置（下）series11:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=452)
- [P45311-折线图生成以及配置项总结05:09](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=453)
- [P45412-数据可视化项目适配方案分析05:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=454)
- [P45513-数据可视化项目适配方案08:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=455)
- [P45614-项目准备以及按照自动刷新浏览器插件04:57](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=456)
- [P45715-可视化项目-body和viewport制作09:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=457)
- [P45816-可视化项目column列容器03:50](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=458)
- [P45917-边框图片使用场景以及切割原理08:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=459)
- [P46018-边框图片使用语法09:47](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=460)
- [P46119-公共面板样式制作（上）08:36](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=461)
- [P46220-公共面板样式制作（下）09:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=462)
- [P46321-通过类名调用字体图标06:06](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=463)
- [P46422-数据可视化项目-概览区域模块制作12:15](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=464)
- [P46523-数据可视化项目-监控区域布局分析05:51](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=465)
- [P46624-数据可视化项目-监控区域tab栏切换分析11:30](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=466)
- [P46725-数据可视化项目-监控区域无缝滚动11:26](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=467)
- [P46801-点位分布point模块-布局05:12](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=468)
- [P46902-点位分布point-引入图表08:45](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=469)
- [P47003-ECharts饼形图-tooltip参数含义08:32](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=470)
- [P47104-ECharts饼形图-series参数含义06:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=471)
- [P47205-点位分布模块-定制配置(上)06:11](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=472)
- [P47306-点位分布模块-定制配置(下)07:28](https://www.bilibili.com/video/BV1Sy4y1C7ha?p=473)

![审美佳，技术强，脾气好，是哪个程序员这么宝藏？](https://i0.hdslb.com/bfs/feed-admin/276af9a950a93889be31c698a8fdfd5add8b2b82.jpg@336w_190h_!web-video-rcmd-cover.webp)

审美佳，技术强，脾气好，是哪个程序员这么宝藏？

bilibili课堂

[![【血泪建议】自学前端越早知道越好的事情!](https://i1.hdslb.com/bfs/archive/1845e6f24b6a0547fad96de181b45fa323bcd25b.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1WF41137fe/?spm_id_from=333.788.recommend_more_video.0)

01:55

【血泪建议】自学前端越早知道越好的事情!

[2次元诺诺](https://space.bilibili.com/1837989886/)

2.7万165

[![黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程](https://i2.hdslb.com/bfs/archive/8a334edc5a07afef88d62e8c938682a03e2f695d.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV14J4114768/?spm_id_from=333.788.recommend_more_video.1)

56:03:20

黑马程序员pink老师前端入门教程，零基础必看的h5(html5)+css3+移动端前端视频教程

[黑马前端](https://space.bilibili.com/415434293/)

1399.6万46.4万

[![前端大神尤雨溪授权的HTML+Vue+JS全套教程，整整600集，学完即可就业](https://i2.hdslb.com/bfs/archive/84f32865ed15a77f0e952ec006c106f2b5f2d600.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Ka411o7xR/?spm_id_from=333.788.recommend_more_video.2)

12:06:55

前端大神尤雨溪授权的HTML+Vue+JS全套教程，整整600集，学完即可就业

[头顶猫的美少女](https://space.bilibili.com/1807606680/)

3.3万177

[![每次我撑不下去的时候，都会打开这个视频，要是在学前端之前能知道这些就好了](https://i0.hdslb.com/bfs/archive/c52dc2c963a02e43800027cd93ad633018215673.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV16W4y1r75v/?spm_id_from=333.788.recommend_more_video.3)

02:39

每次我撑不下去的时候，都会打开这个视频，要是在学前端之前能知道这些就好了

[草莓蛋糕来了](https://space.bilibili.com/2074760195/)

6.2万158

[![【前端教程】JavaScript入门，94集完整版教程（JS核心语法 、DOM、BOM 、 ES6语法）](https://i2.hdslb.com/bfs/archive/bc771c492575a79bc58c6a54ed66e4df67fa09fd.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1bB4y1t7c5/?spm_id_from=333.788.recommend_more_video.4)

40:09:13

【前端教程】JavaScript入门，94集完整版教程（JS核心语法 、DOM、BOM 、 ES6语法）

[前端易学](https://space.bilibili.com/1663033972/)

1.0万11

[![自学前端半年，只会html、css、js、vue就找到了一份还不错的工作！](https://i0.hdslb.com/bfs/archive/a8dae1268fcbd76ca7c4d999200ab9d58f3bb597.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV15R4y1P7pR/?spm_id_from=333.788.recommend_more_video.5)

02:37

自学前端半年，只会html、css、js、vue就找到了一份还不错的工作！

[前端最后的希望](https://space.bilibili.com/1629753361/)

5.2万234

[![【2022最新版】JavaScript入门到精通全套教程（BOM_DOM_ES6_JS）](https://i0.hdslb.com/bfs/archive/1758c709e5bae9b32be814f8df7c45d18d5b5670.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV193411P76J/?spm_id_from=333.788.recommend_more_video.6)

40:35:01

【2022最新版】JavaScript入门到精通全套教程（BOM_DOM_ES6_JS）

[写网页的叮叮](https://space.bilibili.com/1712879676/)

1.8万199

[![黑马前端jquery-pink老师](https://i1.hdslb.com/bfs/archive/197612d24fc8db1a4253654ef70717ac5726b833.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1wo4y1R7t6/?spm_id_from=333.788.recommend_more_video.7)

8:06:03

黑马前端jquery-pink老师

[LaiDiang](https://space.bilibili.com/17187427/)

4.2万324

[![2022最新完整版，HTML+CSS+js教程95集完全入门达到web前端工程师水平，7天轻松搞定，堪称入门级神作](https://i2.hdslb.com/bfs/archive/e5e303009563927365c467fd08a4460a4cde6456.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Er4y1V7KA/?spm_id_from=333.788.recommend_more_video.8)

16:13:10

2022最新完整版，HTML+CSS+js教程95集完全入门达到web前端工程师水平，7天轻松搞定，堪称入门级神作

[百事可瑶_](https://space.bilibili.com/1830568085/)

7.8万989

[![前端 JavaScript基础入学从入门到精通 2023新 js教程含实战 项目 网页设计 轮播图 程序员编程新手入门必看高级完整版视频【渡一教育】](https://i2.hdslb.com/bfs/archive/3e884a22e164aa208b011faa84fefb2c34f2dcb8.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1f4411R7M5/?spm_id_from=333.788.recommend_more_video.9)

54:15:12

前端 JavaScript基础入学从入门到精通 2023新 js教程含实战 项目 网页设计 轮播图 程序员编程新手入门必看高级完整版视频【渡一教育】

[渡一教育-Web前端开发](https://space.bilibili.com/384876532/)

23.3万7526

[![推荐一个练习事件循环的网站，好    用     ！！](https://i0.hdslb.com/bfs/archive/8e9f23e57704da00f2156d24a5a465d4069e8c1b.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Zg411z7cv/?spm_id_from=333.788.recommend_more_video.10)

04:03

推荐一个练习事件循环的网站，好 用 ！！

[黑马前端](https://space.bilibili.com/415434293/)

1.5万3

[![尚硅谷JavaScript基础&实战丨JS入门到精通全套完整版](https://i2.hdslb.com/bfs/archive/41254610da8626866a1e879c8f57f59167fd2fae.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1YW411T7GX/?spm_id_from=333.788.recommend_more_video.11)

39:39:21

尚硅谷JavaScript基础&实战丨JS入门到精通全套完整版

[尚硅谷](https://space.bilibili.com/302417610/)

541.9万15.9万

[![前端学到什么程度就可以找工作了](https://i0.hdslb.com/bfs/archive/9a1688e169eb07cd11de45000812456a84dce7ae.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1xh411s71M/?spm_id_from=333.788.recommend_more_video.12)

02:09

前端学到什么程度就可以找工作了

[小鹿线前端胡老师](https://space.bilibili.com/609838079/)

13.2万84

[![当男程序员和女程序员开始交往后.....](https://i1.hdslb.com/bfs/archive/c5a404441be8fc652a71cd3b4a368baf49dc1257.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1qK4y1r713/?spm_id_from=333.788.recommend_more_video.13)

00:28

当男程序员和女程序员开始交往后.....

[佐玄先生](https://space.bilibili.com/152315179/)

514.9万419

[![2022最新版JavaScript入门到精通，前端js全套基础&实战教程](https://i0.hdslb.com/bfs/archive/0035660795e1456fae0249e8b0ab8950e8b5fc65.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1Kq4y1e7d2/?spm_id_from=333.788.recommend_more_video.14)

18:15:28

2022最新版JavaScript入门到精通，前端js全套基础&实战教程

[黑马前端教程](https://space.bilibili.com/513719037/)

28.9万9099

[![这三种人，千万别学前端开发](https://i1.hdslb.com/bfs/archive/d3b617b983d6dfa8ddf2cf17c494e57eca2da438.png@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1P54y1k7sa/?spm_id_from=333.788.recommend_more_video.15)

06:17

这三种人，千万别学前端开发

[老尚带你学前端](https://space.bilibili.com/405768506/)

9.8万155

[![(资料私信关注)黑马前端就业班(pink老师)第二部分](https://i1.hdslb.com/bfs/archive/65e85b5ec05e159b9c9ab31e743a7e6b5b739697.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1hy4y187zi/?spm_id_from=333.788.recommend_more_video.16)

20:59:04

(资料私信关注)黑马前端就业班(pink老师)第二部分

[GrayCoder](https://space.bilibili.com/1255330937/)

1.1万7

[![【前端小技巧】纯css实现电梯导航](https://i1.hdslb.com/bfs/archive/f9c33811b591a2f822320676565ac373b0e372a0.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1YR4y1y7mk/?spm_id_from=333.788.recommend_more_video.17)

02:52

【前端小技巧】纯css实现电梯导航

[黑马前端](https://space.bilibili.com/415434293/)

3.0万15

[![黑马WEB前端PINK老师全系列JavaScript 篇](https://i0.hdslb.com/bfs/archive/f313bcc9089bc140e55ee77466d14f4a0d0194c4.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV11t4y1i7ht/?spm_id_from=333.788.recommend_more_video.18)

52:15:56

黑马WEB前端PINK老师全系列JavaScript 篇

[一朵小红花emm](https://space.bilibili.com/254046664/)

12.1万1722

[![jQuery不要学](https://i0.hdslb.com/bfs/archive/0bf17262c272b1fab233da0713c7e0ad240a2653.jpg@336w_190h_!web-video-rcmd-cover.webp)](https://www.bilibili.com/video/BV1bf4y1T7Ss/?spm_id_from=333.788.recommend_more_video.19)

02:08

jQuery不要学

[沉浸式编程教学](https://space.bilibili.com/325887266/)

3.3万33

展开

![img](https://i0.hdslb.com/bfs/banner/374857eaf50a1bf7a3d56b24e2953467da50652f.png@700w_350h_!web-video-right-bottom-ad.webp)热点大放送，投稿赢奖金！

小窗

客服

顶部

![img](https://downloads.xinrern.cn/close_sqoxk.png)

![img](https://downloads.xinrern.cn/dsgdY1_dzcbt.gif)