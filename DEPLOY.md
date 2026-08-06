# Deploy & Mirror Guide · 部署与镜像指南

This covers publishing the landing page, mirroring to Gitee for Chinese users, and the social preview image. Everything here is optional — the extension works without any of it.

---

## English

### 1. Publish the landing page with GitHub Pages

The landing page is a single static file at `docs/index.html`, so no build step is needed.

1. Push this repo to GitHub (`main` branch).
2. Go to **Settings → Pages**.
3. Under **Build and deployment → Source**, choose **Deploy from a branch**.
4. Set the branch to `main` and the folder to **`/docs`**, then **Save**.
5. Wait ~1 minute. Your page goes live at:
   `https://wushu75.github.io/TrustExt/`

The social image (`docs/og-image.png`) and store screenshots ship in the same folder, so the Open Graph tags already resolve to the correct URL once Pages is live.

> If you use a custom domain, update the `og:url` and `og:image` values in `docs/index.html` to match.

### 2. Mirror to Gitee (recommended for Chinese users)

Many users in mainland China reach **Gitee** far more reliably than GitHub. A mirror widens your reach and gives people a fast download link.

**Option A — one-time import (simplest):**
1. Sign in to <https://gitee.com>, click **+ → 从 GitHub/GitLab 导入仓库** (Import repository).
2. Paste `https://github.com/wushu75/TrustExt` and import.

**Option B — keep it in sync (push to both):**
```bash
# add Gitee as a second remote
git remote add gitee https://gitee.com/<your-gitee-name>/TrustExt.git

# push to both from now on
git push origin main
git push gitee main
```
Or, on the Gitee repo page, enable **仓库镜像管理** (repo mirroring) to auto-pull from GitHub on a schedule.

**Gitee Pages:** on the Gitee repo, open the **Pages** service, pick the `master`/`main` branch and the `/docs` directory, then deploy. (Note: Gitee Pages may require real-name verification.)

Add both links near the top of your README so visitors can pick whichever loads:
```md
[GitHub](https://github.com/wushu75/TrustExt) · [Gitee 镜像](https://gitee.com/<your-gitee-name>/TrustExt)
```

### 3. Social preview image

`docs/og-image.png` (1200×630) is the card that shows when the landing page or repo link is shared on WeChat, V2EX, X/Twitter, Telegram, etc. It's already wired into `docs/index.html` via Open Graph and Twitter Card tags.

- To refresh it after a redesign, re-run your image tool or edit the source and re-export at exactly **1200×630**.
- After you change the live image, clear the scraper cache: paste the URL into the [Facebook Sharing Debugger](https://developers.facebook.com/tools/debug/) and click **Scrape Again** so platforms pick up the new version.
- GitHub itself uses its own auto-generated repo card; `og-image.png` controls how *your landing page link* previews.

---

## 简体中文

### 1. 用 GitHub Pages 发布落地页

落地页是单个静态文件 `docs/index.html`，无需构建。

1. 将仓库推送到 GitHub（`main` 分支）。
2. 打开 **Settings → Pages**。
3. 在 **Source** 选择 **Deploy from a branch**。
4. 分支选 `main`，目录选 **`/docs`**，点击 **Save**。
5. 约 1 分钟后即可访问：
   `https://wushu75.github.io/TrustExt/`

社交图片与商店截图都在同一目录，Pages 上线后 Open Graph 标签会自动指向正确地址。若使用自定义域名，请同步修改 `docs/index.html` 中的 `og:url` 与 `og:image`。

### 2. 镜像到 Gitee（强烈建议）

国内用户访问 **Gitee** 通常比 GitHub 稳定得多。做一个镜像能显著扩大触达，并提供更快的下载入口。

**方式 A —— 一次性导入（最简单）：**
1. 登录 <https://gitee.com>，点击 **+ → 从 GitHub/GitLab 导入仓库**。
2. 填入 `https://github.com/wushu75/TrustExt` 导入即可。

**方式 B —— 保持同步（同时推两端）：**
```bash
git remote add gitee https://gitee.com/<你的用户名>/TrustExt.git
git push origin main
git push gitee main
```
或在 Gitee 仓库页开启 **仓库镜像管理**，定时从 GitHub 自动拉取。

**Gitee Pages：** 在 Gitee 仓库开启 **Pages** 服务，选择分支与 `/docs` 目录部署（Gitee Pages 可能需要实名认证）。

建议在 README 顶部同时放两个链接，方便访客选择能打开的那个：
```md
[GitHub](https://github.com/wushu75/TrustExt) · [Gitee 镜像](https://gitee.com/<你的用户名>/TrustExt)
```

### 3. 社交分享图

`docs/og-image.png`（1200×630）是把落地页或仓库链接分享到微信、V2EX、X/Twitter、Telegram 时展示的卡片，已通过 Open Graph 与 Twitter Card 标签接入 `docs/index.html`。

- 改版后按 **1200×630** 重新导出即可。
- 更换图片后，平台会缓存旧图。可用 [Facebook 分享调试工具](https://developers.facebook.com/tools/debug/) 输入链接并点击 **Scrape Again** 强制刷新。
- 微信内分享同样读取 og 标签；如遇缓存，稍等或更换链接参数（如 `?v=2`）即可。

---

_Questions? Open an issue: https://github.com/wushu75/TrustExt/issues_
