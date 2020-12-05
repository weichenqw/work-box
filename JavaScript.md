##### bind方法，apply方法，call方法实现：

作用：

1.改变this指向

2.传入参数

3.call apply返回函数结果，bind返回新函数



typeof返回哪些数据类型：

typeof null ： "object"；  null期望获取数组

typeof [1]： "object"；

typeof { }： "object"；  typeof 无法区分null 数组和对象 





##### js检测对象中是否存在某个属性：

 in关键字 判断对象的自有属性和继承来的属性是否存在。

 `hasOwnProperty()`函数用于指示一个对象自身(不包括原型链)是否具有指定名称的属性。如果有，返回`true`，否则返回`false`。 

 该方法属于`Object`对象，由于所有的对象都"继承"了Object的对象实例，因此几乎所有的实例对象都可以使用该方法。  



##### 原型本质：

当实例调用实例方法或实例对象，会先在自身寻找，没有就在原型中寻找

