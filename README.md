# 小鸡过河（Chicken River Crossing）

一个可直接运行的纯前端 Canvas 网页小游戏。

## 本地运行

在项目根目录执行：

```bash
python3 -m http.server 4173
```

然后打开：

- `http://127.0.0.1:4173/`

## Deploy on GitHub Pages

本项目是纯静态站点（`index.html + style.css + script.js`），可直接部署到 GitHub Pages。

### 目录与路径要求（已满足）

- 入口文件在仓库根目录：`index.html`
- 资源路径使用相对路径：
  - `index.html` 通过 `./style.css` 引入样式
  - `index.html` 通过 `./script.js` 引入脚本
- 无需后端服务、无需构建步骤。

### 部署步骤

1. 将代码推送到 GitHub 仓库默认分支（如 `main`）。
2. 进入仓库页面：`Settings` → `Pages`。
3. 在 **Build and deployment** 中设置：
   - **Source**: `Deploy from a branch`
   - **Branch**: `main`（或你的发布分支）
   - **Folder**: `/ (root)`
4. 点击 **Save**。
5. 等待 Pages 构建完成后，访问页面：
   - `https://<你的用户名>.github.io/<仓库名>/`

### 常见阻塞项（本仓库已规避）

- 入口文件不在根目录：已将 `index.html` 放在根目录。
- 使用绝对路径导致子路径部署 404：已使用相对路径 `./style.css`、`./script.js`。
- 依赖 Node/后端构建：当前无此依赖。

