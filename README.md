# 1024 H5 小游戏

经典的 1024 数字合成游戏，单文件实现，零依赖，纯前端。

**在线游玩**：

- Cloudflare Pages（国内访问更稳）：https://game-1024.pages.dev/
- GitHub Pages：https://brentdai.github.io/Game_1024/

## 玩法

- 滑动（手机）或方向键 / WASD（电脑）移动全部方块
- 相同数字碰撞合并翻倍，合成 **1024** 获胜，可继续挑战 2048
- 棋盘填满且无法移动时游戏结束

## 功能

- 触摸滑动 / 鼠标拖拽 / 键盘三种操作方式
- Web Audio 实时合成音效（滑动、合并、胜利、失败），含静音开关
- 移动端适配 + 微信内置浏览器 / iOS Safari 音频解锁兼容
- 计分与最高分（localStorage 持久化）
- 断点续玩：刷新后自动恢复上次棋局

## 部署

推送到 `main` 分支后，GitHub Actions 会自动部署到 Cloudflare Pages（配置见 `.github/workflows/deploy.yml`），需要的仓库 Secrets：

| Secret | 说明 |
|---|---|
| `CLOUDFLARE_API_TOKEN` | Cloudflare API Token（Pages Edit 权限） |
| `CLOUDFLARE_ACCOUNT_ID` | Cloudflare Account ID |

## 本地运行

直接用浏览器打开 `index.html` 即可，无需构建、无需服务器。
