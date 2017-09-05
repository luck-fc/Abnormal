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
