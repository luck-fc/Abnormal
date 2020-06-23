## RecyclerView 
* 连续滚动bug （Cannot call this method in a scroll callback. Scroll callbacks might be run during a measure & layout pass where you cannot change the RecyclerView data）  

    * 解决方案：
    
    ~~~java
    RecyclerView.post(new Runnable() { 
        @Override 
        public void run() { 
            RecyclerView.Adapter.notifyDataSetChanged();
        } 
    });
    ~~~

## AnimatorSet
* AnimatorSet.playTogether(ObjectAnimator,ObjectAnimator,...);动画监听在android 7.0不同步。  

    * 解决方案：
    
   ~~~txt
   给每个ObjectAnimator都添加Animator.AnimatorListener然后给自个view进行操作
   ~~~
## Received close_notify during handshake

问题存在原因：这是Android编译错误，jcenter里面的东西下载不了引起的。

问题解决：在项目的build.gradle文件中将jcenter()换成阿里的源，具体示例代码如下。修改之后再重新Sync Project即可。

~~~gradle
buildscript {
    ext.kotlin_version = '1.3.50'
    repositories {
        google()
        // jcenter()
        maven{ url'http://maven.aliyun.com/nexus/content/groups/public/' }
        maven{ url'http://maven.aliyun.com/nexus/content/repositories/jcenter'}
        
    }
    dependencies {
        classpath 'com.android.tools.build:gradle:3.5.3'
        classpath "org.jetbrains.kotlin:kotlin-gradle-plugin:$kotlin_version"
        // NOTE: Do not place your application dependencies here; they belong
        // in the individual module build.gradle files
    }
}

allprojects {
    repositories {
        google()
        // jcenter()
        maven{ url'http://maven.aliyun.com/nexus/content/groups/public/' }
        maven{ url'http://maven.aliyun.com/nexus/content/repositories/jcenter'}
        
    }
}
~~~
