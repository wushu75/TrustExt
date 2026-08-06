# Chrome Web Store — Submission Pack · 商店提交资料

Everything below is copy-paste ready for the Chrome Web Store developer dashboard. Fields map 1:1 to the dashboard sections. Assets are in this `docs/` folder.

> One-time setup: you need a Chrome Web Store **developer account** (one-time US$5 registration fee) at https://chrome.google.com/webstore/devconsole, then **Add new item** and upload `TrustExt-v1.0.0.zip` (the extension-only zip, not the repo zip).

---

## 1. Store listing

### Item title
```
TrustExt — Trusted open-source extensions
```
(Localized zh title, added under the zh_CN listing locale:)
```
可信扩展 TrustExt — 安全安装开源扩展
```

### Summary (short description · max 132 characters)
**English**
```
Discover and install trusted open-source extensions without the blocked store or a VPN. Each links to its official, verifiable source.
```
**简体中文**
```
无需访问商店、无需 VPN，安全发现并安装高质量开源扩展。每个都开源可核验，并附官方源码链接。完全免费 · MIT。
```

### Detailed description (max 16,000 characters)

**English**
```
TrustExt is a free, open-source launcher that helps you discover and install high-quality open-source browser extensions — and links you straight to each project's official source code so you can verify it before you install.

WHY IT EXISTS
For many people on Chromium browsers, the Chrome Web Store can be slow or unreachable. The usual workarounds cost you something: running a VPN just to install an ad blocker, or downloading .crx files from sites you can't trust. TrustExt removes that trade-off.

WHAT YOU GET
• A curated list of trusted open-source extensions, each with its license shown
• A direct link to every extension's official GitHub repository
• One-tap switching between English and 中文, with your choice remembered
• A clear "load unpacked" guide so you can install offline — no store access required
• A tiny footprint: only the "storage" permission (to remember your language), no trackers, no telemetry

TRUST THROUGH VERIFIABILITY
TrustExt and every extension it lists are open source. The full code is public, so you can read it yourself — or rely on the community that already has. You install from each project's own repository, never a repackaged copy from us.

INSIDE v1.0
uBlock Origin, Dark Reader, Stylus, Violentmonkey, Bitwarden, Vimium, SingleFile, SponsorBlock, Privacy Badger, Simple Translate, Refined GitHub, and uBlacklist.

Free forever, MIT licensed. Source code and contributions: https://github.com/wushu75/TrustExt
```

**简体中文**
```
TrustExt（可信扩展）是一个完全免费的开源导航工具，帮你发现并安装高质量的开源浏览器扩展，并直接给出每个项目的官方源码链接 —— 让你在安装前就能自己核验代码。

为什么需要它
对许多 Chromium 浏览器用户来说，Chrome 网上应用店经常访问缓慢或无法打开。常见的土办法都要付出代价：为了装一个广告拦截器专门去开 VPN，或从不可信的网站下载 .crx 文件。TrustExt 把这个取舍去掉了。

你会得到
• 一份精选的可信开源扩展清单，每个都标注许可证
• 每个扩展的官方 GitHub 仓库直链
• 一键在 English 与 中文 之间切换，并记住你的选择
• 清晰的「加载已解压」指引，可离线安装，无需访问商店
• 极小体积：仅申请 “storage” 权限（用于记住语言），无追踪、无遥测

以「可核验」建立信任
TrustExt 及其收录的每个扩展都是开源项目，完整代码公开 —— 你可以自己阅读，或信任已经读过的社区。你从每个项目自己的仓库安装，而不是我们二次打包的副本。

v1.0 内置
uBlock Origin、Dark Reader、Stylus、Violentmonkey、Bitwarden、Vimium、SingleFile、SponsorBlock、Privacy Badger、Simple Translate、Refined GitHub、uBlacklist。

永久免费，基于 MIT 许可证。源码与贡献：https://github.com/wushu75/TrustExt
```

### Category
```
Tools
```
(Alternative fits: “Developer Tools” or “Privacy & Security”. Avoid “Productivity” — it's the most saturated category.)

### Language
```
Chinese (Simplified)
```
(Set primary language to your largest audience. The extension itself is fully bilingual; you can add an English listing locale too.)

---

## 2. Graphic assets

| Dashboard slot | Required? | Size | File in `docs/` |
|---|---|---|---|
| Store icon | Yes | 128×128 PNG | `store-icon-128.png` (or the `icons/icon128.png` already in the zip) |
| Screenshot 1 | Yes (≥1) | 1280×800 PNG | `store-screenshot-01.png` — *Install without the blocked store* |
| Screenshot 2 | — | 1280×800 PNG | `store-screenshot-02.png` — *Open source & verifiable* |
| Screenshot 3 | — | 1280×800 PNG | `store-screenshot-03.png` — *One-click bilingual* |
| Screenshot 4 | — | 1280×800 PNG | `store-screenshot-04.png` — *Minimal permissions* |
| Small promo tile | Yes | 440×280 PNG | `promo-small-440x280.png` |
| Marquee promo tile | Optional | 1400×560 PNG | `promo-marquee-1400x560.png` (enables featured placement) |

Notes:
- Screenshots **can** be localized per listing locale; the four provided use bilingual captions so one set works for both.
- Promo tiles are **not** locale-specific, so they're kept graphic-forward with minimal text (targeted at the primary audience).
- A promotional **YouTube video** is optional but boosts installs — link one if you make the Bilibili/YouTube demo.

---

## 3. Privacy practices

### Single purpose (required)
```
TrustExt helps users discover and install trusted open-source browser extensions by presenting a curated list and linking to each extension's official source repository.
```

### Permission justification
**storage**
```
The "storage" permission is used only to save the user's language preference (English or Chinese) locally on their device, so the popup opens in their chosen language. No other data is stored, and nothing is transmitted off the device.
```
(TrustExt requests no host permissions, no content scripts, and no other permissions.)

### Remote code
```
No — the extension does not use remote code. All HTML, CSS, and JavaScript are bundled in the package.
```

### Data usage — disclosures
Certify all of the following in the dashboard:
- Personally identifiable information — **Not collected**
- Health information — **Not collected**
- Financial and payment information — **Not collected**
- Authentication information — **Not collected**
- Personal communications — **Not collected**
- Location — **Not collected**
- Web history — **Not collected**
- User activity — **Not collected**
- Website content — **Not collected**

Required certifications (all true for TrustExt):
- ☑ I do not sell or transfer user data to third parties, outside of the approved use cases
- ☑ I do not use or transfer user data for purposes unrelated to my item's single purpose
- ☑ I do not use or transfer user data to determine creditworthiness or for lending purposes

### Privacy policy URL (required — because the extension declares the `storage` permission)
```
https://wushu75.github.io/TrustExt/privacy.html
```
(Publish GitHub Pages from `/docs` first — see `docs/DEPLOY.md` — so this URL resolves. A plain fallback is the repo file: https://github.com/wushu75/TrustExt/blob/main/PRIVACY.md)

---

## 4. Distribution

- **Visibility:** Public
- **Pricing:** Free
- **Regions:** All regions (no reason to restrict)

---

## 5. Pre-submit checklist

- [ ] Developer account registered (US$5 one-time fee paid)
- [ ] `TrustExt-v1.0.0.zip` uploaded (extension-only zip, manifest at root)
- [ ] Title, summary, and detailed description pasted (EN)
- [ ] Store icon (128×128) uploaded
- [ ] At least 1 screenshot (1280×800) uploaded — ideally all 4
- [ ] Small promo tile (440×280) uploaded
- [ ] Marquee tile (1400×560) uploaded (optional)
- [ ] Single purpose + `storage` justification filled in
- [ ] Data-usage disclosures completed + 3 certifications checked
- [ ] Privacy policy URL added and publicly reachable
- [ ] Category (Tools) and Language set
- [ ] (Optional) zh_CN listing locale added with the Chinese title/summary/description + screenshots
- [ ] Submit for review

---

## 6. Adding the Chinese (zh_CN) listing locale

In the dashboard, open the **Localize listing** control, add **Chinese (Simplified)**, and paste the zh title, zh summary, and zh detailed description above. You can reuse the same screenshots and promo tiles. This makes TrustExt discoverable to users searching in Chinese and shows the listing in their language.

---

## 7. Review tips (avoiding common rejections)

- **Match metadata to behavior.** The description promises only what the extension does (list + link to sources). No overclaiming.
- **Least privilege.** Only `storage` is requested, and the justification explains exactly why — reviewers reject vague or unused permissions.
- **No remote code / no obfuscation.** Everything is plain, readable, bundled JS.
- **Accurate privacy fields.** "Collects no data" matches the code; the privacy policy says the same. Mismatches here are a frequent rejection cause.
- **Keep future mirror/CRX features out of the store build.** Anything that side-loads or downloads packaged extensions belongs only in the GitHub/Gitee unpacked build, not the Web Store version.
- Reviews typically take a few days; if rejected, the email cites the exact policy — fix and resubmit.
