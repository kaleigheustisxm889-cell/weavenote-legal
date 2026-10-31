# 织念 WeaveNote — 隐私政策 / 用户协议（GitHub Pages 站点）

本目录是一个可直接发布到 **GitHub Pages** 的静态站点，包含：

- `index.html`：入口页（隐私政策 / 用户协议 两个入口）
- `privacy/index.html`：隐私政策（中文）
- `terms/index.html`：用户协议（中文）
- `assets/style.css`：样式（自适应手机/桌面，深色）
- `.nojekyll`：告诉 GitHub Pages 不要用 Jekyll 处理（避免路径/文件被忽略）

## 发布地址规则

发布后地址为（把 `<用户名>` 换成你的 GitHub 用户名）：

- 站点首页：`https://<用户名>.github.io/weavenote-legal/`
- **隐私政策**：`https://<用户名>.github.io/weavenote-legal/privacy/`
- **用户协议**：`https://<用户名>.github.io/weavenote-legal/terms/`

> 如果仓库名不是 `weavenote-legal`，把路径中的 `weavenote-legal` 换成实际仓库名。
> 如果仓库名是 `<用户名>.github.io`，地址则变成 `https://<用户名>.github.io/privacy/` 与 `https://<用户名>.github.io/terms/`。

## 方式 A：网页上传（不需要 Token，约 3 分钟）

1. 浏览器打开 GitHub，右上角 **+ → New repository**
2. 仓库名填 `weavenote-legal`，可见性选 **Public**，不要勾选 README / .gitignore，点 **Create repository**
3. 在新仓库页点 **uploading an existing file**，把本目录**全部内容**（含 `privacy/`、`terms/`、`assets/`、`index.html`、`.nojekyll`、本 README）拖进去，点 **Commit changes**
   - 注意：浏览器上传是保留文件夹结构的，拖整个目录即可
4. 进入仓库 **Settings → Pages**：
   - Source 选 **Deploy from a branch**
   - Branch 选 **main**，目录选 **/ (root)**，点 **Save**
5. 等 1~2 分钟，页面顶部/`Settings → Pages` 会显示站点地址，用它访问
6. 把 `<用户名>` 告诉我，或直接把你看到的隐私政策/用户协议地址发我，我帮你验证并写回工程配置

## 方式 B：命令行发布（需要你本机已登录 GitHub 凭据）

在本目录中：

```bash
git init -b main
git add .
git commit -m "docs: add privacy policy and user agreement"
git remote add origin https://github.com/<用户名>/weavenote-legal.git
git push -u origin main
```

然后到仓库 **Settings → Pages** 选择 `main` / `/ (root)` 保存即可。

## 上架华为应用市场时填什么

- 隐私政策 URL：`https://<用户名>.github.io/weavenote-legal/privacy/`
- 用户协议 URL：`https://<用户名>.github.io/weavenote-legal/terms/`
- 隐私标签/数据安全表单按工程内 `docs/APPGALLERY_CHECKLIST.md` 填写
- 如果 GitHub Pages 在中国大陆访问不稳定导致审核失败：把同一套文件部署到国内可访问的静态托管（如阿里云 OSS/腾讯云 COS 静态网站、Gitee Pages 等），保持内容与路径不变即可

## 维护

- 修改协议内容时，同步更新：
  1. 本目录中对应的 `index.html`
  2. 工程内 `entry/src/main/ets/constants/LegalDocuments.ets`
  3. 工程内 `docs/PRIVACY_POLICY.md` / `docs/USER_AGREEMENT.md`
- 页面底部“最后更新”日期要同步改。
