# 香港 2 天 · 旅行手册

单文件静态站。`public/index.html` 是全部内容，零外部依赖（无字体、无图片、无 CDN），
浏览器加载后即可离线查看；也可以直接把 `public/index.html` 存到手机里离线打开。

## 部署（Cloudflare Workers + GitHub 自动发布）

仓库里只需要两个文件：

    public/index.html   页面本体
    wrangler.jsonc      Workers 配置

在 Cloudflare 侧连接本仓库，构建命令留空，部署命令用 `npx wrangler deploy`。
之后每次 push 到 main 分支，Cloudflare 会自动重新部署。

## 隐私

页面内不含订单号、证件号、房间号。
