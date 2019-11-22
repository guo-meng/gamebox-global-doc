---
description: 下载对应种类SDK压缩包，解压文件，获取AdSDK.js文件。
---

# 导入资源

## 小游戏

游戏客户端将[**AdSDK.js**](../../../zi-yuan-xia-zai/sdk-xia-zai.md#xiao-you-xi-sdk20190402)放入assets/script目录下即可。

## H5游戏

#### 方法一：

1. 下载广告接入SDK文件[**AdSDK.js**](../../../zi-yuan-xia-zai/sdk-xia-zai.md#h-5-you-xi-sdk20190402)。
2. 游戏客户端需要在游戏中引用AdSDK.js文件。

   如：假如游戏客户端的启动文件为index.html，则在index.html中的开始位置加入：

```text
<script type = "text/javascript" src="./AdSDK.js" ></script>
```

#### 方法二：

直接引用线上JS文件，地址为：[https://cdn.gamebox.cocos.com/res/adSDK.sea.min.js](https://cdn.gamebox.cocos.com/res/adSDK.sea.min.js)



