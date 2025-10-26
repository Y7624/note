**java提供了String类来创建和操作字符串**

String 创建的字符串存储在公共池中，而new创建的字符串对象1在对象上。

String 类是不可变的，一旦创建了String对象，那它的值就无法改变了

如果字符串需要修改，那么使用StringBuffer&StringBuilder类

String类使用静态方法format（）返回一个String对象而不是PrintStream。

String 类的静态方法format（）用来创建可复用的格式化字符串，而不仅仅是用于打印输出







## 正则表达式

Pattern 对象是一个正则表达式的编译表示，pattern没有公共构造方法。要创建一个pattern对象，你必须首先强调用其公共静态编译方法，它返回一个pattern对象，该方法接受一个正则表达式作为它的第一个参数





