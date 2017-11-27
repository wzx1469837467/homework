1. DOM概述
2. ***DOM树
3. *查找
感觉还是把DOM和BOM先看完吧 传智讲DOM和BOM不详细 就讲了一天 达内讲了5天
DHTML
所有能够实现动态网页技术的统称
	DHTML=HTML+css+js
HTML XHTML DHTML XML:
HTML：超文本标记语言，专门编写网页内容的语言
XHTML：严格的HTML语言
XML:可扩展的标记语言
      可以自定义标签 在HTML的语法上完全相同
	<演员>
		<姓名>范冰冰</姓名>
		<数学>91</数学>
		<语文>66</语文>
		<英语>88</英语>
	</演员> 自描述
专门用来储存/传输自描述的结构化数据（标签太多 耗费流量过大）
逐渐被json替代了
json：java 对象表示方法
JSON：JavaScript 对象表示法（JavaScript Object Notation）。
JSON 是存储和交换文本信息的语法。类似 XML。
JSON 比 XML 更小、更快，更易解析。
"{"姓名":"范冰冰"，"数学":91,...}"--json
HTML和XHML的差别 一个是超文本 一个是可扩展

	 history前进后退的按钮
		                     lmage	
	 navigator浏览器的设置      anchor                    textarea
                                    lframe	
window:窗口--document窗口中加载的页面文档-------form-------                  lnput
					
	 location浏览器的地址		                   select	
	
	 screen显示         table---             tablecell
	                                    tablerow  
	 event事件发生时创建的对象

BOM  VS DOM
BOM:浏览器对象模型（API），专门操作浏览器窗口的API
没有标准 但规范支持
DOM：文档对象模型（API），专门操作网页内容的API
	可以对网页中任意对象，做任何修改
	DOM是标准，90%以上浏览器的严格兼容

DOM 概述
DOM是W3C（万维网联盟）的标准，是中立于平台和语言的接口，它允许程序和脚本动态地访问
和更新文档的内容，结构和样式
W3C DOM 标准被分为3个不同的部分
核心DOM 针对任何结构化文档的标准模型 在实际开发中和HTMLDOM混合使用
XMLDOM 针对XML文档的标准模型
HTMLDOM 针对HTML文档的标准模型 能简化就用HTMLDOM


核心DOM：操作所有结构化文档（XML,HTML）的通用API
HTML DOM：针对HTML文档的简化API
HTML DOM 不能完成所有功能，实际开发中都是核心DOM与HTMLDOM配合使用

HTML DOM：网页中一切都是对象（元素，属性,文字）
	  同一网页中的所有对象，在内存中父子相连，形成一棵DOM树。

DOM 标准发展历程

DOM标准发展至今，共三级：
	DOM1级规范:98年,最初的DOM规范.定义文档内容的底层结构.所有浏览器100%都兼容。
	DOM2级规范基于DOM4级增加了许多交互模块，比如:
	1.DOM Level 2 Core:基于DOM1扩展更多方法和属性
	2.DOM Level 2 style:专门踩着HTML样式的APL
	3.DOM Level 2 Traversal and Range:专门遍历DOM树结构的APL
	4.DOM Level 2 Event:标准化事件API。仅IE8不支持，自成一套
	DOM3级规范：进一步扩展了方法和属性，添加了新类型。
DOM操作
通过可编程的对象模型，JavaScript获得了足够的能力
来创建动态的HTML
查找节点信息
修改节点信息
创建新节点
删除节点

常用DOM方法
getElementById()
getElementsByTagName()
getElementsByClassName()
appendChild()
removeChild()
replaceChild()
insertBefore()
createAttribute()
createElement()
getAttribute()
setAttribute()

常用DOM属性
innerHTML
parentNode
childNodes
attributes

2***DOM树
	文档中的每个元素，属性，文字注释，都被看做一个节点对象--Node--所有节点对象的父类型
	当网页被加载进内存时，浏览器会为网页创建一个document对象。所有节点对象都是document对象的子节点
	document，封装了对网页中所有子节点的增加，删除，查找

	Node类型定义了3个公共属性
	nodetype：节点的类型的数值
	何时使用：专门用于判断获得的节点类型
		如果是元素节点，返回4
		如果是文本节点，返回3
	nodeName:节点的名称
	何时使用：专门用于判断获得的标签名
	 如果是元素节点，返回标签名:
	如果是文本节点，返回#text
	强调：nodeName返回的都是大写标签名
  nodeValue：节点的值