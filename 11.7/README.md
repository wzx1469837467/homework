/*数组*/

定义 
var ary=new Array();  //创建对象得方式创建数组
var ary1=[];      //直接创建一个数组

赋值
数组中通过下标的方式进行赋值。下标从0开始。

var ary1=[]; 
ary1[0]=123; 数组赋值
ary1[1]=345;

数组的初始化和遍历 
var ary1=[12,23,45,"34"]; 数组的初始化
//alert(ary1);
//数组的遍历
for(var i=0; i<5; i++){
    alert(ary1[i]);
}

数组数据的个数 length属性
 通过数组名.length获取数组长度 （元素个数）

var ary=[1,"2k","e3",43,23,23,54,65,"y5","y6",7];
	 for(var i=0;i<ary.length; i++){
	 	alert(ary[i]);
	}

数组合并
使用concat方法合并数组。
    var ary1=[2,23,32,21,345,46];
	var ary2=[2,3,4,8,12,"来两串"];
	 // // 数组的合并
	var ary3=ary1.concat(ary2);
	alert(ary3);


Join 方法  返回一个字符串

Join方法返回一个字符串数组。

 var ary1=[2,23,32,21,345,46,"中国人"];
	 var ary2=ary1.join("&");
	 alert(ary2);
	 alert(typeof(ary2));

	 /*函数*/
函数（方法）定义
通过 function  关键字
和自定义方法名 既可定义一个函数。

function test(){
	alert("你好")
}

test();   //方法的调用
