# 宋一凡 · 创意编码作品集（作业三）

> 作业三：成果展示与汇报 · 作品集网站（40%）
> 源码：GitHub **私有仓库** ｜ 网站：**Cloudflare Pages** 公开访问
> 在线地址：部署后形如 `https://<你的站点名>.pages.dev`

**作者：宋一凡** ｜ GitHub：[@songyifan](https://github.com/songyifan)

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
- 教师已被添加为本仓库 Collaborator（只读查看源码）

## 部署到 Cloudflare Pages（六步）

1. 在 GitHub 新建仓库（本作业要求 **Private 私有**），名字建议 `ip-03-portfolio`，不要勾选自动初始化
2. 推送本目录：

   ```bash
   git init
   git add .
   git commit -m "作业三: 作品集网站（三个作品 + 关于我）"
   git branch -M main
   git remote add origin https://github.com/songyifan/ip-03-portfolio.git
   git push -u origin main
   ```

3. 登录 [dash.cloudflare.com](https://dash.cloudflare.com) → 左侧 **Workers & Pages** → **Create** → **Pages** 标签
4. 选择 **Connect to Git** → 授权 GitHub → 选中 `ip-03-portfolio` 仓库 → Begin setup
5. 构建设置全部留空即可：Framework preset 选 `None`，Build command 留空，**Build output directory 填 `/`** → Save and Deploy
6. 约 1 分钟后获得 `https://ip-03-portfolio.pages.dev` 公开网址 —— 源码仍是私有的，网址任何人可看，这就是"私的是仓库，不是网站"

> 注意：作品二顶栏的「GitHub Pages 版」链接指向作业一仓库，需要该仓库 Pages 已开启才可访问；内嵌区域用的是本站副本，不受影响。

## 邀请老师查看源码（私有仓库必做，否则"代码规范"项没有分）

1. 打开私有仓库 → **Settings → Collaborators → Add people**
2. 输入老师的 GitHub 用户名 → 选择权限 **Read**（个人仓库若只提供 Write 选项，直接邀请即可，老师可只读查看代码，不会改动）
3. 老师在邮箱或 GitHub 通知里接受邀请后，即可查看私有源码
4. 提交时在作业说明里附上仓库地址 + 已邀请截图

## 本地运行

直接双击 `index.html` 即可（相对链接正常）。作品二、三需联网加载 p5.js / Three.js 的 CDN；作品一零依赖，离线也能玩。

> 如果是在编辑器/预览面板里打开单文件，点击作品可能显示「暂无数据」——那是预览器的限制，不是网站坏了。请用浏览器打开，或在目录下执行 `python -m http.server 8801` 后访问 `http://127.0.0.1:8801/`。
