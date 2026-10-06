# 小事清单

简洁的中文待办事项网页，采用暖白与绿色界面，支持桌面和手机布局。

## 功能

- 添加任务（Enter 或点击添加，拒绝空白输入）
- 标记完成、恢复待完成、删除任务
- 全部 / 待完成 / 已完成筛选及数量统计
- 使用 localStorage 保存任务，刷新后保留；数据仅保存在当前浏览器
- 通过文本节点展示任务内容，避免将用户输入作为 HTML 执行

## 运行

无需安装依赖或构建。直接用浏览器打开 `dist/index.html`，或在仓库目录运行：

```sh
python3 -m http.server 8000 --directory dist
```

然后访问 http://localhost:8000。

## 项目结构

- `dist/index.html`：全部 HTML、CSS 和 JavaScript 源码，亦为可部署网页
- `.openai/hosting.json`：现有 Sites 项目的部署配置，不含凭据

## 验证

已通过 DOM 交互测试：添加、空值校验、完成、筛选、删除、刷新恢复、文本安全和空状态。真实浏览器视觉检查尚未执行。

## 在线网页

https://xiaoshi-todo-muwdykfp.jiakailee424.chatgpt.site （Sites 私有访问）
