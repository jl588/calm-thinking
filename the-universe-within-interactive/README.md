# The Universe Within — Interactive Remix

基于 [Martijn Steinrucken (BigWings)](https://www.shadertoy.com/user/BigWings) 的 Shadertoy 作品
[《The Universe Within》](https://www.shadertoy.com/view/lscczl) 的交互式 WebGL2 再创作。

原作是纯 GPU 神经脉络网络效果;本项目的最终版本在其基础上加入了:

- **粒子化渲染** — 12 万 GPU 粒子沿原网络线段分布(`gl_VertexID` 无状态粒子系统)
- **鼠标力场** — 斥力 + 涡旋,粒子随鼠标流动避让
- **点击聚形** — 点击线条,附近线段聚成随机形象;1×1 拾取着色器精确命中
- **情绪系统** — 聊天框输入情绪词(开心/兴奋/平静/悲伤/愤怒/恐惧/爱),粒子变色、变亮、旋转并聚成对应形态(星形/花瓣/多边形/谐波/心形/涟漪),每次随机生成
- **冥想 BGM + 音频律动** — WebAudio FFT 分解低/中/高频,实时驱动涟漪扩散速度、波纹起伏、切向水流与波前亮度;支持内置合成冥想音或拖入本地音频
- **实时参数面板** — 粒子化比例、粒子大小、鼠标斥力、动画速度等 13 项滑杆,localStorage 记忆

## 文件

| 文件 | 说明 |
| --- | --- |
| `universe-within.html` | 最终交互版(单文件零依赖,双击即用) |
| `universe-original.html` | 原版复刻(未修改,用于对照) |
| `universe_within.frag` | 原版 GLSL 着色器源码存档 |

## 运行

无任何外部依赖,直接用浏览器打开 HTML 文件即可(需要支持 WebGL2 的浏览器)。

## 交互速查

| 操作 | 效果 |
| --- | --- |
| 拖动鼠标 | 3D 视差(原版)/ 粒子避让涡旋(最终版) |
| 点击线条 | 线段聚成随机形象,挪开恢复 |
| 聊天框输入情绪词 | 变色 / 变亮暗 / 旋转 / 聚成对应抽象形态 |
| 空格 · R · F · H | 暂停 · 重置 · 全屏 · 参数面板 |

## 许可

原始着色器 © Martijn Steinrucken (BigWings),以
[CC BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/) 授权。
本项目(修改版)同样以 CC BY-NC-SA 3.0 分享:署名原作、非商业使用、相同方式共享。
