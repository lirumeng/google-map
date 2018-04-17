# google-map
学习一点Google Map API

### 启用Google Maps Embed API
> [Google API Console](https://console.developers.google.com/apis/library)

找到 Google Maps Embed API，启用就可以了。

### 建立凭证
进入`凭证`，选择API密钥。API密钥是一段很长的代码，这段代码可以让Google识别是哪个使用者在对应的服务，并且根据使用者权限和使用服务，提供对应的功能和限制。


### 地图模式
[文档](https://developers.google.com/maps/documentation/embed/guide)
- place 地点模式

使用place，就可以定义一个位置或者地址，使用place时，后面会用`q`参数定义要在地图上着重展示的地点，如果遇到空格，可用 `+` 号表示。 


- directions 路线规划模式

> - origin 路线起点（必须）。 该值可以是地点名称、地址或地点 ID（地点 ID 应带有 place_id: 前缀）。
> - destination 路线终点（必须）
> - waypoints 指定起点与目的地之间的路线途经的一个或多个中途地点。可以通过使用管道字符 (|) 分隔地点来指定多个路径点
> - mode 定义出行方式。包含driving、walking、bicycling、transit和flying
> - avoid 指示 Google 地图避开 tolls、ferries 和/或 highways。可使用 | 分隔开
> - units 单位，包含metric或imperial。如果未指定，则由查询的 origin 国家决定使用什么单位。

- search 搜索模式
> - q 搜索的关键词（必须）
> - zoom 地图的缩放大小，范围从0到21
> - center 中心点经纬度

- view 返回不带标记或路线的地图
> - center 定义地图视图的中心
> - zoom 设置地图的初始缩放比例。可接受的值范围是 0（全世界）至 21（个别建筑）
> - maptype 可以是 roadmap（默认值）或 satellite，定义要加载的地图图块类型
> - language 定义 UI 元素和地图图块上显示的标签所使用的语言。
> - region 根据地缘政治敏感性定义要显示的相应边界和标签。

- streetview 街景模式
每张街景全景图均提供以单个位置为中心的 360 度全视图。 图像包含 360 度水平视图（全包围）和 180 度垂直视图（从直上至直下）。 streetview 模式提供了一个查看器，通过中心位置的摄像头将生成的全景图渲染为一个球面。
> - location 接受逗号分隔值形式的纬度和经度 (46.414382,10.013988)。（必须）
> - pano 具体的全景图 ID。如果没有location，一定要有这个参数。（必须）
> - heading 以与北方所呈的顺时针角度指示摄像头的罗盘航向。 接受的值范围是 -180° 至 360°。
> - pitch 指定摄像头的向上或向下角度。 pitch 的指定度数范围是 -90° 至 90°。 正值将使摄像头呈向上角度，而负值将使摄像头呈向下角度。 默认间距 0° 的设置取决于摄像头在拍摄图像时的位置。
> - fov 决定图像的水平视野。 视野以度数表示，范围是 10° - 100°。 其默认值为 90°。数字越小，表示缩放比例越大。
> - language 定义 UI 元素和标签所使用的语言。
> - region 根据地缘政治敏感性定义要显示的相应边界和标签。