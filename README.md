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
![��ҳ](https://github.com/nl30du/blog/blob/master/blog/lyops/pic/index.png)
3.**�û��б�**����ʾ�����û���Ϣ(id����ʵ�û�����¼�û�Ȩ�ޣ�����ָ�ƣ�����key��������Ŀ�������û����ʵ�)��
![�û��б�](https://github.com/nl30du/blog/blob/master/blog/lyops/pic/userlist.png)
4.**�û����**��ѡ���Ӧ��Ŀ�Լ��û�Ȩ�����ͣ�ִ����Ӳ��������ں�ִ̨�гɹ��󷵻ض�Ӧ��Ϣ��ҳ�档
![�û����](https://github.com/nl30du/blog/blob/master/blog/lyops/pic/useradd.png)
5.**��Ŀ����**����Ӷ�Ӧ��Ŀ(�пػ�)���û����������Կ��֤��
![��Ŀ����](https://github.com/nl30du/blog/blob/master/blog/lyops/pic/managepro.png)
6.**�����¼**��ʾ�û�����������Ϊ��¼��
![��Ŀ����](https://github.com/nl30du/blog/blob/master/blog/lyops/pic/commandlist.png)

## ��װ
��װ�ر����

```
yum -y update && yum -y install mysql-devel wget epel-release python-devel gcc c++ make openssl openssl-devel passwd libffi libffi-devel
yum -y install ansible
wget https://bootstrap.pypa.io/get-pip.py
python get-pip.py
```

mysql-5.6��װ
```
��װ��ʽ(��),ע���޸�mysql�ַ���Ϊutf8
������Ӧ�����ݿ⣺
mysql>CREATE DATABASE `lyops` DEFAULT CHARACTER SET utf8;
```

����django�����ļ�lyops/settings.py

```
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'lyops',
        'USER': '��Ӧ��Ȩ�û���',
        'PASSWORD': '��Ӧ��Ȩ�û�����',
        'HOST': 'IP',
        'PORT': 'PORT',
    }
}
```


������Щ��������ɺ�Ϳ��Բ�����Ŀ��

��װ����

pip install -r requirements.txt

ͬ�����ݿ�

python manage.py makemigrations

python manage.py migrate

��������Ա

python manage.py createsuperuser

runserver���м���Ƿ�����

python manage.py runserver 0.0.0.0:8080

����޷��������У��������ϲ���

����·����
http://ip:8080/ops/
  
email��tangcc_tl@163.com  


Ŀ����������װ��

	1��openssh-server�İ汾Ҫ������6.6p
	2����������ɺ��޸�sshd�������ļ���Ȼ����������
		AuthorizedKeysCommand /sbin/fetchkey.sh
		AuthorizedKeysCommandUser root
	3���ϴ�fetchkey.sh��prelogin.sh�����ļ�(Դ����scripts/)��/sbin/Ŀ¼�£������ִ��Ȩ��
	
syslog-ng����װ��
	����
	
	
	
PS:
  һ��Ҫ��֤�пػ�(�����)openssh-server�İ汾һ����Ϊ6.6p�����ĵİ汾δ���� 	
  �������к���ʽ������ò���django+nginx+uwsgi(gunicorn)����  
  


ˮƽ��������¡�

