## 动态SQL

随着用户的输入或外部条件变化而变化的SQL语句，称为动态SQL

<if>如果条件成立，则拼接SQL语句

![image-20250712174444048](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250712174444048.png)

<where>where元素只会在子元素有内容的情况下才会插入where子句，而且会自动去除子句开头的and或or

<set>替代set关键字,并会删掉额外的逗号（用在update语句中）

<foreach>

![image-20250712180532606](C:\Users\45379\AppData\Roaming\Typora\typora-user-images\image-20250712180532606.png)

colleation:集合名称

item:集合遍历出来的元素/顶

separator:每一次遍历使用的分隔符

open:遍历开始前拼接的片段

close:遍历结束后拼接的片段

<sql>定义可重用的SQL片段

<include>通过属性refid,指定包含的sql片段