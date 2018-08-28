#  类型信息  Type Information

# key words

Runtime type information (RTTI)  运行时类型信息  


#  类讲解

[Staff.java](../src/main/java/typeinfo/Staff.java)   

构造 `Staff` (工作人员 ) 对象时候传入了一些 `title` (职位名称) , 根据 `title` 创建相应的 `Position` (职位) ,   `Position.person` 属性 赋值了 `Person` 默认构造函数的实例。
`Staff.fillPosition(String title, Person hire)` 方法再给相应职务填充真实属性的人。

先创建组织架构职务,等有人(钱)了,再把真实的张三李四放进去。

在 `TIJ4` 中 [TIJ4-code/Person.java](https://github.com/BruceEckel/TIJ4-code/blob/master/examples/typeinfo/Person.java)使用了静态属性  `NULL` 表示一个空的人实例 ( Null Objects ) , 而新版  [Person.java](../src/main/java/typeinfo/Person.java) 使用了实例属性 `empty` 表示 `Person` 实例是否是一个空人,相对 `TIJ4` 的 静态变量空对象,新版 的空对象 都是独立的实例,会多暂用些内存控件。使用了 Java 8 的 `Optional` 新特性 来简化 null 的判断。
