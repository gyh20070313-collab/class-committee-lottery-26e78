# 26英语78班班委竞选随机抽签系统

## 直接使用

- 双击根目录的 `index.html` 即可离线抽签。
- 通过网页访问时，首次成功打开后会缓存页面，临时断网仍可继续使用。
- 数据保存在当前浏览器中；更换设备或清除浏览器数据后不会自动同步。
- “抽签记录”页面支持删除单条记录或一键清空全部记录；删除记录不会改变岗位的已确认结果。
- 候选名单支持一键只选男生或只选女生；默认名单中有 8 名男生，其余为女生。

## 免费部署到 GitHub Pages

1. 新建一个 GitHub 仓库。
2. 上传 `index.html`、`manifest.json`、`service-worker.js` 和 `icon.svg`。
3. 打开仓库的 **Settings → Pages**。
4. 在 **Build and deployment** 中选择 **Deploy from a branch**，分支选择 `main`，目录选择 `/ (root)`，保存。
5. 等待约 1—2 分钟，GitHub 会显示访问网址。

## 公平性

系统使用 `window.crypto.getRandomValues()` 与无放回抽取。拒绝采样避免取模偏差，不包含预设结果或权重。
