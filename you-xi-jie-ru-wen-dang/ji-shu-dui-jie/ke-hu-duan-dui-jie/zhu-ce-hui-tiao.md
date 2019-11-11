---
description: 该目录下回调函数需要在GameSDK.init()函数调用前调用。
---

# 注册回调

## 设置游戏暂停回调

平台通知游戏平台生命周期，例：平台进入后台调用onPause通知游戏平台进入后台，当平台进入前台调用onResume通知游戏平台进入前台。

函数：

```text
GameSDK.setOnPauseCB(func)
```

参数说明：

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| func | onPause回调函数 | function | 非空 | 详见onPause函数说明 |

onPause函数说明：

```text
function onPause()
```

## 设置游戏继续回调

平台通知游戏平台生命周期，例：平台进入后台调用onPause通知游戏平台进入后台，当平台进入前台调用onResume通知游戏平台进入前台。

函数：

```text
GameSDK.setOnResumeCB(func)
```

参数说明：

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| func | onResume回调函数 | function | 非空 | 详见onResume函数说明 |

onResume函数说明：

```text
function onResume()
```

