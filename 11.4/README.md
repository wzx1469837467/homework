两个数字类型的变量相加，得到的是一个数字类型

一个数字类型和一个字符串相加，得到的是一个字符串

一个数字类型和 一个数字字符串相减，得到的是一个数字类型。

Math  用于执行数学任务

Math    对象属性
属性	描述
E	返回算术常量 e，即自然对数的底数（约等于2.718）。
LN2	返回 2 的自然对数（约等于0.693）。
LN10	返回 10 的自然对数（约等于2.302）。
LOG2E	返回以 2 为底的 e 的对数（约等于 1.414）。
LOG10E	返回以 10 为底的 e 的对数（约等于0.434）。
PI	返回圆周率（约等于3.14159）。
SQRT1_2	返回返回 2 的平方根的倒数（约等于 0.707）。
SQRT2	返回 2 的平方根（约等于 1.414）

Math  对象方法
方法	 描述
abs(x)	 返回数的绝对值。
acos(x)	 返回数的反余弦值。
asin(x)	 返回数的反正弦值。
atan(x)	 以介于 -PI/2 与 PI/2 弧度之间的数值来返回 x 的反正切值。
atan2(y,x) 	返回从 x 轴到点 (x,y) 的角度（介于 -PI/2 与 PI/2 弧度之间）。
ceil(x)	 对数进行上舍入。
cos(x)	 返回数的余弦。
exp(x)	 返回 e 的指数。
floor(x)	对数进行下舍入。
log(x)	 返回数的自然对数（底为e）。
max(x,y)	返回 x 和 y 中的最高值。
min(x,y)	返回 x 和 y 中的最低值。
pow(x,y)	返回 x 的 y 次幂。
random()	返回 0 ~ 1 之间的随机数。
round(x)	把数四舍五入为最接近的整数。
sin(x)	 返回数的正弦。
sqrt(x)	 返回数的平方根。
tan(x)	 返回角的正切。
toSource()	返回该对象的源代码。
valueOf()	返回 Math 对象的原始值。

数据类型转换
	
	var numer= prompt("请输入卡号");
	alert(typeof(numer));


1：将数字类型转换为字符串类型
       隐式类型转换               
      
 强制类型转换（String(),  变量.tostring()）


2：将字符串转换为数字类型
        隐式类型转换               
       
 强制类型转换(Number(),parseInt(),      parseFloat())


3：将其他数据类型转换为布尔类型
       
        
强制类型转换 :Boolean()        数字0转换为false

逻辑运算符
逻辑运算符用于测定变量或值之间的逻辑。

&&	and   （且）
||	or      （或）
！	not     （非）

等号运算符，逗号运算符
运算符	含义
==	等于，比较的是内容
===	全等，比较的是内容和数据类型
!=	不等于，判断的是内容
!==	不全等于，判断的是内容和数据类型

	var a=5, b=6, c=7;
	a=b+c,c=a+b;


