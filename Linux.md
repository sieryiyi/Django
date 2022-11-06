# Linux 

### ssh命令

ssh 最常用的功能是登录远程主机，选择以什么用户连接哪台机器，然后输入密码即可

### Linux常用命令

- cd：进入目录
  - cd ..：表示进入上一级目录 
  - cd -：回到上一次的目录
  - cd ~：回到根目录
- ls：显示文件下的内容
  - ls-a：显示所有文件，包括以.为开头的隐藏文件
  - ls-l：显示详细信息
  - ls-h：信息的人性化显示（？）
  - 后面这些后缀可以加多个，比如ls-lh
  - ls /：代表查看根目录

- pwd：当前所在目录（print working directory）
- whoami：列出当前用户
- hostname：主机名
- mkdir：创建文件夹
    - mkdir {文件名1,文件名2}：一次创建多个文件夹
    - mkdir -p /目录1/目录2/目录3：递归创建文件夹，可以在没有目录2的情况下，自动创建目录2后，再去创建目录3
    - mkdir 文件夹名字1{1..100}：一次创建100个文件夹
- cat：一次显示整个文件
- logout：退出当前系统用户 
- date：查看当前时间


### Linux小知识

- Linux目录的分隔符是正斜杠/（Windows是反斜杠\）

### Linux绝对路径、相对命令

### touch命令

- 创建普通文件：touch mjj.txt
- 修改文件时间

### copy命令

- 复制普通命令：cp mjj.txt new_mjj.tex
- 复制普通文件，且改名放到其他文件夹：cp mjj.tt ./mysite/mjj2.txt 
- 复制文件夹：cp -r  文件夹名字1 新的名字2（递归方式）
- 不改变文件属性：cp -p
- 复制且保持软连接（快捷方式）：cp -d 
- 如果文件2已经存在，询问是否覆盖：cp -i


### mv命令

- 移动：mv ./mjj.txt（原路径）    新路径
- 重命名：mv mjj.tex new_mjj.txt

### rm命令

- 删除文件夹：rm -r
- rm -d：删除空目录

### Linux帮助命令

- man 命令
- 命令 --help

### Linux开关机

- shutdown -r ：重启
- shutdown -h ：关机

### 常用快捷键

- ctrl+c：取消当前操作
- ctrl+l：清屏
- ctrl+d：退出当前用户
- ctrl+a：光标移到行首
- ctrl+e：光标移到行位
- ctrl+u：删除光标到行首的内容

### echo命令

- 打印这个字符串：echo 字符串
- 查看Linux环境变量：echo $PATH

### vim 命令
