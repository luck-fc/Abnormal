# Abnormal
Problems encountered in the development of Android

[java.lang.NullPointerException](https://github.com/luck-fc/Abnormal/blob/master/java.lang.NullPointerException.md)

**һ.����û�г�ʼ����ֵ** 

       1.activity fragment �Զ���View�ȵ��е�viewû��findViewById�ȷ�ʽ��ֵ��ֱ��ʹ��
       2.�Զ����ϵͳ����δͨ��new()�����������ʽ��ֱֵ��ʹ��
       3.���÷������Զ��巽����ֵΪnull������������ڲ�δ�����ж�ֱ��ʹ��
       4. ����~~~

**��.�����г�ʼ��������ʹ����Ϊnull**
 
        1.activity framgnt �����첽���񣬵��첽���������activity��fragment�����ջ��߹ر�ȡ�����������ʱ��
          (1).���˱�����context������صĲ��������磺��ȡsharepreference�������Ի��򣬲������ݿ�ȵȣ�
          (2).ʹ���˵�ǰ�������µ�view����UI���������磺textView.setText() view.setvisibility()�ȵȣ�
         
         ���������
                ��Ҫ������������֮ǰ ���жϵ�ǰactivity�Ƿ����� ���� fragment��ȡ���������ٵ�Ȼ����ʹ�� 
<code>
     if (activity.isFinishing()) {
        return;
     }
 </code>
         ƫ����
         ��������һ��Application List�����������Activity,ÿ��Activity onCreateʱadd��List,ÿ��Activity onDestroyʱremove,��ʱֻҪ�ж�List�����Ƿ����ָ����Activity������

  **��.���� �д�����**              
