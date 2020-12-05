##### [].forEach.call():

this是这个[]

 `.call`是一个prototype，JavaScript函数内置的。`.call`使用它的第一个参数替换掉上面说的这个`this`，也就是你要传人的数组，其它的参数就跟`forEach`方法的参数一样了。 

 `[].forEach.call()`是一种快速的方法访问`forEach`，并将空数组的`this`换成想要遍历的list。 

