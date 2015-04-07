# MKMapView-Extension
这是关于 MKMapView 写的一个基于swift的扩展，可以扩展 MKMapView 的相关功能，减少复用代码量。

##更新说明
2015.04.07 增加了“ZoomLevel”（缩放等级）的获取和设置

##ZoomLevel

###func getZoomLevel() -> Double
这个函数主要是用来获取 MKMapView 的当前缩放级别，缩放级别从1级到17级，缩放级别与海拔高度的对应表如下表所示(近似值)：

| 缩放级别 | 海拔高度 | 对应的显示范围 |
| :----: | :-----: | :----------: |
| 17     |   500m  |    街道级别   |
| 16     |   1km   |    街道级别     |
| 15     |   2km   |    区级别     |
| 14     |   5km   |    区级别     |
| 13     |   10km  |    市级别     |
| 12     |   20km   |    市级别     |
| 11     |   40km   |    州级别     |
| 10     |   80km   |    州级别     |
| 9      |   160km   |    省级别     |
| 8      |   320km   |    省级别     |
| 7      |   640km   |    省级别     |
| 6      |   1280km   |    省级别     |
| 5      |   2560km   |    国级别     |
| 4      |   5120km   |    国级别     |
| 3      |   10240km   |    国级别     |
| 2      |   20480km   |    洲级别     |
| 1      |   40960km   |    全球级别     |

上表的显示范围并未严格定义，只是凭鄙人的视觉效果所判断的，如果大家有更好的建议，欢迎提出！

###func setCenterCoordinate(center: CLLocationCoordinate2D, zoomLevel: UInt, animated: Bool)

这个函数主要是用来以缩放级别来设置当前地图中心点

###func zoomIn() -> Bool

这个函数用来将缩放级别放大一级，返回一个布尔值标明是否放大成功

###func zoomOut() -> Bool

这个函数用来将缩放级别缩小一级，返回一个布尔值标明是否缩小成功