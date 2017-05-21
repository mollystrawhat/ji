####1.form表单有什么作用？有哪些常用的input 标签，分别有什么作用？
><form> 标签用于为用户输入创建 HTML 表单。
表单能够包含 input 元素，比如文本字段、复选框、单选框、提交按钮等等。
表单还可以包含 menus、textarea、fieldset、legend 和 label 元素。
表单用于向服务器传输数据。

######常用input标签
```<input type="text">输入的内容为文本，且为单行
 <input type="password">输入的内容为密码，显示为一个一个的点
 <input type="button">按钮
 <input type="submit">提交按钮
 <input type="image">图片提交按钮
 <input type="reset">重置按钮
 <input type="radio">单选按钮
 <input type="checkbox">复选框
 <input type="file">上传文件
 <input type="hidden">隐藏整个字段 ```



####2.post 和 get 方式的区别？

######2.1 提交的数据放置的位置不同
GET请求的数据会附在URL之后（就是把数据放置在HTTP协议头中），以?分割URL和传输数据，参数之间以&相连，如：login.action?name=hyddd&password=idontknow&verify=%E4%BD%A0%E5%A5%BD。如果数据是英文字母/数字，原样发送，如果是空格，转换为+，如果是中文/其他字符，则直接把字符串用BASE64加密，得出如：%E4%BD%A0%E5%A5%BD，其中％XX中的XX为该符号以16进制表示的ASCII。
POST把提交的数据则放置在是HTTP包的包体中。

######2.2 提交数据字节限制
- Get传输的数据有大小限制，因为GET是通过URL提交数据，那么GET可提交的数据量就跟URL的长度有直接关系了，不同的浏览器对URL的长度的限制是不同的。实际上，URL不存在参数上限的问题，HTTP协议规范没有对URL长度进行限制。这个限制是特定的浏览器及服务器对URL长度的限制。
- 理论上讲，POST是没有大小限制的，HTTP协议规范也没有进行大小限制，POST数据是没有限制的，起限制作用的是服务器的处理程序的处理能力。
　　
######2.3 POST的安全性要比GET的安全性高
- GET请求的数据会被浏览器缓存起来，用户名和密码将明文出现在URL上，其他人可以查到历史浏览记录，数据不太安全。
- POST没有限制提交的数据。POST比GET安全，当数据是中文或者不敏感的数据，则用GET，因为使用GET，参数会显示在地址，对于敏感数据和不是中文字符的数据，则用POST使用GET提交数据还可能会造成Cross-site request forgery攻击。


整体来说，GET是向服务器发索取数据的一种请求，而POST是向服务器提交数据的一种请求，在FORM（表单）中，Method默认为"GET"，实质上，GET和POST只是发送机制不同，并不是一个取一个发。



####3.在input里，name 有什么作用？

- name 属性规定 input 元素的名称。通过name属性对不同的input标签进行分类，相同的name标签为一组。
- name 属性用于对提交到服务器后的表单数据进行标识，或者在客户端通过 JavaScript 引用表单数据。
- 只有设置了 name 属性的表单元素才能在提交表单时传递它们的值。
####4.radio 如何 分组?
通过设置name属性使radio分组，相同name的input标签分为一组。
例如下面name为sex的为一组，fruit为一组
```<input type="radio" name="sex" value="male">男
 <input type="radio" name="sex" value="female">女
<input type="checkbox" name="fruit" value="apple">苹果
 <input type="checkbox" name="fruit" value="pear">梨
 <input type="checkbox" name="fruit" value="banana">香蕉```


####5.placeholder 属性有什么作用?
- placeholder 属性提供可描述输入字段预期值的提示信息（hint）。
- 该提示会在输入字段为空时显示，并会在字段获得焦点时消失。
- placeholder 属性适用于以下的 <input> 类型：text, search, url, telephone, email 以及 password。

举例：```<input type="text" placeholder="请输入密码">```

效果：![placeholder.png](http://upload-images.jianshu.io/upload_images/5804931-a12f72d4325e950a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




####6.type=hidden隐藏域有什么作用? 举例说明
隐藏域在页面中对于用户是不可见的，在表单中插入隐藏域的目的在于收集或发送信息，以利于被处理表单的程序所使用。浏览者单击发送按钮发送表单的时候，隐藏域的信息也被一起发送到服务器。

![hidden.png](http://upload-images.jianshu.io/upload_images/5804931-1a66eaa5935351b4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#####7.简单介绍 HTML 表单的用法
######作用：
HTML 表单用于搜集不同类型的用户输入。
######form 属性：

![form.png](http://upload-images.jianshu.io/upload_images/5804931-4efb2f9e615e79ad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
######表单元素：
- <input> 元素
最重要的表单元素是 <input> 元素。<input> 元素根据不同的 type 属性，可以变化为多种形态。
- <select> 元素（下拉列表）和option配合使用
- <option> 元素定义待选择的选项。列表通常会把首个选项显示为被选选项。可通过添加 selected 属性来定义预定义选项。
- <textarea> 元素定义多行输入字段（文本域）
- <button> 元素定义可点击的按钮
- <datalist> 元素为 <input> 元素规定预定义选项列表。用户会在他们输入数据时看到预定义选项的下拉列。<input> 元素的 list 属性必须引用 <datalist> 元素的 id 属性。
><form action="action_page.php">
<input list="browsers"> 
<datalist id="browsers">
   <option value="Internet Explorer">
   <option value="Firefox">
   <option value="Chrome">
   <option value="Opera">
   <option value="Safari">
</datalist> 
</form>

参考资料：
[Http方法：Get请求与Post请求的区别](https://www.douban.com/note/180488791/)
[html中隐藏域hidden的作用介绍及使用示例](http://www.jb51.net/web/100210.html)
[浅谈HTTP中Get与Post的区别](http://www.cnblogs.com/hyddd/archive/2009/03/31/1426026.html)
[Http方法：Get请求与Post请求的区别](https://www.douban.com/note/180488791/)
[w3cschool](http://www.w3school.com.cn)