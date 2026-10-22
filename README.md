# Jienan Wang · 王介南

Personal site for [www.jienanwang.com](https://www.jienanwang.com). Two self-contained HTML pages, served by Vercel as static files with no install or build step.

王介南的个人网站：[www.jienanwang.com](https://www.jienanwang.com)。两个独立的 HTML 页面，由 Vercel 以静态文件提供，无需安装依赖，也无需构建。

## Pages · 页面

| URL | File · 文件 | Page · 页面 |
| --- | --- | --- |
| `/` | `index.html` | Bilingual homepage · 双语首页 |
| `/zh` | `zh/index.html` | Chinese page · 中文页 |

`favicon.ico` is the site icon. Each HTML file inlines its own CSS, JavaScript, and images. The only external request is Google Fonts. The EN / 中文 buttons on the homepage switch that page's own copy; they do not open `/zh`. The Chinese page has no link back to `/`.

`favicon.ico` 是网站图标。每个 HTML 文件都内联了自己的 CSS、JavaScript 和图片，外部请求只有 Google Fonts。首页上的 EN / 中文按钮只切换该页自己的文案，不会打开 `/zh`。中文页也没有返回 `/` 的链接。

## Update the site · 如何更新

1. Edit `index.html` and/or `zh/index.html`. Leave each file self-contained.
2. Open a pull request.
3. Check the Vercel preview deployment.
4. Merge the pull request into `main`. That deploys [www.jienanwang.com](https://www.jienanwang.com).

1. 编辑 `index.html` 和/或 `zh/index.html`。请保持每个文件自成一体。
2. 提交 Pull Request。
3. 在 Vercel 预览部署里检查页面。
4. 将 Pull Request 合并进 `main`，即可部署到 [www.jienanwang.com](https://www.jienanwang.com)。

`vercel.json` sets the framework to Other (`null`), skips install and build, serves the repository root, and turns on clean URLs so `/zh` maps to `zh/index.html`. If a preview still tries to build Astro, set **Framework Preset** to **Other** in the Vercel project settings. The dashboard value can take precedence when `vercel.json` does not override it.

`vercel.json` 将框架设为 Other（`null`），跳过安装和构建，以仓库根目录作为输出，并开启 clean URLs，使 `/zh` 对应 `zh/index.html`。如果预览仍然尝试构建 Astro，请在 Vercel 项目设置里把 **Framework Preset** 改为 **Other**。当 `vercel.json` 未能覆盖时，以控制台中的设置为准。
