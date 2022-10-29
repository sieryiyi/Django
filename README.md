# Django



一般常使用的，setting、urls

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
- 注册APP
    - 在settings配置文件里的INSTALLED_APPS中注册
    - 'app01.apps.App01Config',
