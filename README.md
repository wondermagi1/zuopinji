# gxr 的前端网页作品集

使用 HTML 和 CSS 制作的静态作品集。深绿色背景、珊瑚红点缀、作品预览卡片，支持桌面、平板和手机布局。卡片使用原生链接，在新标签页打开对应作品，并提供鼠标悬停与键盘焦点效果。

## 文件结构

```text
index.html       页面内容与作品链接
style.css        页面样式与响应式布局
script.js        保留的脚本入口，当前页面无需 JavaScript
img/             三个作品的预览图片
vercel.json      Vercel 静态部署配置
```

## 本地预览

直接用浏览器打开 `index.html` 即可。也可以在项目根目录运行 `python -m http.server 8000`，访问 http://localhost:8000 。无需 npm、打包工具或环境变量。

## 连接 Vercel

1. 登录 Vercel，选择 **Add New → Project**。
2. 连接 GitHub，授权访问并导入 `wondermagi1/zuopinji`。
3. **Root Directory** 保持仓库根目录 `.`，不要填写旧的 `zuopin` 子目录。
4. **Framework Preset** 为 **Other**；无需安装和构建命令，输出目录为 `.`。仓库中的 `vercel.json` 已配置这些设置。
5. 点击 **Deploy**。生产分支使用 `main`，后续推送至该分支可触发自动部署。

如果复用以前的 Vercel 项目，请检查 Settings 中 Root Directory 是否仍为 `zuopin`，将其改为仓库根目录，并确认 Git 连接的是本仓库、生产分支是 `main`。

本项目没有服务端、API 密钥或环境变量。Google Fonts 不可访问时会使用系统字体，不影响布局和链接。作品卡片跳转到独立站点，这些站点的可用性由各自项目维护。

部署后检查首页、三张图片和卡片跳转；缩小窗口确认卡片自动换列。如果 Vercel 看不到仓库，需要在 GitHub 的 Vercel 应用授权中授予本仓库访问权限。

官方参考：[Vercel 配置](https://vercel.com/docs/project-configuration/vercel-json)、[GitHub 集成](https://vercel.com/docs/git/vercel-for-github)。

## 更新作品

- 修改 `index.html` 中卡片的标题、标签和 `href`。
- 替换 `img/` 中的图片，注意文件名大小写与 HTML 一致。
- 修改 `style.css` 调整颜色、间距与截图裁切。
- 提交并推送到 GitHub 的 `main` 分支。
