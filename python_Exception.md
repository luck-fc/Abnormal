# Abnormal
Problems encountered in Python development

[python_Exception.md](https://github.com/luck-fc/Abnormal/blob/master/python_Exception.md)

### 1.UnboundLocalError: local variable 'Variable name' referenced before assignment
该异常是 python 局部变量和全局变量 global使用不当引发的异常。 
局部使用全局数据正确方式
~~~python
num = 0
def addnum():
	global num
	num+=1
~~~

### 2.NameError: name 'Variable name' is not defined
Variable name 未定义 定义变量应该指定数据类型，不然操作该变量会引发该异常

### 3.TypeError: coercing to Unicode: need string or buffer, NoneType found
类型不对转换异常
正确使用方式
~~~python
 'a'+str(b)
~~~

### 4.UnicodeEncodeError: 'ascii' codec can't encode characters in position 0-1: ordinal not in range(128)
编码问题
解决方式1：
~~~python
import sys
 
reload(sys)
sys.setdefaultencoding('utf-8')
~~~
解决方式2：
~~~python
result = urllib2.urlopen(req).read()
result = unicode(result,'GBK').encode('UTF-8')
~~~
万能解决方案
import chardet

~~~python

import chardet # 导入包https://pypi.python.org/pypi/chardet#downloads

typeEncode = sys.getfilesystemencoding()##這里得到的是系统默认编码
print chardet.detect(text)['encoding'] #这里打印出来的是就是text内容的的编码 
json_txt = text.decode(chardet.detect(text)['encoding'],'ignore').encode(typeEncode)
#或者 
infoencode = chardet.detect(text).get('encoding','utf-8')
json_txt = text.decode(infoencode,'ignore').encode(typeEncode)
~~~

### 5.IndexError: list index out of range
类似java常见的数组越界
