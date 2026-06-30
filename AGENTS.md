# cursor-ios

## Cursor Cloud specific instructions

### 项目概况
- 这是一个静态前端项目，目前不包含任何构建系统、包管理文件（无 `package.json`）或后端服务。
- `main` 分支当前仅有 `README.md`。实际的应用代码位于功能分支中（例如 `cursor/tetris-game-e5d6` / PR #1 的 `tetris.html`），是一个自包含的单文件网页应用。
- 页面通过 CDN 引入 Tailwind CSS（`https://cdn.tailwindcss.com`）和 Google Fonts，逻辑为原生 JavaScript，因此**无需安装任何依赖**。

### 运行 / 开发
- 没有需要安装依赖或构建的步骤，因此**没有更新脚本（update script）**。
- 启动方式：在包含 `.html` 文件的目录下运行一个静态文件服务器即可，例如：
  - `python3 -m http.server 8000`，然后访问 `http://localhost:8000/<文件名>.html`。
- 该环境已预装 `python3`、`node`、`npm`，任选其一启动静态服务器均可。

### 测试 / 校验
- 目前仓库没有自动化测试、lint 或 build 流程。
- 验证方式为手动测试：用浏览器打开页面并交互（例如俄罗斯方块用方向键移动/旋转方块）。

### 备注
- 如果某个功能分支的应用代码尚未合入 `main`，可使用 `git worktree add <路径> origin/<分支名>` 在不离开当前分支的情况下检出并预览。
