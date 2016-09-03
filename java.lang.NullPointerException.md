# Abnormal
Problems encountered in the development of Android

[java.lang.NullPointerException](https://github.com/luck-fc/Abnormal/blob/master/java.lang.NullPointerException.md)

**一.对象没有初始化赋值** 

       1.activity fragment 自定义View等等中的view没有findViewById等方式赋值就直接使用
       2.自定义或系统对象未通过new()构造等其他方式赋值直接使用
       3.调用方调用自定义方法传值为null的情况，方法内部未进行判断直接使用
       4. 更多~~~

**二.对象有初始化，后续使用中为null**
 
        1.activity framgnt 中有异步任务，当异步任务结束后activity和fragment被回收或者关闭取消关联等情况时。
          (1).用了被回收context作了相关的操作（例如：获取sharepreference，创建对话框，操作数据库等等）
          (2).使用了当前被回收下的view进行UI操作（例如：textView.setText() view.setvisibility()等等）
         
         解决方案：
                需要操作以上两点之前 先判断当前activity是否被销毁 或者 fragment被取消关联销毁等然后再使用 
<code>
     if (activity.isFinishing()) {
        return;
     }
 </code>
         偏方：
         可以设置一个Application List变量用来存放Activity,每次Activity onCreate时add进List,每次Activity onDestroy时remove,到时只要判断List里面是否存在指定的Activity就行了

  **三.其他 有待发现**              
