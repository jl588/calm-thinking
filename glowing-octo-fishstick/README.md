# Glass Pretzel · 玻璃扭结 —— 参数化互动版

基于 Shadertoy 作者 **Jaenam** 的作品 [Glass Pretzel](https://www.shadertoy.com/view/fcVXDd) 做的本地参数化复刻与互动扩展：单文件、零依赖、双击即用。

## 运行

- 直接双击 `index.html`（需支持 WebGL2 的浏览器：Chrome / Edge / Firefox / Safari）
- 或 `python3 -m http.server 8000` 后访问 http://localhost:8000

## 功能

- **26 个参数滑块**，分六组：动画 / 形状 / 光效 / 颜色 / 互动 / 显示
- **预设一键切换**：🎨 我的定稿（蓝流光）/ 🧊 原版（Shadertoy 初始效果）
- **鼠标互动**：在环上快速划动 → 辉光增强、边缘起涟漪、流光加速、颜色由蓝转橙；静止或移开后约两秒缓缓冷却回蓝（快起慢衰包络，触碰判定用 GPU 掩码回读实现）
- **参数链接分享**：地址栏 `#p=…` 自动同步全部参数，收藏/转发链接即可还原画面；支持 📥 导入与 🎲 随机
- **导航**：拖拽旋转 · 滚轮缩放 · 空格 暂停 · H 收起面板 · R 重置
- **📷 PNG 快照**：一键导出当前画面
- **渲染精度滑块**：0.4–1.0×，视网膜屏性能救星

## versions/

迭代过程留档：`鼠标互动版` → `性能优化版` → `接缝柔化版` → `蓝流光预设版`。
`index.html` 为当前选用版本。

## 许可

原 shader 出自 Jaenam（CC BY-NC-SA 4.0）。本项目整体沿用
[CC BY-NC-SA 4.0](https://creativecommons.org/licenses/by-nc-sa/4.0/deed.zh)：
**署名原作者 · 非商业性使用 · 相同方式共享**。
