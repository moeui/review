本文简要介绍如何在一台电脑上配置多个github账号，以此满足多账号用户需求，如同时支持个人账号以及公司账号。

这里介绍通过SSH方式来连接远程仓库的方式。

## 创建新的SSH key
  ssh-keygen -t rsa -C "your-email-address"

默认的 key 保存路径为 ~/.ssh/id_rsa，这里我们最好重新命名，因为我们是为第二个github账号生成key, 所以最好不要覆盖默认的key. 我们可以命名为 ~/.ssh/id_rsa_second。

将生成的 key 和 github账号绑定
登录github账号并在设置中新增 ssh 配置，并将 ~/.ssh/id_rsa_second.pub文件的内容拷贝过来。

## 拷贝命令： 
  pbcopy < ~/.ssh/id_rsa_second.pub

## 创建多账号配置文件

  touch ~/.ssh/config
  vim config

## config文件的内容如下：

  #Default GitHub
  Host github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa

## 这只默认账号的设置，接下来我们新增另外一个账号的配置

  Host me.github.com
    HostName github.com
    User git
    IdentityFile ~/.ssh/id_rsa_second


## 如何使用

  git remote add origin git@me.git@github.com:moeui/review.git
  git push origin master

注意这里要使用 ssh 地址形式而不是 https 的形式。