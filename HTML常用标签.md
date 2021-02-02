# HTML常用标签

学英文

| 英文   | A返图 |
| :----- | :---- |
| hyper  | 炒鸡  |
| blank  | 空白  |
| frame  | 框架  |
| canvas | 画布  |



### a 标签

+ #### 属性

  + ##### href  (hyper ref超链接)

    

    ![image-20210202192110195](https://i.loli.net/2021/02/02/2ZEtMvI4xbQlpyV.png)

    a href=#xxx 一个id 可以点击跳转id=xxx的命令（跳转到指定的页面 内部的锚点）

     http协议里，根目录是==http服务的目录==而不是 文件的根目录

    ``<a href="https://">超链接</a>``

    

  + ##### target

    ![image-20210202194410721](https://i.loli.net/2021/02/02/P9H8KdqUBT2fCp4.png)

    ``targer="_blank"``在空白页打开超链接

    top 最顶层页面

    self 当前页面（默认）

    

    ``target ="xxx"``打开id为xxx的窗口(windows.name)覆盖同一个窗口

    ``<a href="https://" taget="_blank">超链接</a>``

    

  + ##### download

    下载该网页 不靠谱

    

  + ##### rel=noopener

  

  + **iframe 标签**





### ②table标签

##### 写法

+ thead 表头

  + tr (table row)表列
    + th(表头)

+ tbody 

  + tr
    + td (table data)

+ tfoot（表尾）

  + tr
    + td

  ~~~html
      <table>
          <thead>
              <tr>
                  <th>英语</th>
                  <th>翻译</th>
              </tr>
          </thead>
          
          <tbody>
              <tr>
                  <td>target</td>
                  <td>目标</td>
              </tr>
  
              <tr>
                  <td>reference</td>
                  <td>引用</td>
              </tr> 
          </tbody>
  
          <tfoot>
          </tfoot>
  ~~~

  效果

  

![image-20210202201235106](https://i.loli.net/2021/02/02/m2QwLhtoYexEO9q.png)

+ **table相关的样式**

   + table-layout  CSS属性定义了用于布局表格*单元格*，*行*和*列*的算法

     ​		auto和fixed(auto宽度取决内容 fixed取决于首行的单元)

     ```
     table-layout: auto;
     table-layout: fixed;
     ```

   + border-collapse

     ​	边框是分开的还是合并的。在分隔模式下，相邻的单元格都拥有独立的边框。在合并模式下，相邻单元格共享边框。

     ``border-collapse: collapse``

     ![image-20210202221810844](https://i.loli.net/2021/02/02/dcWfmANoRbJ4D7X.png)

     ``border-collapse: separate;``

     ![image-20210202221820451](https://i.loli.net/2021/02/02/4ulBp6PIEamexNQ.png)

   + border-spacing

     指定相邻单元格边框之间的距离（只适用于 边框分离模式separate ）

     ​	``border-spacing: 10px``间隙10像素





### ③img标签

+ **发出get请求 展示一张图片**

  ​		``<img src="地址"/>``地址可写网络地址、相对路径

+ **属性**

  + **`alt`**

    定义了图像的备用文本描述，图片加载失败时将图像替换为图像所属 `<img>` 元素的 `alt` 属性所提供的文本。

  + ``height``，``width`` 高和宽 

    只定一个则另一个自适应

+ **事件**

  + ``onload``/``onerror``

    图片加载成功/加载失败 则进行什么动作（例：加载失败404

+ **响应式**

  ``max-width: 100%``

  最大宽度100% 手机放大缩小不会影响图片比例





### ④form标签

+ **作用**

  发get或post请求刷新页面

+ **属性**
  + ``action``  
  + ``method``  get还是post
  + ``autocomlete``自动填充
+ **事件**
  + ``onsubmit``



input和button:

button里面可以含有标签 但 input不可，只可以纯文本。button默认sumbit。

form必须接一个``type=submit`` 否则无法提交





### ⑤input 标签

+ **作用**

  让用户输入内容

+ **属性**

  type:

  ``button ``   ``checkbox ``  ``email ``  ``file``  ``hidden``  `` number``  `` password`` ``radio	``   ``search``  ``submit``  ``tel``  ``text``

  其他 ``name``





### 其他输入标签

+ **注意**

  一般不监听input的click

  form里的input要有name

  form要type=submit

  

### 感想

​	标签内容太多了，内容相对枯燥。只有跟着方老师一起操作才能保证不睡着，只单纯过一遍的话，感觉马上就忘了,需要边听边做笔记边一起和方老师操作

