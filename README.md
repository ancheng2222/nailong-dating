# 网恋吗？——抽象奶龙找对象主页

一个抽象风（发癫奶龙）找对象单页，可整个文件夹直接挂到 GitHub Pages。

## 文件结构

```
奶龙找对象网页/
├── index.html                 # 主页（GitHub Pages 的入口文件，必须叫这个名）
├── README.md                  # 本说明
├── 素材备选/                  # 我下载的其他抽象奶龙候选图（不上线，留给你挑）
│   ├── bg_crazy.png           # 双奶龙吐舌发癫版（当前 bg.png 同款）
│   ├── bg_tongue.png          # 吐舌+火焰龙头
│   ├── bg_v.png               # 比 V 手势
│   └── bg_hold.png            # 托腮
└── assets/
    ├── img/
    │   └── bg.png             # 当前背景：双奶龙吐舌发癫版
    └── audio/
        ├── xhs_lieqi.mp3      # 当前背景音乐：小红书"猎奇音效"视频音轨（51 秒循环）
        └── xhs_lieqi.mp4      # 音轨来源视频（已转成 mp3，可删除，不影响页面）
```

## 部署到 GitHub Pages（3 种方式任选）

### 方式一：网页版上传（最简单，不用装任何东西）

1. 打开 https://github.com/new ，创建一个新仓库，名字随意（比如 `nailong-dating`），
   记得选 **Public**（Pages 免费托管需要公开仓库）。
2. 创建后进入仓库 → 点 **Add file → Upload files**，把 `index.html`、
   `README.md` 和整个 `assets` 文件夹一起拖进去，然后 Commit。
3. 仓库页点 **Settings → Pages**，左侧菜单选 Pages；在 "Build and deployment" 里
   Source 选 **Deploy from a branch**，Branch 选 `main`，目录选 `/ (root)`，点 Save。
4. 等 1~2 分钟，页面顶部会出现你的链接，形如：
   `https://你的用户名.github.io/nailong-dating/`
   把链接发给小宝就行。

### 方式二：命令行 git 推送（会 git 的话更快）

```bash
cd D:\software\奶龙找对象网页
git init
git add .
git commit -m "抽象奶龙找对象主页 v1"
git branch -M main
git remote add origin https://github.com/你的用户名/nailong-dating.git
git push -u origin main
```

然后同样去仓库 **Settings → Pages** 开启分支部署（同上第 3 步）。

### 方式三：用 GitHub Desktop

1. 打开 GitHub Desktop → File → New repository，选好本地目录（`D:\software\奶龙找对象网页`），
   Publish 到 GitHub（选 Public）。
2. 之后去网页上 **Settings → Pages** 开启即可。

## 更换背景图和音乐

- **换背景图**：把新图命名为 `bg.png` 直接覆盖 `assets/img/bg.png`（保持同名，
  页面不需要改任何代码）；`素材备选/` 里有 4 张我下载的候选图，想换哪张复制过去改名即可。
- **换音乐**：把新音频命名为 `nailong_laugh.mp3` 覆盖 `assets/audio/nailong_laugh.mp3`
  （推荐 mp3 格式，其他格式需同步改 `index.html` 里的 `<audio src>` 后缀）。

## 说明

- 背景音乐会在打开页面时尝试自动播放；若被浏览器拦截（Chrome/Safari 常见策略），
  点击页面任意位置即可开始，右下角黄色圆钮可随时开关。
- 页面内容（名字、身高、体重等资料）都在 `index.html` 里，想改文案直接搜对应文字修改即可。
