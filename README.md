# deepseek-harness-html

DeepSeek Harness 的 HTML 部署仓库 —— DSH(DeepSeek Harness)生成的交互卡片 / 页面默认归档于此。

## 约定(重要)

**除非特别说明,以后 DSH 生成的、需要部署的 HTML(交互卡片、页面等)默认都提交到本仓库 `cards/` 目录下。**

- 每个部署一个独立完整 HTML 文档:`cards/<name>.html`
- 公共样式与主题令牌:`assets/frame.css`(对齐 DSH 卡片环境的 `--background`、`--foreground`、`--card`、`--viz-series-*` 等变量,以及 `.btn`、`.viz-controls`、`.form-control` 等基类,明暗主题自动适配)
- 卡片集入口:`index.html`(新增卡片记得加一行入口)
- 推送后 GitHub Pages 自动构建更新

## 在线访问

https://DearPeter.github.io/deepseek-harness-html/

## 目录结构

```
.
├── index.html          # 卡片集入口(画廊)
├── assets/
│   └── frame.css       # 独立页面主题令牌 + 基类
└── cards/              # 部署的 HTML 卡片
    ├── sorting.html        # 排序算法可视化
    ├── reaction.html       # 反应速度测试
    └── binary-search.html  # 二分查找 · 逐步执行演示
```

## 添加新 HTML

1. 用 `assets/frame.css` 把 fragment 包装成独立文档,放入 `cards/`
2. 在 `index.html` 添加入口
3. `git add -A && git commit -m "..." && git push`
4. 等待约 1 分钟,GitHub Pages 自动更新
