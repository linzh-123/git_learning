## 一、git config配置
```
git config --global user.name "your_name"
git config --global user.email you_email
```
## 二、配置ssh连接

1.主机使用`ssh-keygen` 命令，创建公钥和私钥，把公钥文件id_dsa.pub的内容拷贝到服务器的SSH的公钥列表中。其中，如果代码是托管在github，需要在setting里面添加ssh公钥，如果代码是存在于Linux服务器上，则需要在.ssh/authorized_key文件末尾添加公钥信息

2、可以用命令判断是否配置SSH成功：`ssh -T user@ip`

3、使用ssh-agent配置，ssh连接不用输入密码
```
ssh-agent bash
eval 'ssh-agent'
ssh-add your_id_rsa_file

```

## 三、clone仓库

1、当ssh服务以及服务器端的project配置完毕之后，可以直接把仓库clone下来使用
```
git clone user@serverip:path/projectname.git
```
