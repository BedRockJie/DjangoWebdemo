# 这是图书管理web的创建过程，仅供学习使用
[toc]
## 1、创建Django开发环境和新建一个项目
- mkdir locallibrary  #网站创建一个文件夹
- cd locallibrary   #用cd命令进入文件夹
- django-admin startproject locallibrary #创建项目文件夹
- cd locallibrary
此时locallibrary的目录是:
```
locallibrary/
    manage.py
locallibrary/
   settings.py
   urls.py
   wsgi.py
```
### 创建Dgingo应用
```
python3 manage.py startapp catalog
```
此时文件结构
```
locallibrary/
    manage.py
    locallibrary/
    catalog/
        admin.py
        apps.py
        models.py
        tests.py
        views.py
        __init__.py
        migrations/
```

### 3、注册Django应用
在` locallibrary/locallibrary/settings.py `中找到`INSTALLED_APPS `
在列表的最后添加新的一行。
```
INSTALLED_APPS = [
    'django.contrib.admin',
    'django.contrib.auth',
    'django.contrib.contenttypes',
    'django.contrib.sessions',
    'django.contrib.messages',
    'django.contrib.staticfiles',
    'catalog.apps.CatalogConfig', 
]
```