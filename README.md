# 宋一凡 · 创意编码作品集（作业三）

> 作业三：成果展示与汇报 · 作品集网站（40%）
> 源码：GitHub 仓库 [syf08241654/ip-03-portfolio](https://github.com/syf08241654/ip-03-portfolio) ｜ 网站：GitHub Pages 公开访问
> **在线地址：https://syf08241654.github.io/ip-03-portfolio/**

**作者：宋一凡** ｜ GitHub：[@syf08241654](https://github.com/syf08241654)

## 网站结构

```
index.html              首页：名字 + 一句话方向介绍 + 三个作品入口 + 关于我
works/neon-drift.html   作品一《霓虹穿梭 · Neon Drift》  Canvas 街机（本仓库内直接运行）
works/dynamic.html      作品二《引力花园》               包装页：顶栏 + iframe 内嵌
works/p5-dynamic.html   作品二本体（p5.js 交互，作业一作品的副本，随本站部署）
works/three-game.html   作品三《星屑猎手》               Three.js 小游戏（本仓库内直接运行）
```

- 任意作品从首页 **1 次点击** 即可到达，作品页顶栏可一键返回
- 作品二以 **iframe 内嵌**形式展示，iframe 指向本站副本 `p5-dynamic.html`，不依赖作业一 Pages 是否已部署；顶栏另附作业一 GitHub Pages 地址
- 三个作品均自包含，部署后可直接玩（作品一完全零依赖，离线也能玩）

## 三个作品

| # | 作品 | 类型 | 技术 |
|---|---|---|---|
| 1 | 《霓虹穿梭 · Neon Drift》 | Canvas 街机小游戏 | 原生 Canvas 2D · WebAudio 合成音效 · 连击/护盾/分区难度系统 |
| 2 | 《引力花园》 | p5.js 交互动态 | p5.js 1.9.4 · deltaTime 物理步进 · WebAudio 音效 · 4 种交互 |
| 3 | 《星屑猎手》 | Three.js 小游戏 | Three.js r128 · 第三人称跟随相机 · Raycaster 触屏操控 |

## 版权与规范

- 三个作品的**代码、玩法设计、页面视觉均为本人原创**，© 2026 宋一凡，保留所有权利
- 第三方库通过 CDN 引入，版权归各自作者：
  - p5.js 1.9.4（jsDelivr CDN）
  - Three.js r128（jsDelivr CDN，MIT License）
- 网站与作品**未使用任何第三方图片、字体素材**；所有视觉均由代码实时绘制
- 仓库为公开仓库，老师与任何人可直接查看源码

## 部署（GitHub Pages，已完成）

1. 仓库已推送至 `https://github.com/syf08241654/ip-03-portfolio`（main 分支）
2. **Settings → Pages** → Source 选 `Deploy from a branch`，Branch `main` / `(root)`，Save
3. 约 1 分钟构建完成，访问 **https://syf08241654.github.io/ip-03-portfolio/**
   - 索引页：`.../ip-03-portfolio/`
   - 作品一《霓虹穿梭》：`.../ip-03-portfolio/works/neon-drift.html`
   - 作品二《引力花园》：`.../ip-03-portfolio/works/dynamic.html`
   - 作品三《星屑猎手》：`.../ip-03-portfolio/works/three-game.html`
4. 之后每次 `git push` 到 main，Pages 会自动重新构建

> 备选：若后续希望仓库保持私有、网站仍公开，可使用 Cloudflare Pages（GitHub 免费版不支持私有仓库开启 Pages）。步骤：dash.cloudflare.com → Workers & Pages → Create → Pages → Connect to Git → 选仓库 → Framework 选 None、Build output directory 填 `/` → Deploy。

> 注意：作品二顶栏的「GitHub Pages 版」链接指向作业一仓库，需要该仓库 Pages 已开启才可访问；内嵌区域用的是本站副本，不受影响。

## 作业一源码（可选，作为素材出处）

作业一的《暖阳 · 群山》《引力花园》单独放在公开仓库 `syf08241654/ip-01-p5-works`，线上地址 https://syf08241654.github.io/ip-01-p5-works/ 。本站作品二的 iframe 内嵌的是本地副本 `works/p5-dynamic.html`，不依赖该仓库是否在线。

## 本地运行

直接双击 `index.html` 即可（相对链接正常）。作品二、三需联网加载 p5.js / Three.js 的 CDN；作品一零依赖，离线也能玩。

> 如果是在编辑器/预览面板里打开单文件，点击作品可能显示「暂无数据」——那是预览器的限制，不是网站坏了。请用浏览器打开，或在目录下执行 `python -m http.server 8801` 后访问 `http://127.0.0.1:8801/`。
