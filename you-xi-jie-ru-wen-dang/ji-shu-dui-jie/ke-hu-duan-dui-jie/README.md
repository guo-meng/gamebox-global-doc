# 客户端接入

## 非对战游戏接口调用时序图如下： ![](https://github.com/guo-meng/gamebox-global-doc/tree/1d64fde0089a5a5c69bfbb96788c7d7c66ce64ef/.gitbook/assets/tu-pian-17.png)

说明：

1. 游戏客户端调用平台客户端init命令进行SDK初始化
2. 游戏客户端通过onInit回调接口获得init函数的返回的用户信息结果
3. 游戏客户端调用平台客户端quit命令，结束游戏

