#前端面试题
##介绍
-----------
根据前端的知识架构总结的前端面试的题库，难度由低到高，全面测试前端工程师业务水平。
答案在[answers](./answers.md)中，题库仍在扩充之中

##Javascript

###Simple
---------------

####1. 在js中如何声明全局变量，为什么要尽量避免申明全局变量，有什么解决办法？

####2. js中有几种数据类型？

####3. 什么叫做函数声明，什么叫做函数表达式，他们之间的区别？

####4. 什么是闭包？

####5. 在js中， === 和 == 的区别？

####6. 什么是严格模式？

####7. js如何在网页注册事件。

####8. 什么是事件冒泡机制，该如何禁止，利用该机制有什么提高性能的编程技巧？

####9.下面一段代码中，alert函数打印结果是什么
```javascript

function fun() {
    var a = b =0;
}

alert(a);
alert(b);

```

####10. 什么是异步函数？

####11. 什么是DOM？如何在DOM中实现增删改查？

####12. 什么是ajax，如何使用ajax向服务器发送get请求，并处理服务器的返回值。

###Normal
---------------

####1. 你有哪些js性能提高技巧？

####2. 什么是worker，该如何使用？

####3. 什么是jsonp，还有哪些跨域方式？

####4. 解释js中的原型链。

####5. 解释js中的作用域链。

####6. js中的this是什么，有什么作用？

####7.下面一段代码中，alert函数打印结果是什么
```javascript

if (!("a" in window)) {
    var a = 1;
}
alert(a);

```

####8.下面一段代码中，alert函数打印结果是什么
```javascript

for(var i= 0; i< 4; i++) {
    setTimeout(function() {
        alert(i);
    },0);
}

```

####9.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
function a() {
    alert(this);
}
a.call(null);
```

####10.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
function b(x, y, a) {
    arguments[2] = 10;
    alert(a);
}
b(1, 2, 3);
```

####11.下面一段代码中，alert函数打印结果是什么
```javascript

function a(x) {
    return x * 2;
}
var a;
alert(a);

```

####12.下面一段代码中，alert函数打印结果是什么,为什么
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

####13. 什么是浅拷贝，深拷贝，实现js中深拷贝

###Difficult

####1. 在js中实现继承。

####2. deferred和promise是什么,有什么区别？

####3. 什么是柯里化（currying），该如何实现一个柯里化函数？

####4. 用js实现订阅分发模式。

####5. 如果要你实现一个js前端MVC框架，你会从哪几个方面去考虑，把它设计成什么样子？

##CSS
-----------

###Simple
--------------
####1. css的优先级规则
####2. 块级元素和行内元素是什么，有什么区别，它们可以互相转换吗？
####3. css中有几种布局，及他们的作用
####4. 什么是float，有什么办法清除浮动。
####4. 什么是伪类，伪元素，它们分别都有哪些？
####5. Sass是什么，有使用过吗？
####6. css中有哪些选择符？
####7. 什么是盒子模型？
####8. 有没有使用过css动画？

##Normal
--------------
####1. 如何实现水平居中，如何实现垂直居中？
####2. 什么是响应式布局，有哪些关于响应式布局的css属性
####3. 有没有听说过圣杯布局或者双飞翼布局，它们的好处是什么，该如何实现。
####4. 什么是硬件加速，该如何触发硬件加速？
####5. 网页上能用哪些类型图片，各有什么特点，我们该如何选择，有哪些优化方法？
####6. 如果让你设计一个css框架，该从哪几个方面去考虑？
####7. 如何使元素在网页上消失，你有几种方法，各有什么区别？
####8. 负值的margin有什么作用。
####9.几种方法设置元素透明度，它们之间有什么区别？


##HTML
---------------

###Simple
-------------
####1. doctype 元素是什么， 有什么作用？
####2. 解释一下什么是HTML语义化，语义化有什么好处，我们做什么可以使网站语义化更好？
####3. HTML5提供了那些新的特性？
####4. meta标签什么的，你常用它来做什么？
####5. img标签中的title和alt分别是做什么的？

###Normal
--------------
####1. 什么是canvas，svg，它们有什么区别，使用过它们么？
####2. 什么是iframe，我们能用iframe做什么，使用iframe是好还是不好，为什么？
####3. 什么是HTML模板？有没有使用过HTML模板（框架不限）？
####4. 什么是SEO，如何给网站提供更好的SEO。
####5. script标签的defer和async属性有什么作用？

###Difficult
------------------
####1. 什么是BFC，BFC有什么作用，该如何触发BFC？
####2. 什么是 shadow dom？
####3. 你能用几种方法画出一个平行四边形？

##Security
------------------
####1. 什么是XSS，该如何防范？
####2. 什么是CSRF，该如何防范？

##ES6
------------------
####1. 使用let申明变量，和使用var申明变量的区别有哪些？
####2. const变量个let变量的异同？
####3. es5中有几种声明变量的方式，es6中有几种声明变量的方式？
####4. 互换变量x和y的值.
####5. 请问以下两种写法的区别，对应不同情况下的x, y值？
```javascript
// 写法一
function m1({x = 0, y = 0} = {}) {
  return [x, y];
}

// 写法二
function m2({x, y} = { x: 0, y: 0 }) {
  return [x, y];
}
###
```

####6. 以下代码的输出值是多少？

```javascript
function foo() {
  setTimeout(() => {
    console.log('id:', this.id);
  }, 100);
}

var id = 21;

foo.call({ id: 42 });
// id: 42
```

####7. Symbol是什么，解决了什么问题？

####8. ES6中Set是怎样的数据结构？和weakSet的区别是什么？

###9. ES6中Generator函数和yield语句是什么？有什么作用？

###10. ES6中yield语句和yield*的区别是什么？

###11. 使用ES6后，使用了哪些编程风格？

##Others
------------------
####1. 对前端性能有研究么？有多少种方法优化前端性能？
####2. 浏览器内核是做什么的？
####3. 解释浏览器是如何解析并渲染网页的？
####4. 解释从用户输入网址，到网页打开，都经历了什么，越详细越好。
####5. 什么是websocket，使用过websocket吗？
####6. 你是如何调试前端代码的？
####7. 使用过前端自动化工具么？你都用它做了什么？
####8. 什么是AMD？它有哪些好处？你使用过哪些库去实现AMD。

##版本控制
------------------
####1. 什么是集中式版本控制系统，什么是分布式版本控制系统？
####2. 解释git中暂存区的概念？
####3. Git中如何回退到一个指定版本，需要执行哪些操作？
####4. 请依次执行如下操作，创建一个新分支，并将工作区修改提交到当前新分支，将新分支提交到远程代码库，删除当前新分支。
####5. 如何解决分支冲突？
####6. 如何为命令配置别名？
