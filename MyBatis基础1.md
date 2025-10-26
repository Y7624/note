## MyBatis

MyBatis是一款优秀的持久层框架，用于简化JDBC的开发



****

## JDBC

JDBC:是使用java语言操作关系型数据库的一套API

数据库连接池：一个容器，负责分配，管理数据库连接

它允许应用程序重复使用一个现有的数据库连接，而不是重新建立一个

释放空闲时间超过最大空闲时间连接，来避免因为没有释放连接而引起的数据库连接遗漏



![image-20250711115546627](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250711115546627.png)

DataSourse

@Data：提供更综合的生成代码功能

@NoArgsConstructor：为实体类生成无参的构造方法

@AllArgsConstructor：为实体类生成除了static修饰符之外带有各参数的构造器方法

注意：lombok会在编译时，自动生成对应的java代码，我们使用lombok时，需要安装一个lombok的插件



******

### Mybatis增删改查

![image-20250711213401784](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250711213401784.png)

如果mapper接口方法形参只有一个普通类型的参数，#（……）里面的属性名可以随便写，如：#（id)、#(value)

Sql注入是通过操作输入的数据来修改事先定义好的SQL语句，以达到执行代码对服务器进行攻击的方法

### 参数占位符

#### #{...}

执行SQL时，会将#{...}替换为？，生成预编译SQL，会自动设置参数值

使用时机：参数传递，都使用#{...}

#### ${...}

拼接SQL,直接将参数拼在sql语句中，存在sql注入问题

使用十几：如果对表名、列表进行动态设置时使用

#### 数据封装

实体类属性名和数据库表查询返回的字段名一致，mybatis会自动封装

如果实体类属性名和数据库表查询返回的字段名不一致，不能自动封装

![image-20250712132105963](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250712132105963.png)

起别名：在SQL语句中，对不一样的列名起别名，别名和实体类属性名一样

手动结果映射：通过@Results及@Result进行手动结果映射

开启驼峰命名：如果字段名与属性名符合驼峰命名规则，mybatis会自动通过驼峰命名规则映射

查询（条件查询）

![image-20250712134304188](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250712134304188.png)

''中不能包含#{}，${}安全性不高，可通过concat解决这个问题

在springboot1.x版本中加上@params注解来指定我们要获取的哪个参数

