# google-map
学习一点Google Map API

### 启用Google Maps Embed API
> [Google API Console](https://console.developers.google.com/apis/library)

找到 Google Maps Embed API，启用就可以了。

### 建立凭证
进入`凭证`，选择API密钥。API密钥是一段很长的代码，这段代码可以让Google识别是哪个使用者在对应的服务，并且根据使用者权限和使用服务，提供对应的功能和限制。


### 地图模式
- place 地点模式

使用place，就可以定义一个位置或者地址，使用place时，后面会用`q`参数定义要在地图上着重展示的地点，如果遇到空格，可用 `+` 号表示。 


- directions 路线规划模式

> - origin 路线起点（必须）
> - destination 路线终点（必须）
> - waypoints 路线中间点，可使用 | 符号分隔
> - mode 旅行方式，包含driving、walking、bicycling、transit和flying
> - avoid 避开一些特殊线，包含tolls、ferries和highways，可使用 | 分隔开
> - units 单位，包含metric或imperial