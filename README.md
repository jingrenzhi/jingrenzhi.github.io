# jingrenzhi.github.io

学术个人主页，纯静态 HTML + CSS，无需构建工具。通过 GitHub Pages 发布在 <https://jingrenzhi.github.io/>。

## 目录结构

```
index.html          主页（简介、研究方向、新闻、论文、联系方式）
cv.html             CV 页（经历、教育、奖项、教学与指导、学术服务）
assets/style.css    样式（Jon Barron 式极简单栏；深色模式跟随系统，含移动端适配）
assets/photo.svg    头像占位图
assets/favicon.svg  浏览器标签页图标
files/              放 CV 等可下载文件（如 files/cv.pdf）
.nojekyll           让 GitHub Pages 跳过 Jekyll，直接发布静态文件
```

## 如何修改内容

内容在 `index.html` 和 `cv.html` 里，搜索 `TODO` 和方括号 `[...]` 即可找到需要替换的占位内容。

- **头像**：把照片存为 `assets/photo.jpg`，并将 `index.html` 中的 `assets/photo.svg` 改成 `assets/photo.jpg`。
- **CV**：把 PDF 存为 `files/cv.pdf`。
- **论文**：复制一个 `<li class="pub">...</li>` 块并修改；自己的名字用 `<strong>` 包起来。
- **论文配图**：把图放进 `assets/pubs/`（建议约 640×400、8:5 比例，jpg/png/gif 均可），并把该论文 `<img class="pub-img">` 的 `src` 改成对应文件；没有图的论文删掉这一行 `<img>` 即可。
- **新闻**：在 `<ul class="news">` 顶部加一行 `<li>`。
- **链接颜色 / 悬停高亮色**：改 `assets/style.css` 顶部的 `--link` 和 `--highlight`。

## 本地预览

```bash
python3 -m http.server 8000
```

然后打开 <http://localhost:8000>。

## 发布

```bash
git add -A && git commit -m "Update homepage" && git push
```

推送到 `main` 分支后约一分钟自动上线。
