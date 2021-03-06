#前端面试题
##介绍
-----------
根据前端的知识架构总结的前端面试的题库，难度由低到高，全面测试前端工程师业务水平。
答案在[answers](./answers.md)中，题库仍在扩充之中。
由于水平有限，问题和答案难免有纰漏，还望不吝指正。

##Javascript

###Simple
---------------

####1. 在js中如何声明全局变量，为什么要尽量避免申明全局变量，有什么解决办法？

> _Answer_：1.全局作用域声明的变量；2.函数作用域不带var声明也可全局访问，但不是全局变量，而是挂在window下属性。 3.直接window下挂载属性；
>为什么避免：全局变量冲突（最关键），内存占用。
>如何避免：闭包，命名空间。


####2. js中有几种数据类型？

> _Answer_： object, array, number, string, undefined, null。

####3. 什么叫做函数声明，什么叫做函数表达式，他们之间的区别？

> _Answer_：如果一个函数是表达式的一部分的话，则为函数表达式，反之则为函数声明。
>区别：1.函数声明需有函数标识符，表达式可以省略；
>      2.函数声明会在任何表达式被解析和求值之前先被解析和求值, 函数表达式是到执行到时才被解析。

####4. 什么是闭包？

>_Answer_:闭包是一系列代码块（在ECMAScript中是函数），并且静态保存所有父级的作用域。通过这些保存的作用域来搜寻到函数中的自由变量。

####5. 在js中， === 和 == 的区别？

>_Answer_: ===是严格等于，不仅值要相等，类型也需要相等。

####6. 什么是严格模式？

>_Answer_: 要答三点：1.声明位置的影响；2.声明后的效果；（至少两种，越多越好）3.为什么要设计严格模式。

####7. js如何在网页注册事件。

>_Answer_: addEventListener; ie:attachEvent;jquery:有对应事件名的函数，bind,on,one,live,delegate。

####8. 一次事件响应的完整过程分为几步？什么是事件冒泡机制，该如何禁止，利用该机制有什么提高性能的编程技巧？

>_Answer_:三步：捕获，响应，冒泡。
>event.stopPropagation(),
>常用技巧：底层事件，顶层捕捉。

####9.下面一段代码中，alert函数打印结果是什么
```javascript

function fun() {
    var a = b =0;
}

alert(a);
alert(b);

```

>_Answer_: a:undefined, b:0.

####10. 什么是异步函数？

>_Answer_: 需回答什么是异步函数，并在js中实现异步的方式：回调，事件监听，promise等。

####11. 什么是DOM？如何在DOM中实现增删改查？

>_Answer_:文档对象模型，js操作HTMl和xml的接口。
>增：createElement，createTextNode，appendChild等
>删：removeChild
>改：element.value, element.className, element.name ...
>查：getElementById, getElementByName, getElementByTagName,parentNode,children ....

####12. 什么是ajax，如何使用ajax向服务器发送get请求，并处理服务器的返回值。

>_Answer_:略。

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

>_Answer_:打印undefined。 变量声明先于内容执行。

####8.下面一段代码中，alert函数打印结果是什么
```javascript

for(var i= 0; i< 4; i++) {
    setTimeout(function() {
        alert(i);
    },0);
}

```

>_Answer_: 打印4遍4。setTimeout要在线程空闲的时候才会执行

####9.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
function a() {
    alert(this);
}
a.call(null);
```

>_Answer_: 打印window对象。

####10.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
function b(x, y, a) {
    arguments[2] = 10;
    alert(a);
}
b(1, 2, 3);
```

>_Answer_: 打印3。arugments和实参不在一个内存地址

####11.下面一段代码中，alert函数打印结果是什么
```javascript

function a(x) {
    return x * 2;
}
var a;
alert(a);

```

>_Answer_: 打印 function a。 函数声明会覆盖变量声明

####12.下面一段代码中，alert函数打印结果是什么,为什么
```javascript
var obj1 = {a:1,b:2};

function fun1(obj) {
    obj = {c:2, d:3};
};

fun1(obj1);
alert(obj1);

var obj2 = {a:1,b:2};

function fun2(obj) {
    obj.a = 3;
    obj.b = 4;
};

fun2(obj2);
alert(obj2);

```

>_Answer_: 第一遍打印：{c:2,d:3}，第二遍打印6。
>考察js的传参策略，传的是参数引用的拷贝。


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

>_Answer_: 跨站脚本攻击，攻击方式主要有两种：
> 1. 基于dom攻击，中招的是少数人，漏洞在于页面参数直接渲染，攻击者可以可以利用参数注入恶意代码
> 2. 将攻击代码发布到网上，存储于服务器的数据库中，危害范围广，主要漏洞在于没有对用户的输入做过滤检查。
> 防范对策：对用户输入做转义;在将不可信数据插入到HTML标签之间时，对这些数据进行HTML Entity编码;

####2. 什么是CSRF，该如何防范？

>_Answer_: 跨站请求伪造，只有在你同时打开已登录的网站和危险网站的时候才有可能发生，攻击者在危险网站中诱使
> 用户点击攻击性地登录网站链接，利用cookie伪造了你的身份，便可以修改你的用户数据。
> 防范对策：使用post上传数据；cookie hash；验证码；检查refered，是不明来源的请求拒绝执行。

##ES6

------------------
####1. 使用let声明变量，和使用var声明变量的区别有哪些？

>_Answer_:
> 1. 增加了块作用域概念，只在申明它的代码块中有效。
> 2. 不存在变量提升。
> 3. 不允许重复声明。

####2. const变量个let变量的异同？

>_Answer_: 同：1.只在代码块中有效。2.不能重复声明。 3.不存在变量提升。
> 异：1.const值声明后不能改变。

####3. es5中有几种声明变量的方式，es6中有几种声明变量的方式？

>_Answer_: ES5: var, function;  ES6: var, function, let, const, class, import.

####4. 互换变量x和y的值

>_Answer_: [x, y] = [y, x];

####5. ####5. 请问以下两种写法的区别，对应不同情况下的x, y值？
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

>_Answer_:

```javascript
// 函数没有参数的情况
m1() // [0, 0]
m2() // [0, 0]

// x和y都有值的情况
m1({x: 3, y: 8}) // [3, 8]
m2({x: 3, y: 8}) // [3, 8]

// x有值，y无值的情况
m1({x: 3}) // [3, 0]
m2({x: 3}) // [3, undefined]

// x和y都无值的情况
m1({}) // [0, 0];
m2({}) // [undefined, undefined]

m1({z: 3}) // [0, 0]
m2({z: 3}) // [undefined, undefined]
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
>_Answer_: 42， 因为在箭头函数中，函数体内的this对象，就是定义时所在的对象，而不是使用时所在的对象。

####7. Symbol是什么，解决了什么问题？

>_Answer_: 新加入的类型，表示独一无二的值，解决命名冲突。

####8. ES6中Set是怎样的数据结构？和weakSet的区别是什么？

>_Answer_: Set只允许添加不重复的值。weakSet的区别在于它只能储存对象，且都是弱引用。所以垃圾回收机制在回收内存空间时
>不考虑是否在weakSet中。所以weakSet不可遍历。

###9. ES6中Generator函数和yield语句是什么？有什么作用？

>_Answer_: 可以将generator函数看作一个状态机，返回一个遍历对象，通过next函数依次遍历状态。
> yield语句用来定义状态，是可以暂停执行状态的函数，只有调用next才会遍历下一个状态。
> 在将异步操作转为同步操作时比较有用。

###10. ES6中yield语句和yield*的区别是什么？

>_Answer_: yield* 后面可以解析generator函数，而yield不行。

###11. 使用ES6后，使用了哪些编程风格？

>_Answer_: 1.let和const替代var；2.字符串拼接；3.解构赋值；4.箭头函数，函数默认值；5.使用class语法糖去定义类；
>6.es6模块应用； 7. promise，async，await 的应用；等

##React

##1. React组件的生命周期是怎样的, 这里面有哪些常用的方法？
>_Answer_: 组件实例化： getDefaultProps -> getInitialState -> componentWillMount -> render -> componentDidMount -> componentWillUnmount
> 属性改变： componentWillReceiveProps -> shouldComponentUpdate -> componentWillUpdate -> componentDidUpdate.
> 常用方法有： getDefaultProps,用于初始化props; getInitialState,用于初始化state; render,用于渲染dom; componentDidMount, 用于在初渲染到dom的时候，提供一些挂载方法，如ajax等; shouldComponentUpdate: 用于确定组件是否应该被刷新。

##2. React中如何得到dom对象？
>_Answer_: 1.reactDOM提供了findDOMNode; 2. refs.

##3. 你是如何优化react渲染性能的？它的原理是什么？
>_Answer_: pureRenderMixin and immutable.js;
> 原理： componentShouldUpdate,和浅相等。


##Others

####1. 对前端性能有研究么？有多少种方法优化前端性能？
####2. 浏览器内核是做什么的？
####3. 解释浏览器是如何解析并渲染网页的？
####4. 解释从用户输入网址，到网页打开，都经历了什么，越详细越好。
####5. 什么是websocket，使用过websocket吗？
####6. 你是如何调试前端代码的？
####7. 使用过前端自动化工具么？你都用它做了什么？
####8. 什么是AMD？它有哪些好处？你使用过哪些库去实现AMD。
