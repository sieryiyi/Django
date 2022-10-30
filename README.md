# Django


一般常使用的，setting、urls

### 创建Django项目

- django-admin.exe startproject djgo1test
- "E:\pythonproject\pythonProject
\venv\Scripts\django-admin.exe" startproject djgo1test

### APP 概念

- 每一个大项目里有很多分类的小功能
- 即：拆分成不同的app
- 每个APP里可以有各自独立的函数、数据库表结构、HTML模板、CSS等

ps：简单的开发用不到多APP，一般情况，一个项目下创建一个APP即可

### APP 创建

- cd djgo1test  进入目录
- python manage.py startapp app01

经常会操作的：view、model

### 简单功能实现

- 创建APP
- 注册APP【setting.py】
    - 在settings配置文件里的INSTALLED_APPS中注册
    - 'app01.apps.App01Config',
- 编写url和视图函数的对应关系【urls.py】
- 编写视图函数【view.py】
- 启动Django：python manage.py runserver


### 静态文件

- 开发过程中，一般将图片、CSS、js等称之为静态文件
- 1、创建在APP目录下创建static文件夹

### 模板语法

- 本质上：在HTML中写一些占位符，由数据对这些占位符进行替换和处理
