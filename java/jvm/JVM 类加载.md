JVM 底层存储
HSDB

MetaspaceObj Klass InstanceKlass ->  
（非数组） 存储java类

InstanceMirrorKlass -> Class 对象 （堆区）

    InstanceRefKlass 引用

ArrayKlass
存储数组类

class

klass java 类在JVM中的存在形式

Java 中的数组
1. 静态数据类型
2. 动态数据类型



类的加载过程

1. 根据class 全限定名（包名+类名）读取class文件

准备

解析


初始化


常量池
1. class 文件常量池
2. 运行时常量池


JVM 加载类是懒加载模式


ubuntu
jdk
