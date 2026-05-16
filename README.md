# 我的博客（静态站点）

这是一个用于托管到 GitHub Pages 的静态站点仓库，内容为 Hexo 生成后的发布产物（类似 Hexo 工程里的 `public/` 目录）。如果你在找 Hexo 的源码工程（`source/`、`themes/`、`_config.yml`、`package.json` 等），它不在这个仓库中。

- 在线访问：<https://dmqm.github.io>
- 生成器：Hexo 7.2.0
- 作者：dmqm

## 仓库内容

- `index.html`：站点首页
- `archives/`：归档页
- `2024/`：按日期组织的文章静态页面
- `css/`、`js/`、`lib/`、`img/`、`fancybox/`：主题资源与前端依赖
- `content.json`：站点内容索引（用于搜索/索引类功能的 JSON 输出）

## 本地预览

直接用静态服务器预览（推荐），不要用浏览器直接双击打开 `index.html`（相对路径与路由行为可能不同）。

```bash
python3 -m http.server 8000
```

然后打开：<http://localhost:8000>

## 部署

该仓库可以直接作为 GitHub Pages 的发布仓库使用：

1. 将本仓库推送到 GitHub
2. 在仓库 Settings → Pages 中选择发布分支（常见为 `main`/`master`）与根目录 `/`
3. 保存后等待 Pages 构建完成，即可通过站点地址访问

如果你是从 Hexo 源码工程发布到这里，建议流程是：

1. 在 Hexo 源码工程中生成静态文件：`hexo generate`
2. 将生成结果（通常是 `public/` 下的内容）同步覆盖到本仓库根目录
3. 提交并推送到远端，触发 GitHub Pages 更新

## 已知事项

- 导航中可能包含 `/about`、`/atom.xml` 等链接；如果对应文件不存在，会产生 404，需要在 Hexo 源码工程里生成并发布，或在主题配置中移除。
- 页面中集成了多说（Duoshuo）评论脚本；该服务已停止维护多年，如需继续评论功能，建议迁移到其他方案（例如 Giscus/Disqus 等）。

## 许可与版权

本仓库当前未提供 LICENSE 文件。除非另有声明，文章内容版权归作者所有；如需以开源协议发布，请补充 LICENSE 并在此说明。

