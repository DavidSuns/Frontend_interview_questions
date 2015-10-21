#前端面试题
----
##Javascript
###Simple
####1.下面一段代码中，alert函数打印结果是什么
```javascript

if (!("a" in window)) {
    var a = 1;
}
alert(a);

```

####2.下面一段代码中，alert函数打印结果是什么
```javascript

function fun() {
    var a = b =0;
}

alert(a);
alert(b);

```
####3.下面一段代码中，alert函数打印结果是什么
```javascript

function a(x) {
    return x * 2;
}
var a;
alert(a);

```

####4.下面一段代码中，alert函数打印结果是什么
```javascript

for(var i= 0; i< 4; i++) {
    setTimeout(function() {
        alert(i);
    },0);
}

```

####5.下面一段代码中，alert函数打印结果是什么
```javascript

for(var i= 0; i< 4; i++) {
    setTimeout(function() {
        alert(i);
    },0);
}

```

####6.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
var obj1 = {a:1,b:2};

function fun1(obj) {
    obj = {c:2, d:3};
};

fun1(obj1);
alert(obj1);

var obj2 = 5;

function fun2(obj) {
    obj = 6;
};

fun2(obj2);
alert(obj2);

```

####7.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
function a() {
    alert(this);
}
a.call(null);
```

####7.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
function b(x, y, a) {
    arguments[2] = 10;
    alert(a);
}
b(1, 2, 3);
```

####7. 在js中如何声明全局变量，为什么要尽量避免申明全局变量，有什么解决办法？

####8. js中有几种数据类型？

####9. 什么叫做函数声明，什么叫做函数表达式，他们之间的区别？

####10. 什么是闭包？

####11. 在js中， === 和 == 的区别？

####12. 什么是严格模式？

####13. 什么是浅拷贝，深拷贝，实现js中深拷贝

####14. 什么是DOM？

####15. 什么是ajax，如何使用ajax向服务器发送get请求，并处理服务器的返回值。

####16. js中的this是什么，有什么作用？

####17. 解释js中的原型链。

####18. 解释js中的作用域链。

####19. js如何在网页注册事件。

####20. 什么是事件冒泡机制，该如何禁止，利用该机制有什么提高性能的编程技巧？

####21. 在js中实现继承。

####22. 你有哪些js性能提高技巧？

####23. 什么是worker，该如何使用？

####24. 