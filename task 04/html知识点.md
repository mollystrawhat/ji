##### 1. HTML、XML、XHTML 有什么区别
网页编码发展过程：html-->xhtml-->xml

|HTML | XHTML | XML |
| :-------------: |:-------------:| :-----:| 
| 超文本编辑语言 | 可扩展超文本标记语言 | 可扩展标记语言 |
|最早写网页的语言，但是由于时间早，规范不是很好，大小写混写且编码不规范| 对html进行了规范，编码更加严谨纯洁|一种跨平台语言，编码更自由，可以自由创建标签 |  
| 编码不规范，结构混乱臃肿，需要智能的终端才能很好的显示;表现和结构混乱，不利于开发和维护;不能使用更多的网络设备，比如手机、PDA等 | 元素必须要有结束标签；元素必须嵌套；name属性是不赞成使用的|严格区分大小写 |


##### 2. 怎样理解 HTML 语义化
语义化是标签内容语义化，在表现结构的同时告诉我们每个标签的的作用。例如下图中并没有出现div标签，依然完成了整个布局，其中的header标签就告诉我们这是网页的头部。选择合适的标签可以便于开发者阅读和写出更优雅的代码，HTML 语义化对浏览器更友好。
![](http://upload-images.jianshu.io/upload_images/5804931-77050525c7605cf8.jpg?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
###### 标签语义化的好处
- 方便机器理解代码,利于SEO（搜索引擎优化）。
使搜索引擎爬虫更好的理解你的代码，你的网站排名自然有加分了。
- 代码更简洁，复用性更高。使用合适的标签，可以少些很多css或者js
例如h1~h6标签本身具有不同的font-size，没有特殊要求不用css来设置，而且可以重复使用。
- 访问性更好
这个主要就是针对读屏器或者其他一些对CSS理解不好的浏览器。语义化的HTML可以做到脱离CSS还能看，而非语义化的就难了
##### 3. 怎样理解内容与样式分离的原则
内容主要由html负责，样式主要由css负责，而js主要负责行为
##### 4. 有哪些常见的meta标签
- 申明编码
```<meta charset='utf-8' />
- 优先使用 IE 最新版本和 Chrome

><meta http-equiv="X-UA-Compatible" content="IE=edge,chrome=1" />
<!-- 关于X-UA-Compatible -->
<meta http-equiv="X-UA-Compatible" content="IE=6" ><!-- 使用IE6 -->
<meta http-equiv="X-UA-Compatible" content="IE=7" ><!-- 使用IE7 -->
<meta http-equiv="X-UA-Compatible" content="IE=8" ><!-- 使用IE8 -->

- 浏览器内核控制
国内浏览器很多都是双内核（webkit和Trident）,webkit内核高速浏览，IE内核兼容网页和旧版网站。 而添加meta标签的网站可以控制浏览器选择何种内核渲染。
搜狗高速浏览器、QQ浏览器：IE内核（兼容模式）
360极速浏览器、遨游浏览器：Webkit内核（极速模式）
 
 > <meta name="renderer" content="webkit|ie-comp|ie-stand">





- 禁止浏览器从本地计算机的缓存中访问页面内容
这样设定，访问者将无法脱机浏览。

> <meta http-equiv="Pragma" content="no-cache">
- 避免百度转码申明
用百度打开网页可能会对其进行转码（比如贴广告），避免转码可添加如下meta

> <meta http-equiv="Cache-Control" content="no-siteapp" />

- 页面关键词
每个网页应具有描述该网页内容的一组唯一的关键字, 不要太短也不要太长

> <meta name="keywords" content="your tags" />
- 页面描述
每个网页都应该有一个不超过150个字符的页面描述

> <meta name="description" content="150 words" />

- 设置搜索引擎索引方式

> <meta name="robots" content="index,follow" />
<!--
    all：文件将被检索，且页面上的链接可以被查询；
    none：文件将不被检索，且页面上的链接不可以被查询；
    index：文件将被检索；
    follow：页面上的链接可以被查询；
    noindex：文件将不被检索；
    nofollow：页面上的链接不可以被查询。
 -->









##### 5. 文档声明的作用?严格模式和混杂模式指什么?<!doctype html> 的作用?
<!DOCTYPE>声明叫做文件类型定义（DTD），声明的作用为了告诉浏览器该文件的类型。让浏览器解析器知道应该用哪个规范来解析文档。<!DOCTYPE>声明必须在 HTML 文档的第一行，这并不是一个 HTML 标签。
- 严格模式：又称标准模式，是指浏览器按照 W3C 标准解析代码。

- 混杂模式：又称怪异模式或兼容模式，是指浏览器用自己的方式解析代码。
- 如何区分：浏览器解析时到底使用严格模式还是混杂模式，与网页中的 DTD 直接相关。
<!doctype html> 是说明代码是按照html5的规范来写的。

##### 6. 浏览器乱码的原因是什么？如何解决
- 网站头部设定的编码和网页本身的编码不一致导致的，html网页头部代码：<meta http-equiv="Content-Type" content="text/html; charset=gb2312" />是告诉浏览器该用什么编码来读取网页的内容，然后浏览器就会启用相应的解码来程序内容，同时，网站本身还存在一个编码的机制，中国人一般使用gbk、gb2312、utf-8编码，如果网站制作者将网页文件存储为了gbk格式，然后在网页头部却设置了utf-8的格式，那么浏览器在读取网页的时候就会将中文或其他非英文和数字的字符解析成乱码。
如果是这种编码错误，解决办法很简单，将解码方式和文件存储的编码修改成一致即可，浏览者在遇到此类情况，可以在网页空白处右键-编码种选择多种编码方式试试，就可以看到乱码的文字了。
?
- 不合理的字符串截取造成个别字符乱码，在gbk和gb2312编码下，中文是占用两个字节，而在utf-8编码模式下，中文字符占用三个字节，而英文和数字都是占用一个字节，如果用英文的一些截取方式去截取中文字符的话，就可能出现将一个中文截断的现象，网页就会出现中文乱码，而gbk和utf-8的中文截取手段也不一样。
这种情况的解决办法就是规范截取字符串的函数，因地制宜。
?
- 数据库编码问题导致，这种情况在mysql中经常出现，因为mysql等一些数据库支持存储各种编码的字符串，并且也有编码的区分，?读取数据库的方式这个很关键，必须和网页的头部设定和存储编码一致，如果不一致就会出现乱码。
?
- AJAX传递中文编码导致的，AJAX在传递中文数据的时候只支持UTF-8编码的中文，所以如果尝试用其他编码方式传递的话就会出现乱码，解决办法是在传递中文数据前就将中文数据转码成utf-8。

##### 7. 常见的浏览器有哪些，什么内核

- Trident-IE浏览器内核 
- Gecko-火狐浏览器内核Mozilla 
- Blink(Webkit的分支)-谷歌浏览器内核 
- Presto，现为Blink-Opera浏览器内核
##### 8. 列出常见的标签，并简单介绍这些标签用在什么场景

|标签|应用场景|
|--------|----------|
|h1~h6|标题|
|p|段落|
|img|插入图片|
|a|插入一个链接|
|ul    li|制作导航栏|
|table dt dl dd|制作表格|
|article|独立的自包含内容|
|audio|插入一段音频|
|body|文档的主体|
|button|定义一个按钮|
|div|独立的自包含内容，是块级元素|
|form|为用户输入创建 HTML 表单|
|header|标签定义文档的页眉（介绍信息）|
|script|在 HTML 页面中插入一段 JavaScript|
|title|元素可定义文档的标题|



参考:
[html和xhtml和xml的区别](http://www.cnblogs.com/fredshare/archive/2011/11/10/2244308.html)
[关于HTML语义化的一些理解](http://www.cnblogs.com/season-huang/p/3548514.html)
[meta常用属性](https://tink.gitbooks.io/fe-collections/content/ch02-html/s03-meta.html)
[网站制作](http://www.kmwzjs.com/)
