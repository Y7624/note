## 阿里云oss

阿里云对象存储oss，是一款海量、安全、低成本、高可靠的云存储服务。

SDK：软件开发工具包,包括辅助软件开发的依赖、代码示例等，都可以叫做SDK

![image-20250715145921753](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250715145921753.png)

Bucket：存储空间是用户用于存储对象的容器，所有的对象都必须隶属于某个存储空间

![image-20250715150339991](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250715150339991.png)



***

## 配置文件

@value注解通常用于外部配置的属性注入

@value（”$(key值)")

![image-20250715211904080](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250715211904080.png)



yml基本语法：

大小写敏感

数值前边必须有空格，作为分隔符

使用缩进表示层级关系，不允许使用Tab键，只能用空格（idea中会自动将Tab转换为空格

缩进的空格数目不重要，只要相同层级的元素左侧对齐即可

#表示注释，从这个字符一直到行尾，都会被解析器忽略

@ConfigurationProperties

### @RestControllerAdvice 全局异常处理器

**@ExceptionHandler**

@RestControllerAdvice=@ControllerAdvice+@ResponseBody

