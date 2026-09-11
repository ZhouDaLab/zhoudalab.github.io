# 周达课题组网站（ZhouDa Lab Website）

厦门大学周达课题组官方网站，使用 [Jekyll](https://jekyllrb.com/) 构建，并通过 GitHub Pages 和 Cloudflare Pages 部署。

- 访问地址：<https://zhoudalab.github.io/>
- GitHub 仓库：<https://github.com/ZhouDaLab/zhoudalab.github.io>

## 内容维护

| 内容 | 文件或目录 |
| --- | --- |
| 首页及个人简介 | `_pages/home.md` |
| 课题组成员 | `_data/students.yml` |
| 毕业成员 | `_data/alumni.yml` |
| 招生信息 | `_pages/openings.md` |
| 研究方向 | `_pages/research.md` |
| 论文列表 | `_pages/publications.md` |
| 新闻动态 | `_pages/news.md` |
| 课题组照片 | `_pages/pictures.md`、`images/` |
| 顶部导航和页脚 | `_includes/header.html`、`_includes/footer.html` |

修改 YAML 数据文件时请保持现有缩进，不要使用 Tab。成员照片放在 `images/teampic/` 中，文件名及大小写需与 `photo` 字段完全一致；页面图片统一放在 `images/` 下。

### 在 GitHub 网页端更新

1. 打开需要修改的文件，点击右上角的编辑按钮。
2. 完成修改后填写提交说明并点击 **Commit changes**。
3. 等待 Pages 构建完成，再访问网站并强制刷新浏览器缓存（Windows/Linux：`Ctrl+F5`，macOS：`Cmd+Shift+R`）。

## 本地预览

请先安装 Ruby 和 Bundler，然后在仓库根目录运行：

```bash
bundle install
bundle exec jekyll serve
```

浏览器访问 <http://127.0.0.1:4000/>。修改 `_config.yml` 后需要重启 Jekyll。

生成生产版本：

```bash
JEKYLL_ENV=production bundle exec jekyll build
```

PowerShell 中可使用：

```powershell
$env:JEKYLL_ENV = "production"
bundle exec jekyll build
```

构建结果位于 `_site/`。该目录以及 Jekyll 缓存均为本地生成内容，不应提交到 Git。

## 部署配置

### GitHub Pages

在仓库 **Settings → Pages** 中选择从 `master` 分支根目录部署。推送内容后，GitHub Pages 会自动重新构建网站。

### Cloudflare Pages

Cloudflare Pages 可使用以下构建参数：

| 配置项 | 值 |
| --- | --- |
| Framework preset | Jekyll |
| Build command | `bundle exec jekyll build` |
| Build output directory | `_site` |

自定义域名应在对应平台的 Pages 设置中维护；如需为 GitHub Pages 使用自定义域名，再添加内容正确的 `CNAME` 文件。

## 提交前检查

```bash
bundle exec jekyll build
git status
```

确认构建无报错，且提交中不包含 `_site/`、`.jekyll-cache/`、日志或操作系统生成的隐藏文件。
