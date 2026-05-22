# Love Catcher - For Nisrin ♥

A Disney/Mickey Mouse themed 2D game, packaged as a mobile app.

---

## 方法一：PWA 安装（最简单，推荐）

PWA（Progressive Web App）可以让 Nisrin 直接从浏览器安装到手机桌面，使用体验和原生 App 一样（全屏、离线可用、有图标）。

### 步骤：

1. **把项目部署到网上**（任选一种）：

   **GitHub Pages（免费）：**
   ```bash
   git init
   git add .
   git commit -m "Love Catcher game"
   git remote add origin https://github.com/<your-username>/nisrin.git
   git push -u origin main
   ```
   然后去 GitHub 仓库 → Settings → Pages → 选 main branch → 保存。
   几分钟后网址就是：`https://<your-username>.github.io/nisrin/game.html`

   **Netlify（拖拽部署）：**
   - 打开 https://app.netlify.com/drop
   - 把整个 `nisrin` 文件夹拖进去
   - 自动获得一个链接

2. **在 Nisrin 手机上打开链接**

3. **安装到桌面：**
   - **Android Chrome**: 打开网页 → 点击菜单(⋮) → "添加到主屏幕" / "安装应用"
   - **iPhone Safari**: 打开网页 → 点分享按钮(↑) → "添加到主屏幕"

4. **完成！** 桌面上会出现 Love Catcher 图标，点开就全屏玩！

---

## 方法二：打包成 Android APK（Capacitor）

如果你想生成一个真正的 `.apk` 文件直接安装到手机：

### 前置要求：
- Node.js (https://nodejs.org)
- Android Studio (https://developer.android.com/studio)

### 步骤：

```bash
# 1. 安装依赖
npm install

# 2. 添加 Android 平台
npx cap add android

# 3. 同步 web 文件到 Android 项目
npx cap sync android

# 4. 在 Android Studio 中打开
npx cap open android
```

在 Android Studio 中：
- 等 Gradle 同步完成
- 点击 Build → Build Bundle(s) / APK(s) → Build APK(s)
- APK 文件会在 `android/app/build/outputs/apk/debug/` 目录下
- 把 APK 传到 Nisrin 手机上安装即可

---

## 方法三：本地测试（电脑上模拟手机体验）

```bash
# 安装 http-server
npm install

# 启动本地服务器
npx http-server . -p 8080
```

然后打开 `http://localhost:8080/game.html`，用浏览器开发者工具的手机模式测试。

---

## 文件结构

```
nisrin/
├── game.html          # 游戏主文件
├── index.html         # 浪漫心形页面
├── manifest.json      # PWA 配置
├── sw.js              # Service Worker（离线支持）
├── icon.svg           # 应用图标
├── capacitor.config.json  # Capacitor 配置
├── package.json       # Node 项目配置
└── README.md          # 本文件
```

---

Made with ♥ by Han for Nisrin
# nisrin
