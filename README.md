# hello_github

github在windows和linux上的使用方式

## 1.Windows

1）首先下载Github Desktop

2）选择自己想要放在本地的库，选择Open in Desktop，选择一个文件路径

3）之后可以对该文件夹下文件进行修改或者添加文件

4）更改完毕后，打开Github Desktop，会自动提醒所修改的文件，然后点击Commit to master +push origion完毕

## 2.linux

1）安装git

```
sudo apt-get install git
```

2)配置git文件

```
git config --global user.name "your name" //配置用户名

git config --global user.email "your email" //配置email
```

3）生成ssh key

```
ssh-keygen -t rsa -C "your_email@youremail.com"
```

然后可以看到有提示id_rsa.pub的地址，打开该文件复制里面的内容

4）在github上添加ssh key

在个人设置页面（personal settings），点击SSH and GPG Keys，添加一个ssh key，title名字随便填，key文本框里就复制步骤3中id_rsa.pub里面的所有内容

5）验证是否设置成功

```
ssh -T git@github.com
```



6）克隆项目

```
cd 文件夹
git clone “库的链接”
```

7）上传修改

```
git add newfile
git commit -m "add new file test"
git push origin master
```

