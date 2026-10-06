# 小事清单

简洁的中文待办事项网页，采用暖白与绿色界面，支持桌面和手机布局。

## 功能

- 添加任务（Enter 或点击添加，拒绝空白输入）
- 标记完成、恢复待完成、删除任务
- 全部 / 待完成 / 已完成筛选及数量统计
- 使用 localStorage 保存任务，刷新后保留；数据仅保存在当前浏览器
- 通过文本节点展示任务内容，避免将用户输入作为 HTML 执行

## 运行

无需安装依赖或构建。直接用浏览器打开根目录的 `index.html`，或在仓库目录运行：

```sh
python3 -m http.server 8000
```

然后访问 http://localhost:8000。

## 项目结构

- `index.html`：GitHub Pages 根目录入口，包含全部 HTML、CSS 和 JavaScript
- `.nojekyll`：禁用 Jekyll，直接提供静态文件
- `dist/index.html`：现有 Sites 发布版本；更新 Sites 时需与根目录入口同步
- `.openai/hosting.json`：现有 Sites 项目的部署配置，不含凭据

## 验证

已通过 DOM 交互测试：添加、空值校验、完成、筛选、删除、刷新恢复、文本安全和空状态。真实浏览器视觉检查尚未执行。

## 在线网页

https://xiaoshi-todo-muwdykfp.jiakailee424.chatgpt.site （Sites 私有访问）

## GitHub Pages 部署

将本次 Pull Request 合并到 `main` 后，在 GitHub 仓库中打开 **Settings → Pages**：

1. 在 **Build and deployment → Source** 选择 **Deploy from a branch**。
2. 将分支设置为 **main**，目录设置为 **/(root)**，点击 **Save**。
3. 等待 Pages 部署完成，访问 https://lijiakai123.github.io/friendly-noodle/ 。

网页无需构建，也不依赖外部字体、图片或脚本。所有样式和脚本均内嵌，没有 `/` 开头的资源路径、`<base>` 标签或需要服务器回退的路由，因此可直接运行于 `/friendly-noodle/` 子路径。后续新增资源请使用 `./assets/...` 等相对路径。

GitHub Pages 和 Sites 是不同站点来源，浏览器本地任务数据不会在两者之间自动同步。
