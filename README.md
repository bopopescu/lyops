# lyops
+ ʹ��Django��ܿ�������ά����ƽ̨
+ ��������: python;
+ ��˿��: Django;
+ ǰ�˿�ܣ�bootstrap/jquery��
+ ��Ŀ���ܣ������û�Ȩ�޼��п����Լ��û�������Ϊ���(�����)���Զ�������(������)�����ù���(�ƻ���)�����̹���(�ƻ���)��

## ������
+ RHEL 6.8 x86_64
+ django-1.11
+ ansible-2.4.2
+ ansible-api-2.3.0
+ python 2.7
+ MySQL 5.6
+ syslog-ng-3.2.5

## lyops���¼�¼��
    > ansible-api��ع��ܷ�װ(ָ��ģ��ִ�С���̬�������籾ִ�С��ص���д)��
    > �Զ�������ǰ��ҳ�湹��(������)��
    > Ȩ����ƹ�����ɣ�
    > ҳ���û��������(������ʾ����ӵ��û�)��

## ���ܽ���
1.**��½ҳ��**
![��½](https://github.com/nl30du/blog/blob/master/blog/lyops/pic/login.png)
2.**��ҳ**����ʾƽ̨һЩ˵����Ϣ�ȡ�
![�Ǳ���]()
3.**�����б�**
���������б���棬����ѡ�������ά����Ա��ʹ��ajax����ÿ��ѡ���ӿ������²�ѯ�������������ݣ�
��Щ��������ص���Ϣ֧���Զ��ɼ�������Ŀǰд�ķ���ֻ����ɲɼ��������Բ�û�н����ӷų�������������ͨ������ָ�����ӽ��з��ʡ�
![�����б�](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/asset.png)
4.**SaltStack**
��������¹��ܣ�
+ ��������ʼ������ģ�鲿��ȣ�
+ �������ø���
+ �ճ�ά������
+ Զ������ִ��
����Minionִ�в���ʱ�����¼����Ŀ��Minion��������Ȼ���뷵�ؽ����Minion�������жԱȣ��ҳ���Щû�з��ؽ���������յ����ؽ����ʹ��bootstrap��ģ̬����ʾ�����������ɫ��ʾִ�гɹ�����ɫ��ʾ��ʧ�ܴ��ڣ����Ե����ǩ�鿴��ϸ�����
![ģ�鲿��](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/deploy.png)
![ģ�鲿��-���ؽ��-ģ̬��չ��-ʧ�����](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/deploy_show.png)
![ģ�鲿��-���ؽ��-ģ̬��չ��-�ɹ����](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/deploy_show_success.png)
![Զ������ִ��](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/execute.png)
5.**MinionKeys����**
���Էֱ�ѡ���ѽ��ܡ������ܡ��Ѿܾ������ҿ���ѡ�������ά����Ա�����ж�Ӧ�Ĺ��������
![MinionKeys����](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/manage.png)
6.**������¼**
���Լ�¼ÿ�β���ִ���˵��˺š�������Ŀ�ꡢ��jid��������ͨ��jid�鿴�ôβ����ķ��ؽ����ϸ�����
![������¼](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/record.png)
![������¼-��ϸ](https://github.com/Hasal/dzhops_picture/blob/master/dzhops_pic/record_detail.png)
7.**����ϸ�ڲ���׸��**
