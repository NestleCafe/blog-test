# HTML



1980年，物理学家蒂姆·伯纳斯-李在欧洲核子研究中心（CERN）在承包工程期间，为使CERN的研究人员使用并共享文档，他提出并创建原型系统ENQUIRE。1989年，伯纳斯-李在一份备忘录中提出一个基于互联网的超文本系统。

#### 起手式

![image-20210202160915927](https://i.loli.net/2021/02/02/7T8hJjCDvf1dop2.png)

~~~html
<!DOCTYPE html>		//文档类型
<html lang="en">	//lang language 把lang可改成zh-CN
<head>
    <meta charset="UTF-8"> //文件字符编码
    <meta name="viewport" content="width=device-width, initial-scale=1.0">		//禁用缩放
    <title>Document</title>	//title标题
</head>
<body>
    
</body>
</html>
~~~



#### 章节标签

h1~h6 一级标题到六级标题

section 节

`  <footer>&copy; 版权所有</footer>`



### 全局属性标签

##### class 分类 标记

~~~html
[class = middle]{}
    可以简写为
    .middle{}
	//含有middle的class全算
~~~

不到万不得已 不要用 **id**  ，id不报错 也会误让人以为是唯一

~~~
[id = xxx]{}
同样可以简写为
#xxx{}
~~~

​     js会覆盖style



##### contenteditable 

使任何一个元素可以被编辑



##### hidden

隐藏元素



##### tabindex

使元素可用tab键移动 

tabindex=1 tab是第一个访问到的元素 按顺序

0是最后一个 -1是禁用



##### title

鼠标停留显示内容

经常与下面搭配

~~~html
white-space: nowrap; 不换行
text-overflow: elipsis; 溢出变成省略号
overflow: hidden; 溢出省略
~~~



![image-20210202170956812](https://i.loli.net/2021/02/02/dwrVUjufQneL5Gz.png)





#### 默认样式

##### 怎么看默认样式

+ Chrome开发者工具

  Element  -> Style -> user agent sylesheet

  User Agent就是浏览器

  

![image-20210202171946873](https://i.loli.net/2021/02/02/Hu2TqfBlYJjSacy.png)

##### CSS reset

默认样式以及不符合需求，干掉默认样式



![image-20210202173016377](https://i.loli.net/2021/02/02/Ip5jdMy2cwVA63H.png)

#### 内容标签

**ol** 	(ordered list)顺序列表 

​	ol里的子元素是**li** (list item)



**ul** (unordered list)无序列表

​	子元素同样是 li



**dl** (description list) 描述列表

​	元素是 **dt**(描述对象description term) 和 **dd**（描述内容）

​	dl声明一个描述列表，dt列出对象，dd是内容



**pre**	保留空格回车tab 用pre包起

通常与 code 一起用 不让空格回车不保留

![image-20210202174520903](https://i.loli.net/2021/02/02/nVHNJBkA5tMclpe.png)

**code** 展示代码



**hr** 分割线

**br** 换行



**a标签**



**em** 强调emphasis 默认斜体

**strong** 重要	默认粗体

**quote** 引用

**blockquote** 引用内容前多一个空格