# 重命名计划：将 "hux" 替换为 "Guan"

## 1. 文件重命名

| 原文件名 | 新文件名 |
| :--- | :--- |
| `css/hux-blog.css` | `css/guan-blog.css` |
| `css/hux-blog.min.css` | `css/guan-blog.min.css` |
| `js/hux-blog.js` | `js/guan-blog.js` |
| `js/hux-blog.min.js` | `js/guan-blog.min.js` |
| `less/hux-blog.less` | `less/guan-blog.less` |

## 2. 内容修改

### 2.1 package.json
- 修改 `name` 字段：`"name": "Guan Blog"`
- 修改 `description` 字段：`"description": "Guan Blog is a simple, beautiful and opensource blog theme for Jekyll."`

### 2.2 pwa/manifest.json
- 修改 `name` 字段：`"name": "Guan Blog"`
- 修改 `short_name` 字段：`"short_name": "Guan Blog"`

### 2.3 _config.yml
- 确保所有 "hux" 引用已替换为 "Guan"（根据之前的检查，似乎已经完成）

### 2.4 _includes/head.html
- 替换 CSS 引用：`<link rel="stylesheet" href="{{ "/css/hux-blog.min.css" | prepend: site.baseurl }}">` → `<link rel="stylesheet" href="{{ "/css/guan-blog.min.css" | prepend: site.baseurl }}">`
- 替换 `#huxblog_navbar` 为 `#guanblog_navbar`

### 2.5 _includes/footer.html
- 替换 "Powered by Hux Blog" 为 "Powered by Guan Blog"
- 替换 JS 引用：`<script src="{{ "/js/hux-blog.min.js" | prepend: site.baseurl }}"></script>` → `<script src="{{ "/js/guan-blog.min.js" | prepend: site.baseurl }}"></script>`
- 替换注释中的 "Hux" 为 "Guan"

### 2.6 _doc/Manual.md
- 替换文档中的 "Hux Blog User Manual" 为 "Guan Blog User Manual"
- 替换作者示例中的 "Hux" 为 "Guan"
- 替换 GitHub 用户名配置中的 "huxpro" 为 "guanyugangstar"

### 2.7 README.md
- 替换标题中的 "Hux Blog" 为 "Guan Blog"
- 替换链接 `https://huangxuan.me` 为你的博客地址
- 替换版权信息中的 "Huxpro" 为 "guanyugangstar"

### 2.8 Rakefile
- 替换模板中的作者字段：`author: "Hux"` → `author: "Guan"`

### 2.9 js/sw-registration.js
- 替换注释中的 "@huxpro" 为 "@guanyugangstar"

### 2.10 CSS/LESS 文件
- 在 `css/guan-blog.css` 和 `less/guan-blog.less` 中，替换所有 `#huxblog_navbar` 选择器为 `#guanblog_navbar`

## 3. 实施步骤

1. 备份整个项目
2. 按照上述表格重命名文件
3. 按照上述内容修改列表逐一修改文件内容
4. 测试网站功能确保一切正常
5. 提交更改到版本控制系统