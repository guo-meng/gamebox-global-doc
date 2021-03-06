# 调用接口

#### 1、初始化

调用广告SDK任何其他的函数前，都要先调用该函数请求初始化SDK。

函数：

```text
adSDK.initAdSense(options);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| options | 初始化选项 | Object | 非空 |  |

options是一个对象,包含字段如下：

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| userId | 用户id | Number | 非空 | 通过登录接口获取的 |
| gameId | 游戏id | Number | 非空 | 开放平台创建游戏生成的gameId |

#### ~~2、创建文本广告~~

调用该函数后平台会创建一个文本广告。

函数：

```text
adSDK.createTextAd();
```

 该函数会返回一个Promise

#### ~~3、展示文本广告~~

调用该函数后平台会将之前创建的文本广告显示出来。

函数：

```text
adSDK.showTextAd();
```

#### ~~4、隐藏文本广告~~

调用该函数后平台会将之前创建的文本广告隐藏。

函数：

```text
adSDK.hideTextAd();
```

#### ~~5、销毁文本广告~~

调用该函数后平台会将之前创建的文本广告销毁。

函数：

```text
adSDK.destroyTextAd();
```

**建议每次创建展示完文本广告之后都将其销毁，以便回收内存**

#### 6、创建图片广告

调用该函数后平台会创建一个图片广告。

函数：

```text
adSDK.createImageAd();
```

**注意：如果是在游戏刚启动时调用该接口，请增加参数isStartingAd，该参数表示游戏在用户无交互的情况下调用图片广告，格式如下：**

```text
adSDK.createImageAd(isStartingAd);
```

| **参数** | **类型** | **是否为空** |
| :--- | :--- | :--- |
| isStartingAd | Boolean | 可空 |

该函数会返回一个Promise

#### 7、展示图片广告

调用该函数后平台会将之前创建的图片广告显示出来。

函数：

```text
adSDK.showImageAd();
```

#### 8、隐藏图片广告

调用该函数后平台会将之前创建的图片广告隐藏。

函数：

```text
adSDK.hideImageAd();
```

#### 9、销毁图片广告

调用该函数后平台会将之前创建的图片广告销毁。

函数：

```text
adSDK.destroyImageAd();
```

**建议每次创建展示完图片广告之后都将其销毁，以便回收内存**

#### 10、监听广告错误

当拉取广告发生错误时会触发此函数里面的回调函数，cp通过可通过此方法监听广告的错误并作出相应处理

 例如当errorCode为1009时，表示adSense没有广告填充。

函数：

```text
adSDK.onError(callback);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| callback | 设置拉取广告错误时的回调 | Function | 可空 |  |

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| params | callback参数 | Object | 非空 |  |

  
params参数信息

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| type | 错误类型 | String | 非空 |  |
| errorCode | 错误码 | Number | 非空 |  |
| desc | 错误描叙 | String | 非空 |  |

#### 11、监听广告播放完成

当广告完成时会触发此函数里面的回调函数（广告自动关闭）

函数：

```text
adSDK.onComplete(callback);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| callback | 设置广告完成时的回调 | Function | 可空 |  |

#### 12、监听广告点击跳过

当用户点击跳过广告按钮会触发此函数里面的回调函数：

```text
adSDK.onSkipped(callback);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| callback | 设置用户跳过广告时的回调 | Function | 可空 |  |

#### 13、监听用户关闭广告

当用户关闭广告会触发此函数里面的回调函数：

```text
adSDK.onUserClose(callback);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| callback | 设置用户关闭广告时的回调 | Function | 可空 |  |

#### ~~14、创建底部横幅广告~~

调用该函数后平台会创建一个底部横幅广告。

函数：

```text
AdSDK.createCoexistingTextAd();
```

该函数回返回一个Promise，Promise resolve的返回值是一个广告实例 coexistingTextAd

#### ~~15、展示底部横幅广告~~

用返回的广告实例调用该函数后平台会将之前创建的底部横幅广告显示出来。

函数：

```text
coexistingTextAd.showCoexistingTextAd();
```

#### ~~16、隐藏底部横幅广告~~

用返回的广告实例调用该函数后平台会将之前创建的底部横幅广告隐藏。

函数： 

```text
coexistingTextAd.hideCoexistingTextAd();
```

#### ~~17、销毁底部横幅广告~~

用返回的广告实例调用该函数后平台会将之前创建的底部横幅广告销毁。

函数：

```text
coexistingTextAd.destroyCoexistingTextAd();
```

建议每次监听到底部横幅广告关闭后都将其销毁，以便回收内存

#### ~~18、监听底部横幅广告错误~~

当拉取广告发生错误时会触发此函数里面的回调函数，开发者可通过此方法监听广告的错误并作出相应处理，

例如当errorCode为1009时，表示adSense没有广告填充。

函数：

```text
coexistingTextAd.onError(callback);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| callback | 设置拉取广告错误时的回调 | Function | 可空 |  |

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| params | callback参数 | Object | 非空 |  |

params参数信息

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| type | 错误类型 | String | 非空 |  |
| errorCode | 错误码 | Number | 非空 |  |
| desc | 错误描叙 | String | 非空 |  |

#### ~~19、监听底部横幅广告展示完毕~~

当广告完成时会触发此函数里面的回调函数（广告自动关闭）

函数：

```text
coexistingTextAd.onComplete(callback);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| callback | 设置广告完成时的回调 | Function | 可空 |  |

#### ~~20、监听底部横幅广告被主动关闭~~

当用户关闭广告会触发此函数里面的回调函数：

```text
coexistingTextAd.onUserClose(callback);
```

| **参数** | **含义** | **类型** | **是否为空** | **备注** |
| :--- | :--- | :--- | :--- | :--- |
| callback | 设置用户关闭广告时的回调 | Function | 可空 |  |

### 错误码

| 错误码 | 错误说明 |
| :--- | :--- |
| 11 | 请求广告错误 |
| 12 | SDK不是最新的 |
| 1009 | adSense广告没有填充 |
| 301 | 请求广告超时（可能网络慢，可能VPN） |

