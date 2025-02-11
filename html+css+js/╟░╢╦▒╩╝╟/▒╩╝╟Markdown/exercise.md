```javascript
1.javascirpt中的数字在计算机内存储为() //8Byte
知识点：Javascript中,由于其变量内容不同,变量被分为基本数据类型变量和引用数据类型变量,
    基本类型变量用八字节内存,存储基本数据类型(数值、布尔值、null和未定义)的值,
    引用类型变量则只保存对对象、数组和函数等引用类型的值的引用(即内存地址).
```

```javascript
2.以下表达式的运行结果是()
var arr = Array(3);
arr[0] = 2;
console.log(arr);//[2,empty*2]
var x = arr.map(function(elem){return '1';});
console.log(x);//["1",empty*2]
3.下面有关JavaScript中 call和apply的描述,错误的是()
A.call与aplly都属于Function.prototype的一个方法,所以每个function实例都有call、apply属性 
B.两者传递的参数不同,call函数第一个参数都是要传入给当前对象的对象,apply不是 
C.apply传入的是一个参数数组,也就是将多个参数组合成为一个数组传入 
D.call传入的则是直接的参数列表.call 方法可将一个函数的对象上下文从初始的上下文改变为由 thisObj 指定的新对象 
【正确答案】B
【答案解析】call()方法和apply()方法的作用相同,他们的区别在于接收参数的方式不同.对于call(),第一个参数是this值没有变化,变化的是其余参数都直接传递给函数.(在使用call()方法时,传递给函数的参数必须逐个列举出来.使用apply()时,传递给函数的是参数数组）如下代码做出解释：
function add(c, d){ 
return this.a + this.b + c + d; 
} 
var o = {a:1, b:3}; 
add.call(o, 5, 7); // 1 + 3 + 5 + 7 = 16 
add.apply(o, [10, 20]); // 1 + 3 + 10 + 20 = 34 
所以选B

3.(单选题)length的值是();
var length = 10;
function fn(){
    alert(this.length);
}
var obj = {
    length: 5,
    method: function(fn) {
        fn();
        arguments[0]();//匿名自调函数
    }
}
obj.method(fn);
A.10 
B.5 
C.2 
D.1 
【正确答案】D
【答案解析】本题的考点为this,arguments,我们知道取对象属性于除了点操作符还可以用中括号,这里fn的scope是arguments,即fn内的this===arguments,调用时仅传了一个参数fn,因此length为1.所以选D
3.关于this关键字说法错误的是()
A.this是js的一个关键字,随着函数使用场合不同,this的值会发生变化 
B.this指的是调用函数的那个对象 
C.this一般情况下:是全局对象Global 
D.在javascript中一共有四种调用模式:方法调用模式,函数调用模式,构造器调用模式,数组调用模式 
【正确答案】D
【答案解析】在javascript中一共有四种调用模式:方法调用模式,函数调用模式,构造器调用模式,apply调用模式.所以选D
4.以下表达式的运行结果是()
[]==[]
A.true 
B.false 
C.报错 
D.其他 
【正确答案】B
【答案解析】数组,在 Javascript 中是对象,对象使用 == 比较都是比较的引用.简单的说,就是,如果是同一个对象,就相等,如果不是同一个对象,就不等.每次使用 [] 都是新建一个数组对象,所以 [] == [] 这个语句里建了两个数据对象,它们不等.所以选B
5.(单选题)W3C DOM 标准被分为()个不同的部分
A.3 
B.2 
C.4 
D.5 
【正确答案】A
【答案解析】W3C DOM 标准被分为 3 个不同的部分：
核心 DOM - 针对任何结构化文档的标准模型
XML DOM - 针对 XML 文档的标准模型
HTML DOM - 针对 HTML 文档的标准模型.所以选A
6.(多选题)关于DOM节点树描述有误的是()
A.每个 HTML 元素是元素节点 
B.整个文档是一个根节点 
C.注释是文本节点 
D.HTML 元素内的文本是节点 
【正确答案】B,C,D
【答案解析】根据 W3C 的 HTML DOM 标准,HTML 文档中的所有内容都是节点:
整个文档是一个文档节点
每个 HTML 元素是元素节点
HTML 元素内的文本是文本节点
每个 HTML 属性是属性节点
注释是注释节点.所以选BCD
7.(单选题)JavaScript中能够查询和设置文档属性的方法有()
A.5 
B.6 
C.8 
D.4 
【正确答案】A
【答案解析】一共有五种,分别是:
createAttribute() 创建属性节点
getAttribute(name) 返回属性值, 该值是字符串型, 而不是数值、布尔值或对象
setAttribute(name,value) 设置属性值
hasAttribute(name) 检测是否还有属性, 返回布尔值
removeAttribute(name) 完全删除属性
所以选A
```

```
1.(单选题)在python中，用正则表达式截取字符串中第一个出现的英文左括号之前的字符串。比如：北京市'海淀区''朝阳区'西城区，截取结果为：北京市。正则表达式为（）
A. r".*?\(?='\)"  
B.r".*?\(?='\)" 
C.r".*?(?=')" 
D.r".*?(?=\(\)" 
【正确答案】C
【答案解析】选C
前面的.*?是非贪婪匹配的意思， 表示找到最小的就可以了
(?=Expression) 顺序环视, (?=')就是匹配单引号
其它选项错误因为raw字符串无需转义；
2.(单选题)正则表达式(01|10|1001|0110)*与下列哪个表达式一样？
A.(0|1)* 
B.(01|01)* 
C.(01|10)* 
D.(11|01)* 
【正确答案】C
【答案解析】1001可以由10和01构成，0110可以由01和10构成，选择C，意味由01或10构成的串。
A选项可以匹配01|10|1001|0110，但是也可以匹配0或者1，不符合；
B选项无法匹配0110
D选项无法匹配0110和1001
```

