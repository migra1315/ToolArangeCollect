# git和Github

## git

### 安装git

```
sudo apt-get install git
```

### 新建本地仓库

```
# 进入本地仓库文件夹
git init
# 在文件夹下生成.git文件

#配置git，来区分不同的用户
git config --global user.name “migra1315”
git config --global user.email “1791575694@qq.com”
```

### 新建云端仓库

```
# 在github.com New repository
# 云端仓库名称与本地相同
```

### 通过ssh方式建立连接

```
ssh-keygen -C ‘1791575694@qq.com’ -t rsa
#  在./root 下生成.ssh文件夹，存储公钥id_rsa.pub和私钥id_rsa
# 在github上，Setting中，设置公钥id_rsa.pub
# 使用ssh的原因是，http连接每次都需要密码验证
```

### 建立连接

```
# 进入本地仓库文件夹

# 与云端库建立连接，该连接的名称为 origin
git remote add origin git@github.com:migra1315/ToolArangeCollect.git

#文件夹中文件归入本地仓库管理
git add test.py
#填写必要解释
git commit -m "必要注释"

#上传到origin连接的master分支
git push origin master
```

