基本数据类型
    string  number  boolean
复杂数据类型（引用类型）
    Array  Date  Object  RegExp  String  Number  Boolean

    Object function

如何获取一个数据的数据类型
    使用关键字 typeof

typeof返回值为string类型

String  Number  Date  首字母大写的都是构造函数

两个空的类型
    null
    undefined

/全等和等于/
=== 全等
    类型和值都要进行比较
== 等于
    只比较值
    <script>
    var str1 = "abc";
    var str2 = "abc";
    console.log(str1 == str2);

    var a = 1;
    var b = "1";
    console.log(a === b);
</script>

in关键字
    1. 最常用的是在for in 循环中 遍历对象的键
    2. 判断属性是否存在于对象中
       语法   属性名 in 对象

    对象的键为字符串类型

     var propName = "name";
     var isExsit = propName in obj;
     console.log(isExsit);

值类型和引用类型

值类型：  string  number  boolean  undefined
     存储的就是数据本身的变量就是值类型的数据
     存储的是数据在内存中的地址，数据在内存中单独存储 就是引用类型的数据

    引用类型：object
    存储的是数据在内存中的地址，数据在内存中单独存储 就是引用类型的数据

     引用类型赋值
     引用类型赋值的时候，是将变量中存储的地址复制一份单独存储，但是两个变量共享同一个对象
     修改其中一个对象，两外一个引用来访问的时候，也会访问到修改后的对象
     值类型的赋值
     直接将存储的数据复制一份进行赋值，两份数据在内存中是完全独立的
<script>
    var str = "凡是不能击败我的";
    var str1 = str;

    str = "只会让我更heitai";

    console.log(str1);

    var num1 = 110;
    var num2 = num1;
    num1 = 119;
    console.log(num2);
</script>

引用类型和值类型在函数中的使用

实参：就是函数调用的时候，实际传入的参数
形参：函数声明的时候，用来站位的变量名，没有具体的数值
在函数调用时，会默认的将实参赋值给形参


值类型做函数的参数
函数内部的变量，也就是形参和实参只是简单的赋值操作，两个数据独立存储于内存中的
在函数内部对形参进行修改，不会影响外面的变量

引用类型做函数的参数
实参存储的地址赋值给了形参，在函数内部，形参同样也指向该对象，

在函数内部对该对象进行修改，会影响到外面的变量

如果在函数内部重新创建对象，为该形参赋值，那么两个对象将不再有关系

修改其中一个，另外一个不受影响


对象的动态特性

1.给对象动态添加属性

当一个对象需要某个属性的时候，可以用两种方式为其添加属性

直接使用对象名.属性名 = 值这种形式，为对象添加对应的属性。
使用关联数组语法对象名["属性名"] = 值这种形式，为对象添加对应的属性

var o = {}; //这是一个没有然后属性的属性值

o.name = "张三"; //这个拥有了name属性

o["age"]=18; //使用对象["属性名"]=值


2.对象属性的访问形式

点语法：对象名.属性名
关联数组：对象名[属性名]

var o = {
    name:"张三",
    sayHello:function(){
        console.log("你好，我叫"+ this.name);
    }
};

//点语法
console.log(o.name);

//关联数组语法
console.log(o["name"]);

//可以对这个对象的属性进行遍历，如果是值就打印，如果是方法就调用
for(var k in o){
    if ( typeof o[ k ] == 'function' ) {
        o[ k ]();
    } else {
        console.log( 'log: ' + o[ k ] );
    }
}


/常用DOM操作/

获取元素操作

getElementById getElementsByTagName getElementsByClassName

元素节点操作

appendChild insertBefore removeChild replaceChild cloneNode

createElement createTextNode（创建文本节点）

属性节点操作

getAttribute setAttribute removeAttribute

常用DOM属性

className innerHTML innerText/textContent value

children

 增
document.createElement
appendChild

删
removeChild

改
style
id
className
innerHTML
innerText

查
getElementById
getElementsByTagName
getELementsByClassName



/异常处理/

常见的异常分类

运行环境的多样性导致的异常（浏览器）
语法错误，代码错误
异常最大的特征，就是一旦代码出现异常，后面的代码就不会再执行

异常捕获

捕获异常，使用try-catch语句

try{
    //这里写可能出现异常的代码
}catch(e){
    //这里的e就是捕获的异常对象
    //可以在这里写，出现异常后的处理代码
}

异常捕获语句执行的过程为：

代码正常运行, 如果在try中出现了错误, try 里面出现错误的语句后面的代码都不再执行, 直接跳转到 catch 中

catch中处理错误信息

然后继续执行后面的代码

如果 try 中没有出现错误, 那么不走 catch 直接执行后面的代码

通过try-catch语句进行异常捕获之后，代码将会继续执行，而不会中断。

抛出异常


抛出异常使用throw关键字，语法如下：

throw 异常对象;
异常对象一般是用new Error("异常消息"), 也可以使用任意对象

function test(para){
    if(para == undefined){
        throw new Error("请传递参数");
        throw {"id":1, msg:"参数未传递"};
    }
}

try{
    test();
}catch(e){
    console.log(e);
}
异常的传递机制

function f1 () {
    f2(); // f1 称为调用者, 或主调函数, f2 称为被调用者, 或被调函数
}

function f2 () {
    f3();
}

function f3() {
    throw new Error( 'error' );
}
f1();
当在被调函数内发生异常的时候，异常会一级一级往上抛出。

异常捕获语句的完整模式

异常捕获语句的完整模式为try-catch-finally

try {
    //可能出现错误的代码
} catch ( e ) {
    //如果出现错误就执行
} finally {
    //结束 try 这个代码块之前执行, 即最后执行
}

