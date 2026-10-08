# 英语师范教师就业决策平台｜GitHub Pages 发布包

这是只包含网站生产文件的发布包，不含工作簿、调研脚本和审查截图。

## 建议仓库与公开地址

- GitHub 仓库：`shy-sgsg/teacher-career-atlas`（公开仓库）
- Pages 地址：`https://shy-sgsg.github.io/teacher-career-atlas/`

生产文件已按 `/teacher-career-atlas/` 子路径构建。站点的城市报告链接、数据请求和客户端路由均使用该路径前缀。`site/404.html` 支持 GitHub Pages 对客户端路由的直接访问和刷新。

## 发布步骤

1. 在 `shy-sgsg` 账号下创建公开仓库 `teacher-career-atlas`。
2. 将本包中的所有内容解压到仓库根目录，提交并推送到 `main`。
3. 打开仓库 **Settings → Pages → Build and deployment**，将 **Source** 设为 **GitHub Actions**。
4. 在 **Actions** 中等待 `Deploy GitHub Pages` 成功。
5. 打开上面的 Pages 地址检查首页和内部页面。后续推送到 `main` 会自动更新网站。

GitHub 官方说明：自定义 Actions 工作流需上传 Pages artifact，并由 `actions/deploy-pages` 发布。见[GitHub Pages 自定义工作流文档](https://docs.github.com/en/pages/getting-started-with-github-pages/using-custom-workflows-with-github-pages)。

如果仓库名称不同，需将前端以 `VITE_BASE_PATH=/<仓库名>/` 重新构建，再替换 `site/` 内容。
