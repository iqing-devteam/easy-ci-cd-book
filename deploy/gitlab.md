# 安装GitLab

## 版本

使用GitLab有两种模式，一种是类似GitHub的托管模式，另一种是自己安装。

为了速度快自然是选择自己安装，然后GitLab推出了三个版本，两个商业收费版本一个社区(CE)版本，
因为社区版够用外加比较抠就用社区版。

GitLab CE也提供了一系列安装方式，比如一键整合包，Docker容器，独立安装GitLab本体等等。

#### 使用一键整合包安装

推荐使用一台内存不小于4G以及大于50G硬盘的独立VPS，来安装Gitlab CE一键整合包。

一键整合包会自动安装Gitlab CE本体以及配置和启动Mysql和Redis等依赖。

安装完毕后就可以看到Gitlab的界面了，非常方便。

下面是Gitlab CE的清华镜像源安装方法
https://mirror.tuna.tsinghua.edu.cn/help/gitlab-ce/

安装完毕后配置和启动GitLab

```bash
# https://about.gitlab.com/installation/#ubuntu
sudo gitlab-ctl reconfigure
```

#### Docker容器安装GitLab，不推荐

用Docker启动过Mysql的同学应该也有所体会，Docker在持久化上并不是太好使（有传闻即使设置了磁盘映射也可能会丢文件）。

GitLab需要在把代码仓库持久化储存在本地磁盘上，也有这样的问题。

如果你不希望仓库突然就消失了的话，不推荐。

PS1. 给开发和测试环境用的MySQL用Docker还是可以的，但是在生产环境下确实让人不放心。

PS2. 想在自己开发机上尝鲜的话，GitLab with Docker也是可以的，但是还是不如直接在虚拟机内安装一键整合包。

#### 独立安装GitLab本体，不推荐

这种方式需要自行搭建所有的环境。

由于GitLab是使用Ruby on Rails实现，Ruby的环境配置方法大多数人不熟。环境不仅仅是数据库，还有更多Ruby社区常用的依赖都需要配置。

所以不推荐。
