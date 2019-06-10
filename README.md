# lottie

> Lottie project of Vue

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report
```
## Link 文件库
https://www.lottiefiles.com/

## 安装

```
# NPM
npm install lottie-web
```


## 使用

> 调用 lottie.loadAnimation()方法启动动画


```
var animation = bodymovin.loadAnimation({
  container: document.getElementById('lottie'), // Required
  path: 'data.json', // Required
  renderer: 'svg/canvas/html', // Required
  loop: true, // Optional
  autoplay: true, // Optional
  name: "Hello World", // Name for future reference. Optional.
})
```

```
container：动画容器，dom 元素
path：从 AE 中导出的 json 文件
renderer：动画格式
loop：是否循环播放动画
autoplay： 是否自动播放动画
name：动画名称
```
### 动画实例的主要方法

anim.play() — 播放动画。

anim.stop() — 停止动画。

anim.pause() — 暂停动画。

anim.setSpeed(speed) — 设置播放速度，参数 speed 为 Number ，1为正常速度。

anim.goToAndStop(value, isFrame) — 跳到某一帧并暂停播放。第一个参数是 Number 。第二个参数是 Boolean，设置true则表明第一个参数代表的是帧数，false代表第一个参数为时间值（单位毫秒），默认 false。

anim.goToAndPlay(value, isFrame) — 跳到某一帧并播放。同上。

anim.setDirection(direction) — 设置播放方向。1 为正着播，-1反着播。

anim.playSegments(segments, forceFlag) — 播放某一片段。第一个参数为一维数组或多维数组，每个数组包含两个值（开始帧，结束帧），第二个参数是一个 Boolean ，决定是否立即强制播放该片段。

anima.destroy() — 注销动画。

### lottie 的主要方法

lottie.play(<name>) — 播放所有动画，name为动画名称，播放该动画。

lottie.stop(<name>) — 停止所以动画，name为动画名称，停止该动画。

lottie.setSpeed(speed, <name>) — 设置动画播放速度，speed指定速度，1为正常值，name为动画名称，只设定该动画的速度。

lottie.setDirection(direction, <name>) — 设置动画播放方向，direction指定方向，1为正向，-1为反向，name为动画名称，只设定该动画。

lottie.loadAnimation(obj) — 加载动画

lottie.destroy() — 注销动画释放资源，同时清空 dom 节点。

lottie.registerAnimation() — 可以给一个节点直接注册一个动画，该节点必须包含有指向 json 文件的data-animation-path属性。

lottie.setQuality() — 设置播放质量，默认 high，可以设置为 high、medium、low 或者一个大于 1 的数值。在有些动画中，数值低于 2 时不会有区别。

### 事件监听

complete — 动画播放结束时触发（循环播放不会触发）

loopComplete — 进入下一个循环时触发

enterFrame — 每进入一帧触发一次

segmentStart — 进入片段播放时触发

config_ready — 初始化配置完成时触发

data_ready — 动画所有部分加载完成时触发

DOMLoaded — dom 元素加载完成时触发

destroy — 注销动画时触发


```
// 例如：
anim.addEventListener('complete', function () {
    console.log('complete');
});
```
