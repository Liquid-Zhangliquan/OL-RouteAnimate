# 基于openlayer的小车运动轨迹动画
## 实现思路
利用原生requestAnimationFrame函数，获取每个step的坐标，然后更新小车当前位置，并且push轨迹路线
## 存在问题
* 插值和节点没有做处理，使得拐点轨迹不好看
* 小车车头方向未做调整
## mapbox实现轨迹
大家参照朋友利用mapbox和turf的LineSliceAlong对轨迹进行增密
[掘金地址](https://juejin.im/post/5cfc98e351882515ba0eefe1)
[github地址](https://github.com/tpolong/route)
## 体验地址
* [openlayer版本](https://liquid-zhangliquan.github.io/OL-RouteAnimate/)
* [mapbox版本](https://liquid-zhangliquan.github.io/OL-RouteAnimate/mapbox_route.html)