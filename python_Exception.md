# Abnormal
Problems encountered in Python development

[python_Exception.md](https://github.com/luck-fc/Abnormal/blob/master/python_Exception.md)

* 1.UnboundLocalError: local variable 'Variable name' referenced before assignment
该异常是 python 局部变量和全局变量 global使用不当引发的异常。 
局部使用全局数据正确方式
~~~python
num = 0
def addnum():
	global num
	num++
~~~

* 2.NameError: name 'Variable name' is not defined
Variable name 未定义 定义变量应该指定数据类型，不然操作该变量会引发该异常

* 3.TypeError: coercing to Unicode: need string or buffer, NoneType found
类型不对转换异常
正确使用方式
~~~python
 'a'+str(b)
~~~

* 4.UnicodeEncodeError: 'ascii' codec can't encode characters in position 0-1: ordinal not in range(128)
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