**基于idea开发springboot程序需要确保联网且能够加载到程序框架结构**

SpringBoot是由于pivotal团队提供的全新框架，其设计目的是用来**简化**spring应用的**初始搭建**以及**开发过程**

**继承parent模块可以避免多个依赖使用相同技术时出现依赖版本冲突**

**继承parent的形式也可以采用引入依赖的形式实现效果**

**starter:定义了当前项目使用的所有依赖坐标，以达到减少依赖配置的目的**

**SpringBoot的引导类是Boot工程的执行入口，运行main方法就可以启动项目**

**SpringBoot工程运行后初始化Spring容器，扫描引导类所在包加载been**

内嵌tomcat服务器，辅助功能，

**jetty比tomCat更轻量级，可扩展性更强(相当于Tomcat)**

#### 内置服务器：

**tomCat（默认）  apache出品，粉丝多，应用面广，负载了若干较重的组件**

jetty：