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

