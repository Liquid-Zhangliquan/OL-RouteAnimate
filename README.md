# 基于openlayer的小车运动轨迹动画
## 实现思路
v1利用原生requestAnimationFrame函数，利用ol自带的getCoordinateAt获取每个step的坐标，然后更新小车当前位置，并且push轨迹路线
v2利用turf的LineSliceAlong对轨迹进行增密，然后利用requestAnimationFrame绘制每一帧动画
## 存在问题
* ~~插值和节点没有做处理，使得拐点轨迹不好看~~
* 小车车头方向未做调整
## mapbox实现轨迹
大家参照朋友利用mapbox和turf的LineSliceAlong对轨迹进行增密
* [掘金地址](https://juejin.im/post/5cfc98e351882515ba0eefe1)
* [github地址](https://github.com/tpolong/route)
## maptalks实现轨迹
maptalks是我接触最早的一个开源二三维地图api
line直接提供[animateShow](http://maptalks.org/maptalks.js/api/0.x/LineString.html#animateShow)这个方法
* maptalks将line.animateShow()返回的对象作为player，所以可以直接执行pause,play等方法控制播放
* 小车经过摄像头时改变摄像头状态（计算小车到摄像头的距离，小于某个值，激活摄像头)
## 体验地址
* [openlayer-v1版本](https://liquid-zhangliquan.github.io/OL-RouteAnimate/openlayer/openlayer_route.html)
* [openlayer-v2版本](https://liquid-zhangliquan.github.io/OL-RouteAnimate/openlayer/openlayer_routeV2.html)
* [mapbox版本](https://liquid-zhangliquan.github.io/OL-RouteAnimate/mapbox/mapbox_route.html)
* [maptalks版本](https://liquid-zhangliquan.github.io/OL-RouteAnimate/maptalks/maptalks_route.html)