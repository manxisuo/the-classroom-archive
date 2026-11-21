# 旧时光课本阅览室 · 教材导入

## Import Textbook 工作流

本仓库的 `Import Textbook` 工作流可以自动下载 ZIP、验证 WebP 文件、提交到 GitHub 并触发 Pages 更新。

1. 准备一个可公开访问、可直接下载的 **HTTPS ZIP 链接**。ZIP 内目录格式：`assets/books/chinese-8/001.webp` 至 `154.webp`。
2. 打开仓库 **Actions → Import Textbook → Run workflow**。
3. 填写 `archive_url`、`book_id=chinese-8`、`expected_pages=154`。
4. 运行成功后，图片将自动提交到默认分支。Pages 需配置为从该分支发布。

> 注意：ChatGPT 的 sandbox 下载地址不是公开 HTTPS URL，不能直接填入 archive_url。可先将 ZIP 上传到 GitHub Release、对象存储等可直链下载的位置。仅上传有公开传播授权的教材。

### 数据约定

图片文件命名使用三位数字顺序，阅读器通过 `assets/books/chinese-8/NNN.webp` 加载。未来可以将书籍元数据迁移到独立 JSON。
