/while/ 

循环会在指定条件为真时循环执行代码块。
while (条件)
  {
  需要执行的代码
  }
while循环语句需现在循环体外定义变量。

<script>
function myFunction()
{
	var x="",i=0; 
	while (i<5) //条件 0-5 结束循环
  	{
  	x=x + "The number is " + i + "<br>";
  	i++;
  }
document.getElementById("demo").innerHTML=x;
}
</script>

/do while/

do{
循环体代码；首先执行该循环体代码一次。
如果while后边的表达式结果为true,该循环体会一直循环。
如果结果false,该循环终止。
}while(条件表达式)

do while 比 while 循环多循环一次

var n1=1；
var n2=5；
	do{
	 alert（"n1>n2"）;
	}while(n1>n2)

/for循环/

for (语句 1; 语句 2; 语句 3)
  {
  被执行的代码块
  }
<script>
      function myFunction()
      {
	var x="";
	for (var i=0;i<5;i++)
 	 {
  	   x=x + "The number is " + i + "<br>";
  	 }
	document.getElementById("demo").innerHTML=x;
      }
</script>
如果条件表达式结果为true的时候，执行for循环里的代码，如果为false，循环体代码终止执行。
先执行变量和条件表达式循环一次，再执行自增自减。

/break语句/

在循环体内，只要代码遇到break,程序立马结束当前循环。
当前循环指的是break语句所在的循环体。

/continue语句/

Continue语句指的是跳出本次循环，该语句后面的代码不再执行,整个循环体继续循环。