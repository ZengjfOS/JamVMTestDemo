# JamVM使用学习

[JAVAC 命令详解](http://www.cnblogs.com/JeffChen/archive/2008/01/16/1041783.html)

## 没有包的使用情况

* Java源代码：
  ```Java
  public class Hello {
      public static void main(String[] args) {
          for (int i=0; i < args.length; i++) {
              System.out.println("Hello " + args[i]);
          }
      }
  }
  ```
* Windows javac编译：
  ```Bat
  javac Hello.java
  ```
* 拷贝到ARM主板上运行输出信息：
  ```Shell
  [ZengjfOS@root ~]# jamvm Hello World Universe Everyone
  Hello World
  Hello Universe
  Hello Everyone
  ```

## 有包的使用情况

* Java源代码：
  ```Java
  package greetings;

  public class Hello {
      public static void main(String[] args) {
          for (int i=0; i < args.length; i++) {
              System.out.println("Hello " + args[i]);
          }
      }
  }
  ```
* Windows javac编译：
  ```Bat
  javac greetings\Hello.java
  ```
* 拷贝到ARM主板上运行输出信息：
  ```Shell
  [ZengjfOS@root ~]# jamvm greetings.Hello World Universe Everyone
  Hello World
  Hello Universe
  Hello Everyone
  ```
