# 总结

本文通过实际操作的演示了从代码编写到CI检查与合并，最后在云端部署的过程。

第一次本书的同学可以回顾一下总体的[流程](flow.md)，那么会有新的体验和自己去构建CI流程的想法。

现在留下了一个缺憾，就是还没有演示怎么把项目本体也跑在阿里云容器服务的过程。这个稍后更新。

不过认真读过本书的同学应该已经明白了。
在容器云运行项目，也是创建容器仓库，绑定gitlab分支，构建之后通过编排模板把项目跑起。这个过程和之前写过的托管Runner到阿里云容器服务是一样的。