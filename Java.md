### Java

##### 命令介绍：

###### cd:

…/表示往前退

进入根目录的方式；

放回上次目录的方法

TAB按键的用法：用来补全文件名

###### dir：

###### 用来显示目录中的文件

###### cls：

清除屏幕中显示的内容

###### ipconfig-all:

显示当前所用的网络设备信息

###### netstat-ano

显示应用的协议、端口以及监听情况

##### 目录结构

Program Files：计算机软件的默认安装目录

Windows目录：系统文件存放目录（勿乱动）

Users目录：用户文件存放目录

##### 常量

![image-20230724165152203](Java.assets/image-20230724165152203.png)

##### 基本数据类型

![image-20230725144154388](Java.assets/image-20230725144154388-16902673174501.png)

##### 应用数据类型

![image-20230724165407484](Java.assets/image-20230724165407484-16901888487742.png)

##### 变量

![image-20230724165444220](Java.assets/image-20230724165444220-16901888861453.png)

##### 代码注释：

1./* 

​			  多行注释

​		 */

2.//单行注释

##### 变量的基本使用

![image-20230724170252161](Java.assets/image-20230724170252161-16901893734314.png)

##### 交换变量

```java
swap(){
    a ^ = b;
    b ^ = a;
    a ^ = b;
}
```

##### 运算符

![image-20230724171318927](Java.assets/image-20230724171318927-16901900001125.png)

##### 键盘输入内容取值

```Java
import java.util.Scanner
    
  public class scanner{
      public static void main(String[] args){
          int  a = new;
          Scanner(System.in).nextInt();
          //键盘获取值
      }
  }
```

##### 常量为什么要写在==的前边

![image-20230724173916804](Java.assets/image-20230724173916804-16901915580646.png)

##### 用户输入一个年份和月份，反馈对应的天数

![image-20230724174254685](Java.assets/image-20230724174254685-16901917761717.png)

#### 数组

![image-20230724175600288](Java.assets/image-20230724175600288-16901925612178.png)

##### 数组的特性

![image-20230724175929802](Java.assets/image-20230724175929802-16901927723439.png)

```java
//max number
public class one {
    public static void main(String[] args) {
        Random ran = new Random();
        int[] arr = new int[10];
        for (int i = 0;i<arr.length; i++) {
            arr[i] = ran.nextInt(100);
        }
        for (int j = 0; j < arr.length; j++) {
            System.out.print(arr[j] + " ");
        }
        System.out.println();
        int max = arr[0];
        for (int k = 0; k < arr.length; k++) {
            if(arr[k] > max)
            max = arr[k];
        }
        System.out.print(max);
    }
    
}
```

##### 逆序存储

![image-20230724182756788](Java.assets/image-20230724182756788-169019447861110.png)

##### 有序数组插入数字仍然有序

![image-20230724183323723](Java.assets/image-20230724183323723-169019480552011.png)

```java
//冒泡排序
public static void main(String[] args) {
        Random ran = new Random();
        int[] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = ran.nextInt(100);
        }
        for (int i = 0; i < arr.length; i++) {
            System.out.print(arr[i]+" ");
        }
        System.out.println("\n=======================");
        for (int i = 0; i < arr.length-1; i++) {
            for (int j = i; j < arr.length; j++) {
                if(arr[i]>arr[j]){
                    int temp =arr[i];
                    arr[i] = arr[j];
                    arr[j] = temp;
                }
            }
        }
        for (int j = 0; j < arr.length; j++) {            
            System.out.print(arr[j]+" ");
        }
    }
```

##### 二维数组的转置

![image-20230724185723523](Java.assets/image-20230724185723523-169019624599812.png)

##### 增强for循环的使用

![image-20230724185917539](Java.assets/image-20230724185917539-169019635941513.png)

#### 方法

![image-20230724190211850](Java.assets/image-20230724190211850-169019653290615.png)

![image-20230724190918560](Java.assets/image-20230724190918560-169019696048516.png)

####  面向对象

##### 面向对象的概念

1.类是对象的抽象

2.对象是类的实例

3.面向对象的三大特性：封装、继承、多态

##### 类的定义

```java
public class test {
    //成员变量（属性）
    public String name;
    public String age;

    //成员方法
    public void fun(/*形参列表 */){
        /*方法体 */
    }
}
```

#### 成员变量和局部变量

##### 成员变量

1.在类内、方法体外声明的变量

2.有默认值时，各种形态为0或空

##### 局部变量

1.在方法体内声明的变量

2.没有默认值，在没对其进行初始化之前不能使用，否则报错

##### 成员方法和静态方法

```java
{
    Person p = new Person();
    //通过对象.出来的是成员方法
    //没有static关键字修饰，通过对象.的方法进行调用
    p.eat();
    p.sleep();
    
    
    //用static关键字修饰的方法为静态方法，不通过对象调用，通过类名.的方式调用
    //通过类名.出来的是静态方法
    Person.drink();
}
```

122节（返回类的对象）

##### this的用法

如果局部变量和成员变量同名，局部变量会屏蔽掉成成员变量，若一定要使用成员变量，可以通过**this**关键字进行访问，**this**的作用可以理解为当前对象自己。

#### 封装

通过封装可以保证数据的安全可靠。

##### 方法

将一些功能整理到一个方法中，方便再次使用，提高嗲吗的可服用率

##### private

将类中的一些成员私有化，保证成员数据的准确性

set和get方法（编译器自动生成）（在idea当中使用Alt+insert使用）

​    1.set方法：用来设置私有成员属性的值

​    2.get方法：用来获取私有成员属性的值

#### 构造方法

##### 特点：

1.与类同名

2.无返回值

3.如果不手动创建构造方法，则系统默认生成一个无参构造方法

4.构造方法不需要手动调用，在类创建对象时被自动调用

5.如果手动创建了构造方法，系统则不再生成无参的构造方法

6.构造方法支持重载

##### 用处

初始化类中的成员属性（尽量在类中使用set方法对成员属性赋值）

当输出一个对象的时候，如果有toString 方法的重写，将会被自动调用

#### 继承

##### 作用（意义）

共性抽取：子类抽取父类当中public、protected修饰的成员（成员属性和成员方法）

##### 特点

子类可以继承（拥有）父类当中public、protected修饰的所有成员，并且子类可以有自己的成员，自己的成员在父类中是不可以使用的。

##### 格式

```java
/******************************/
public class father{
    //...
}
/********************************/
public class son extends father{
    //...
}



super()//调用父类的构造方法
this()//可以调用当前类的构造方法
```

##### **this与super的区别** 

super: 它引用当前对象的直接父类中的成员（用来访问直接父类中被隐藏的父类中成员数据或函 数，基类与派生类中有相同成员定义时如：super.变量名 super.成员函数据名（实参） this：它代表当前对象名（在程序中易产生二义性之处，应使用this来指明当前对象；如果函数的 形参与类中的成员数据同名，这时需用this来指明成员变量名）

 super()和this()类似,区别是，super()在子类中调用父类的构造方法，this()在本类内调用本类的其 它构造方法。 super()和this()均需放在构造方法内第一行。 尽管可以用this调用一个构造器，但却不能调用两个。 this和super不能同时出现在一个构造函数里面，因为this必然会调用其它的构造函数，其它的构造 函数必然也会有super语句的存在，所以在同一个构造函数里面有相同的语句，就失去了语句的意 义，编译器也不会通过。 

this()和super()都指的是对象，所以，均不可以在static环境中使用。包括： static变量,static方法，static语句块。 从本质上讲，this是一个指向本对象的指针, 然而super是一个Java关键字。

##### 继承的权限

![image-20230725144238921](Java.assets/image-20230725144238921-16902673617532.png)

### 抽象和接口

#### 抽象abstract

##### abstract修饰符

1.用abstract修饰的方法叫做抽象方法，不能有方法体

2.拥有抽象方法的类必须是抽象类

3.抽象类中可以存在不是抽象方法的普通方法

4.抽象类必须被继承

5.抽象方法必须在子类中重写

6.抽象类不能直接创建对象，需要通过子类对象进行调用

##### 举例说明

图形：只要是图形就有计算面积和周长的方法，但是计算的公式却都不相同；

动物：每种动物都能够吃和运动，但是不同的动物吃的东西不同，运动的方式也不同。（以图形和动物为例，他们都有固定的行为，但是行为的具体形式不同，那么在程序中类似的问题就可以以抽想的方式来表现）

#### 接口interface

接口interface是一种公共的规范，是一种引用数据类型

##### 接口的定义

```java
public interface 接口名称{
    /*成员*/
}
```

##### 接口的成员

接口中的常量

​	格式：public static final常量名称 = 值

​	注意事项：

​				1.final修饰的变量不能改变

​				2.接口中的常量必须赋值

​				3.常量使用大写字母、匈牙利命名法（OPEN_DOOR)

**接口中的抽象方法必须用public abstract 修饰******

接口中的默认方法

​	格式： public default 返回值类型  方法名（参数列表）{方法体}

注意事项：

​		1.用于接口升级

​		2.通过实现类的对象可以直接调用

​		3.默认方法也可以在实现类中进行重写

​		4.JAVA8.0以上版本

##### 接口的实现

接口的实现格式

```java
public class 类名称 implements 接口名称{
    /*......*/
}
```

注意事项：

​		1.实现接口的类中必须重写接口中所有的抽象方法

​		2.通过创建“实现类”对象来调用接口中的成员

​		3.如果实现类中没有重写接口中所有的抽象方法，那么这个类一定是个抽象类

##### 一个类可以同时实现多个接口

```java
public class 类名 implements 接口1，接口2{
    /*.........*/
}
```

注意事项：

​		实现多个接口的时候需要重写实现所有接口当中的所有方法

​		如果存在重复的默认方法，那么实现中必须对重复的方法进行重写

##### 接口中的默认构造方法

格式：public default 返回值类型 方法名（参数列表）{方法体}

注意事项：

​		1.用于接口升级

​		2.通过实现类的兑现可以直接调用

​		3.默认方法也可以实现类中进行重写

​		4.java8.0以上版本（包含）

##### 接口中的静态方法

格式：public static 返回值类型 方法名（参数列表）{方法体}

注意事项：

​		1.不能通过对象进行调用

​		2.通过类名直接调用

​		3.Java8.0以上版本（不包含）

##### 接口中的私有方法

格式：private [static] 返回值类型 方法名（参数列表）{}

注意事项：

​			1.私有方法只提供本类中使用

​			2.普通私有方法：解决普通default方法间的代码复用问题

​			3.静态私有方法：解决静态default方法的代码复用问题

​			4.java8.0以上版本（不包含）

##### final的使用

修饰类：用final修饰的类不能被继承

修饰局部变量： 用final修饰的局部变量一旦被赋值则不允许修改

修饰成员变量：用final修饰的成员变量必须初始化一个值

​		直接赋值

​		构造方法赋值

修饰方法：用final修饰的方法不能被重写

###    多态

##### 格式

```java
父类名，对象名 = new 子类名（）;
父类接口名，对象名 = new 子类名();
```

##### 多态调用成员方法

编译看左，运行看右

##### 多态调用成员属性

编译运行都看左

#### 对象的的上下转型

##### 向上转型

向上转型就是创建一个子类对象，把它当做父类对象来使用

**注意事项**：

​			向上转型一定是安全的

​			弊端：无法调用子类特有方法

##### 向下转型

向下转型就是还原子类对象，用强制类型转换的方法实现。

**注意事项：**

​		用谁new的就还原成谁

​		还原之前使用 对象名instanceof类名 进行判断，避免出错。

#### 内部类

**内部类的访问特点**

​		内部类可以直接访问外部类的成员，包括私有成员

​		外部类要访问内部类的成员，必须要创建对象

```java
public class Demo {
    private int num = 9527;
    //定义内部类
    public class Inner{
        public void showNum(){
            System.out.println(num);
        }
    }
    public void method() {
        Inner inner = new Inner();
        inner.showNum();
    }
    public static void main(String[] args) {
        new Demo().method();
    }
}
```

![image-20230727145215328](Java.assets/image-20230727145215328-16904407366541.png)

#### 匿名内部类

前提：存在一个类或者接口，这里的类可以是具体的也可以是抽象类

本质：匿名内部类的实际上就是一个继承类该类或者实现该类接口的子类匿名对象

```java
//格式
new 类名/借口名(){
    重写方法；
}
//EX：
new Inter(){
    public void show(){
        //方法体
    }
}
```

#### 常用类

##### 包装类

自动装箱和拆箱

​		装箱：把基本数据类型转换为对应的包装类类型

​		拆箱：吧包装类类型转换为对应的基本数据类型

```java
public static void main(String[] args){
    //装箱
    Integer i01 = Integer.valueof(9527);//手动装箱
    Integer i02 = 100;//自动装箱 JDK>1.5
    
    //拆箱
    i02 = i01.intValue() +9527;//手动拆箱
    i02 += 9527;//自动拆箱
    
    System.out.println(i01);
    System.out.println(i02);
    
    Integer i03 = null;
    if(i03 != null)//解决空指针异常
        i03 +=9527;
}
```

#### String

字符串类

无论是常量还是变量在Java中都是字符串对象

##### 字符串类的特点

字符串不可边，他们的值在创建之后是不能被改变的

虽然String的值是不可变的，但是他们是共享的

字符串效果上相当于字符数组（char[])<=JDK8,实际底层原理是字节数组（byte[])>=JKD9

##### 常用构造方法

| 方法名                     | 说明                                      |
| -------------------------- | ----------------------------------------- |
| public string（）          | 创建一个空白字符串对象，不含有任何内容    |
| public string（char[] chs) | 根据字节数组内容，来创建字符串对象        |
| public string (byte[] bys) | 根据字节数组内容，来创建字符串对象        |
| String str = “Hello”       | 直接赋值的方式创建字符对象，内容就是Hello |

![image-20230727162825378](Java.assets/image-20230727162825378-16904465069572.png)

##### String对象的特点

1.通过new穿件的字符串对象，每一次new，JVM都会申请一个新的内存空间，虽然内容相同但是地址不同。

2.以“”方式给出的字符串，只要字符序列相同（包括顺序和大小写），无论在程序中出现多少次，JVM都只会建立一个String对象，并存放在字符串池汇总进行维护。

##### String的比较

用==（关系运算符）作比较

​		基本数据类型：比较的是**数据值**是否相同

​		引用数据类型：比较的是**地址值**是否相同

用public boolean equals (String str)作比较

​		讲此字符串与给定字符串对象作比较，比较其中存储的内容是否相同

##### 字符串常用方法

![image-20230727164508586](Java.assets/image-20230727164508586-16904475103913.png)

reverse（）//字符串反向存储

![image-20230727185502741](Java.assets/image-20230727185502741-16904553042901.png)

![image-20230727190632464](Java.assets/image-20230727190632464-16904559948644.png)

![image-20230727190823503](Java.assets/image-20230727190823503-16904561061536.png)

#### Object类

| 方法名                                     | 说明                                         |
| ------------------------------------------ | -------------------------------------------- |
| public String tostring                     | 将类成员编辑成字符串，通常在自定义类中被重写 |
| public Boolean equals(Object obj1,Object2) | 对比两个对象是否相等，通常在自定义类中被重写 |

#### System

```java
System.exit(0);//终止当前正在进行的Java虚拟机

System.currentTimeMillis();//获取当前系统时间戳 单位ms
```

![image-20230727200343735](Java.assets/image-20230727200343735-16904594268697.png)

![image-20230727200620325](Java.assets/image-20230727200620325-16904595825718.png)

![image-20230727201415401](Java.assets/image-20230727201415401.png)

### FILE

#### 构造方法

File(String pathname)-通过将给定的路径名字符串转换为有抽象路径名来穿件新的File实例

File(String parent,String chlid)-从父类路径名字符串和自路径名字符串创建新的File实例

File(File parent,String child)-从父类抽象路径和自路径名字符串创建的File实例

```java
public static void main(String[] args){
    File file01 = new File("./a.txt");
    System.out.println(file01);
    
    File file02 = new File("./","a.txt");
    System.out.println(file02);
    
    File file03 = new File("./");
    FIle file04 = new FIle(file03,"a.txt");
    System.out.println(file04);
}
```

#### File类的创建功能

createNewFile():创建文件

mkdir():创建目录

mkdirs():创建多级目录

```java
public static void main(String[] args) throws IOException{
    File f1 = new File(".\\a.txt");
    //如果存在则返回true，并创建文件，如果不存在则放回false
    System.out.prinln(f1.creatNewFile());
    System.out.prinln("======================");
    
    File f2 = new File(".\\testDir");
    System.out.println(f2.mkdir());
    System.out.println("=========================");
    
    File f3 = new File(".\\Hello\\World");
    System.out.println(f3.mkdirs());
    
    //注意：目录名和文件名也不能重复，否则穿件不会成功
}18
```

#####  File类的判断和获取功能

·isDirectory（）: 是否为目录
		·isFile()是否为文件
		exists():是否存在
		getAbsolutePath（）: 返回绝对路径
		·getPath(): 返回给定的路径名字符串
		·getName(): 返回File封装的文件或目录名
		list(): 返回目录文件列表(字符串)
		listFiles（): 返回文件列表(对象)

![image-20230728180837117](Java.assets/image-20230728180837117.png)

### IO流

#### io流的分类

IO流概述：

IO：输入/输出(input/output)

流：是一种抽象的概念、是对数据传输的总称、就是说数据在设备的传输成为流，流的本质是数据的传输

IO流就是用来处理设备间数据传输问题的   常见的应用：文件的复制、上传、下载等

**根据数据的流向**

​			1.输入流：读数据

​			2.输出流：写数据

**根据数据类型**

​			字节流（万能流）：（读不懂的数据用字节流）

​						字节输入流

​						字节输出流

​			字符流（能读懂的用字符流）

​						字符输入流

​						字符输出流

#### 字节流数据

字节流抽象类

​			1.InputStream:字节输入流

​			2.OutputStream:字节输出流

​			3.子类名称特点：子类名称都是以父类名称作为子类名称的后缀

![image-20230729121051014](Java.assets/image-20230729121051014-16906038530111.png)

![image-20230729133443973](Java.assets/image-20230729133443973-16906088852972.png)

![image-20230729134303362](Java.assets/image-20230729134303362-16906093858573.png)

![image-20230729134727295](Java.assets/image-20230729134727295-16906096493254.png)

#### 字节输入输出流缓冲区

BufferedOutputStream:该类实现缓冲输出流。通过设置这样的输出流，应用程序可以向底层输出流写入字节流，而不必写的每个字节而导致底层系统的调用。

BufferedinputStream:创建BufferedinputStream将创建一个内部缓冲区数组。当从流中读取或效果字节时，内部缓冲区将根据需要从所包含的输入流中重新填充，一次多个字节。

![image-20230729135935134](Java.assets/image-20230729135935134-16906103769625.png)

#### 字符串中的编码与解码

##### 编码

getBytes():使用平台(IDEA)默认字符集

getBytes(String charsetName):设置字符集

##### 解码

String(byte[] bytes);使用平台(IDEA)默认字符集解码

String(byte[]bytes,String charsetName);使用指定字符解码

```java
public static void main(String[] args) throws UnsupportedEncodingException{
    String s01 = "iceWan is 冰";
    //byte[] bytes = s01.getBytes("UTF-8");
    byte[] bytes = s01.getBytes("GBK");
    //字节流当中汉子的字符编码是负数值
    
    System.out.println(Arrays.toString(bytes));
    
    System.out.println(new String(bytes));//默认字符集
    system.out.pirntln(new String(bytes,"GBK"));
}
```

#### 字符流的编码解码

InputStreamReader:字符输入流

OutputStreamWriter:字符输出流

```java
    public static void main( String[] args ) throws IOException {
        final  String SRC = "Demo01-测试\\test.txt";
        FileOutputStream fos = new FileOutputStream(SRC);
        //OutputStreamWriter osw  = new OutputStreamWriter(fos);
        //OutputStreamWriter osw = new OutputStreamWriter(fos,"UTF-8");
        OutputStreamWriter osw = new OutputStreamWriter(fos,"GBK");

        osw.write("name");
		osw.flush();
        osw.close();

        //==============================读写分割线====================

        FileOutputStream fis = new FileOutputStream(SRC);
        InputStreamReader isr = new InputStreamReader(fis, "GBK");

        int ch;
        while((ch = isr.read()) != -1){
            System.out.print((char)ch);
        }
        isr.close();
    }
```

##### 缓冲区特有的功能

BufferedWriter类-void newLine():行分隔符，根据不同系统写入分隔符

BufferedReaderl类-String readLine():读一行文字，不包括换行符，读完返回null

```java
putlic static void main(String[] args) throws IOException{
    BufferedWriter bw= new BufferedWriter(new FileWriter("Demo01-测试\\test.txt"));
    BufferedReader br = new BufferedReader(new FileReader("Demo01-测试\\test.txt"));
    
    bw.write("Hello");
    bw.newLine();
    bw.write("Hello");
    bw.newLine();
    bw.flush();//刷新流
    
    String line;
    while((line-br.read != null){
        //多一行，不包括换行符
        System.out.print(line);
    }
          
     bw.close();
     br.close();
}
```

##### 利用字符缓冲区特有功能实现字符文件的复制

```java
public static void main(String[] args) throws IOException{
    final String SRC = "Demo01-\\src\\top\\mrxie\\iostream\\Demo01.java";
    final String DEST = "Demo01-\\test.java";
    //定义字符输出流对象
    FileReader fr = new FileReader(SRC);
    //定义字符输出流对象
    FileWriter fw = new FileWriter(DEST);
    //定义缓冲区对象
    BufferedReader br = new BufferedReader(fr);
    BufferedWriter bw = new BufferedWriter(fw);
    
    //一次读写一行进行复制
    String line;
    while((line = br.readLine()) != null){
        bw.write(line);
        bw.newLine();
        bw.flush();
    }
    
    //释放资源
    br.close();
    bw.close();
}
```

![image-20230730202635285](Java.assets/image-20230730202635285-16907199966521.png)

![image-20230730203156324](Java.assets/image-20230730203156324-16907203178622.png)

![image-20230730203507826](Java.assets/image-20230730203507826-16907205089893.png)

#### Scanner字符串采集

![image-20230730203831425](Java.assets/image-20230730203831425-16907207128744.png)

![image-20230730205551860](Java.assets/image-20230730205551860-16907217531815.png)

### 序列化

 //228集 IO总结

### 异常

#### 异常处理

默认处理方式：当程序的执行过程中产生异常时，若没有手动进行处理，则由Java虚拟机默认方式处理

手动处理方式：根据自己想法进行处理

#### 异常类

java.lang.Throwable类是Java程序所有错误的父类，主要有Error和Exception类

​	Error类：主要描述比较严重的错误，不可以通过编程来解决的重大问题

​	Exception类：主要描述比较轻量级的错误，可以通过编程来解决

#### Exception的主要分类

RuntimeException，运行时异常类，非检测性异常类，在编译阶段无法被检测出来的异常

​	ArithmeticException - 算数异常类

​	ArrayIndexOutOfBoundsException - 数组下标越界异常

​	NullPointerException - 空指针异常

​	ClassCastException - 数字格式异常

IOException和其他异常类，检测性异常类（例如，FileInputStream类new对象时产生的异常）

#### 异常的解决方法

​	通过条件判断来避免异常的出现

​	通过try、catch捕获异常并处理

```java
try {
    容易出问题的代码
}
catch(异常对象){
	异常解决办法
}
finally{
    必须执行的代码
}
```

​	有多个catch时子类写在上边，父类写在下边

​	finally中的代码无论是否产生异常都会执行，return不好使



#### 异常的抛出

当异常产生后无法直接处理或者不想直接处理时，此时可以将异常转移给当前方法的调用者

格式：

```java
返回值类型 方法名 （参数列表） throws 异常类型{方法体}
```

方法重写的时候抛出的异常不能大于被重写方法抛出的异常

#### 自定义异常类

解决Java官方库中没有描述的异常

语法：

```java
throw new Exception();
```

自定义Exception类

继承Exception类并设置构造方法，有参（调用父类中的有参构造方法）、无参



​		
