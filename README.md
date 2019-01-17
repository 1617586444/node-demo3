hello nodejs

  使用ssh方式 连接远程仓库

 1.生成本地电脑的 公钥和私钥
    ssh=keygen - t rsa -C "xxx@xx.com"
 1.1 将般地生成的公钥给写到远程的平台上(github)

2.将本地仓库与远程仓库建立py关系

    git remote add origgin xxx