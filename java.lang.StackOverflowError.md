# Abnormal
Problems encountered in the development of Android

[java.lang.StackOverflowError.md](https://github.com/luck-fc/Abnormal/blob/master/java.lang.StackOverflowError.md)

#StackOverflowError是由于当前线程的栈满了  ，也就是函数调用层级过多导致。#
**一.无限递归** 
	同一个方法没有截止的自己调用自己就很出现该bug
	
**二.Gson解析导致如下错误信息，因为使用到了context** 

 java.lang.StackOverflowError
 at java.lang.Class.isArray(Class.java1044)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java331)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java375)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java380)
 at com.google.gson.internal.$Gson$Types.resolve($Gson$Types.java355)
at com.google.gson.internal.bind.ReflectiveTypeAdapterFactory.getBoundFie

 **三.其他 有待发现添加**  
 