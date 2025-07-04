# 法修的个人博客 | Wangzhao.GitHub.io

一个基于GitHub Pages的个人博客网站，使用Time Machine主题构建。

**网站地址**: https://faxiubite.github.io/blog/  
**仓库地址**: https://github.com/faxiubite/wangzhao.github.io

## 📖 关于博客 | About

* 曾是一个思想大于行动的人，计划太多行动太少，错过遗失了太多...
* 建立博客分享个人成长之路，欢迎大家分享共同成长
* 成长源自每天的进步，努力向前走
* 加油，极客之路

## 🔧 技术栈 | Tech Stack

- **前端**: HTML5, CSS3, JavaScript (jQuery)
- **主题**: Time Machine Theme by Jon Rohan
- **托管**: GitHub Pages
- **特性**: 响应式设计, 代码高亮, 动态导航

## 📚 开发文档 | Documentation

### 完整文档
- **[📖 API 文档](API_DOCUMENTATION.md)** - 完整的API参考和组件文档
- **[📋 组件示例](COMPONENT_EXAMPLES.md)** - 详细的使用示例和代码片段
- **[⚡ 快速参考](QUICK_REFERENCE.md)** - 开发者快速参考指南

### 核心功能
- 🔢 **自动代码行号** - 为代码块自动添加行号
- 🧭 **动态导航** - 基于页面标题的浮动导航
- 📜 **平滑滚动** - 一键返回顶部功能
- 🎨 **语法高亮** - 支持多种编程语言的代码高亮

## 🚀 快速开始 | Quick Start

1. **克隆仓库**
   ```bash
   git clone https://github.com/faxiubite/wangzhao.github.io.git
   cd wangzhao.github.io
   ```

2. **配置站点信息**
   编辑 `params.json` 文件：
   ```json
   {
       "name": "您的站点名称",
       "tagline": "您的标语",
       "body": "您的内容..."
   }
   ```

3. **自定义内容**
   编辑 `index.html` 中的内容部分

4. **本地测试**
   在浏览器中打开 `index.html` 文件预览

5. **部署到GitHub Pages**
   ```bash
   git add .
   git commit -m "更新网站内容"
   git push origin gh-pages
   ```

## 📂 文件结构 | File Structure

```
wangzhao.github.io/
├── index.html                 # 主页面
├── README.md                  # 项目说明
├── params.json               # 站点配置
├── images/                   # 图片资源
├── javascripts/
│   └── script.js            # 核心功能脚本
├── stylesheets/
│   ├── stylesheet.css       # 主样式文件
│   └── github-dark.css      # 代码高亮样式
└── docs/                    # 文档文件
    ├── API_DOCUMENTATION.md
    ├── COMPONENT_EXAMPLES.md
    └── QUICK_REFERENCE.md
```

## 🛠️ 自定义指南 | Customization

### 修改颜色主题
```css
/* 在 stylesheet.css 中 */
a { color: #your-color; }
body { background: #your-background; }
```

### 调整布局宽度
```css
.wrapper { width: 800px; } /* 默认: 675px */
```

### 添加新功能
```javascript
$(document).ready(function(){
    // 在这里添加您的自定义代码
});
```

## 🤝 贡献 | Contributing

欢迎提交 Issue 和 Pull Request！

1. Fork 本仓库
2. 创建功能分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

## 📄 许可证 | License

本项目采用 MIT 许可证 - 查看 [LICENSE](LICENSE) 文件了解详情

## 📞 联系方式 | Contact

- **GitHub**: [@faxiubite](https://github.com/faxiubite)
- **博客**: https://faxiubite.github.io/blog/

---

*⭐ 如果这个项目对您有帮助，请给它一个 Star!*
