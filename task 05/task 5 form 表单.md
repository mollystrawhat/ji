####1.form����ʲô���ã�����Щ���õ�input ��ǩ���ֱ���ʲô���ã�
><form> ��ǩ����Ϊ�û����봴�� HTML ����
���ܹ����� input Ԫ�أ������ı��ֶΡ���ѡ�򡢵�ѡ���ύ��ť�ȵȡ�
�������԰��� menus��textarea��fieldset��legend �� label Ԫ�ء�
��������������������ݡ�

######����input��ǩ
```<input type="text">���������Ϊ�ı�����Ϊ����
 <input type="password">���������Ϊ���룬��ʾΪһ��һ���ĵ�
 <input type="button">��ť
 <input type="submit">�ύ��ť
 <input type="image">ͼƬ�ύ��ť
 <input type="reset">���ð�ť
 <input type="radio">��ѡ��ť
 <input type="checkbox">��ѡ��
 <input type="file">�ϴ��ļ�
 <input type="hidden">���������ֶ� ```



####2.post �� get ��ʽ������

######2.1 �ύ�����ݷ��õ�λ�ò�ͬ
GET��������ݻḽ��URL֮�󣨾��ǰ����ݷ�����HTTPЭ��ͷ�У�����?�ָ�URL�ʹ������ݣ�����֮����&�������磺login.action?name=hyddd&password=idontknow&verify=%E4%BD%A0%E5%A5%BD�����������Ӣ����ĸ/���֣�ԭ�����ͣ�����ǿո�ת��Ϊ+�����������/�����ַ�����ֱ�Ӱ��ַ�����BASE64���ܣ��ó��磺%E4%BD%A0%E5%A5%BD�����У�XX�е�XXΪ�÷�����16���Ʊ�ʾ��ASCII��
POST���ύ���������������HTTP���İ����С�

######2.2 �ύ�����ֽ�����
- Get����������д�С���ƣ���ΪGET��ͨ��URL�ύ���ݣ���ôGET���ύ���������͸�URL�ĳ�����ֱ�ӹ�ϵ�ˣ���ͬ���������URL�ĳ��ȵ������ǲ�ͬ�ġ�ʵ���ϣ�URL�����ڲ������޵����⣬HTTPЭ��淶û�ж�URL���Ƚ������ơ�����������ض������������������URL���ȵ����ơ�
- �����Ͻ���POST��û�д�С���Ƶģ�HTTPЭ��淶Ҳû�н��д�С���ƣ�POST������û�����Ƶģ����������õ��Ƿ������Ĵ������Ĵ���������
����
######2.3 POST�İ�ȫ��Ҫ��GET�İ�ȫ�Ը�
- GET��������ݻᱻ����������������û��������뽫���ĳ�����URL�ϣ������˿��Բ鵽��ʷ�����¼�����ݲ�̫��ȫ��
- POSTû�������ύ�����ݡ�POST��GET��ȫ�������������Ļ��߲����е����ݣ�����GET����Ϊʹ��GET����������ʾ�ڵ�ַ�������������ݺͲ��������ַ������ݣ�����POSTʹ��GET�ύ���ݻ����ܻ����Cross-site request forgery������


������˵��GET�������������ȡ���ݵ�һ�����󣬶�POST����������ύ���ݵ�һ��������FORM�������У�MethodĬ��Ϊ"GET"��ʵ���ϣ�GET��POSTֻ�Ƿ��ͻ��Ʋ�ͬ��������һ��ȡһ������



####3.��input�name ��ʲô���ã�

- name ���Թ涨 input Ԫ�ص����ơ�ͨ��name���ԶԲ�ͬ��input��ǩ���з��࣬��ͬ��name��ǩΪһ�顣
- name �������ڶ��ύ����������ı����ݽ��б�ʶ�������ڿͻ���ͨ�� JavaScript ���ñ����ݡ�
- ֻ�������� name ���Եı�Ԫ�ز������ύ��ʱ�������ǵ�ֵ��
####4.radio ��� ����?
ͨ������name����ʹradio���飬��ͬname��input��ǩ��Ϊһ�顣
��������nameΪsex��Ϊһ�飬fruitΪһ��
```<input type="radio" name="sex" value="male">��
 <input type="radio" name="sex" value="female">Ů
<input type="checkbox" name="fruit" value="apple">ƻ��
 <input type="checkbox" name="fruit" value="pear">��
 <input type="checkbox" name="fruit" value="banana">�㽶```


####5.placeholder ������ʲô����?
- placeholder �����ṩ�����������ֶ�Ԥ��ֵ����ʾ��Ϣ��hint����
- ����ʾ���������ֶ�Ϊ��ʱ��ʾ���������ֶλ�ý���ʱ��ʧ��
- placeholder �������������µ� <input> ���ͣ�text, search, url, telephone, email �Լ� password��

������```<input type="text" placeholder="����������">```

Ч����![placeholder.png](http://upload-images.jianshu.io/upload_images/5804931-a12f72d4325e950a.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)




####6.type=hidden��������ʲô����? ����˵��
��������ҳ���ж����û��ǲ��ɼ��ģ��ڱ��в����������Ŀ�������ռ�������Ϣ�������ڱ�������ĳ�����ʹ�á�����ߵ������Ͱ�ť���ͱ���ʱ�����������ϢҲ��һ���͵���������

![hidden.png](http://upload-images.jianshu.io/upload_images/5804931-1a66eaa5935351b4.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

#####7.�򵥽��� HTML �����÷�
######���ã�
HTML �������Ѽ���ͬ���͵��û����롣
######form ���ԣ�

![form.png](http://upload-images.jianshu.io/upload_images/5804931-4efb2f9e615e79ad.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
######��Ԫ�أ�
- <input> Ԫ��
����Ҫ�ı�Ԫ���� <input> Ԫ�ء�<input> Ԫ�ظ��ݲ�ͬ�� type ���ԣ����Ա仯Ϊ������̬��
- <select> Ԫ�أ������б���option���ʹ��
- <option> Ԫ�ض����ѡ���ѡ��б�ͨ������׸�ѡ����ʾΪ��ѡѡ���ͨ����� selected ����������Ԥ����ѡ�
- <textarea> Ԫ�ض�����������ֶΣ��ı���
- <button> Ԫ�ض���ɵ���İ�ť
- <datalist> Ԫ��Ϊ <input> Ԫ�ع涨Ԥ����ѡ���б��û�����������������ʱ����Ԥ����ѡ��������С�<input> Ԫ�ص� list ���Ա������� <datalist> Ԫ�ص� id ���ԡ�
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

�ο����ϣ�
[Http������Get������Post���������](https://www.douban.com/note/180488791/)
[html��������hidden�����ý��ܼ�ʹ��ʾ��](http://www.jb51.net/web/100210.html)
[ǳ̸HTTP��Get��Post������](http://www.cnblogs.com/hyddd/archive/2009/03/31/1426026.html)
[Http������Get������Post���������](https://www.douban.com/note/180488791/)
[w3cschool](http://www.w3school.com.cn)