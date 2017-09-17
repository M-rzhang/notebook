# ububtu配置github环境(已有github账号)

* 安装 Git : sudo apt-get install git

* 生成 ssh key : ssh-keygen -t rsa -C your_email@youremail.com

* 网页登录到你的 github ，右上角点击头像 -> Settings，左边选择 SSH and GPG Keys，点击 New SSH SSH Key ,title 随便填，进入你的主目录下的 .ssh 目录下，cat id_rsa.pub 复制从ssh-rsa 开始的字符串，将其粘贴到key表单框。

* 测试 ssh key 是否成功，使用命令 “ssh -T git@github.com”，如果出现 You’ve successfully authenticated, but GitHub does not provide shell access 。这就表示已成功连上 github。

* 配置 Git 的配置文件，username 和 email

  * git config --global user.name "your name" // 配置用户名

  * git config --global user.email "your email" // 配置 email

* 建立项目

  * mkdir nodebook and cd nodebook

  * echo "# notebook" >> README.md

  * git init

  * git add README.md

  * git commit -m "first commit"

  * git remote add origin https://github.com/M-rzhang/notebook.git

  * git push -u origin master 输入用户名密码即可创建项目

* 免密码提交

  * git remote rm origin

  * git remote add origin git@github.com:M-rzhang/notebook.git

  * git push -u origin master
