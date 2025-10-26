## XML映射文件

xml映射文件的名称与Mapper接口名称一致，并且将xml映射文件和Mapper接口放置在相同包下（同包同名）

xml映射文件的namespace属性位Mapper接口全限定名一致

xml映射文件中sql语句的id与Mapper接口中的方法名一致，并保持返回类型一致



![image-20250712135635242](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250712135635242.png)

使用MyBatis的注解，主要是来完成一些简单的增删查改功能。如果需要实现复杂的SQL功能，建议使用XML来配置映射语句

## 开发规范-Restful

REST，表述性状态转换，它是一种软件架构风格。

![image-20250713203353830](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250713203353830.png)

REST是风格，是约定方式，约定不是规定，可以打破

描述模块的功能通常使用复数，也就是加s的格式来描述，表示此类资源，而非单个资源