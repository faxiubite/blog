# ⚡ Quick Reference Guide

## 🏗️ Essential File Structure
```
├── index.html          # Main page
├── params.json         # Configuration
├── javascripts/
│   └── script.js       # Core functionality
└── stylesheets/
    ├── stylesheet.css  # Main styles
    └── github-dark.css # Code highlighting
```

## 🎯 JavaScript Quick Commands

### Initialize Code Line Numbers
```javascript
$("pre").each(function(){
    // Automatic line numbering - no action needed
});
```

### Setup Navigation
```javascript
var headings = [];
if($(".markdown-body h1").length > 1) $(".markdown-body h1").each(collectHeaders)
else if($(".markdown-body h2").length > 1) $(".markdown-body h2").each(collectHeaders)
```

### Scroll to Top
```javascript
$(".current-section a").click(function(){
    $(window).scrollTop(0);
    return false;
})
```

## 🎨 Essential CSS Classes

| Class | Purpose | Usage |
|-------|---------|-------|
| `.wrapper` | Main container | `<div class="wrapper">` |
| `#container` | Content wrapper | `<div id="container">` |
| `.markdown-body` | Content styling | `<div class="markdown-body">` |
| `.current-section` | Navigation | Fixed position nav |
| `.download-bar` | Action bar | GitHub links section |
| `h1.title` | Site title | Main heading |

## ⚙️ Configuration (params.json)

```json
{
    "name": "Site Title",
    "tagline": "Site Description", 
    "body": "Markdown content",
    "note": "Don't delete this file!"
}
```

## 📝 HTML Template

```html
<!doctype html>
<html>
<head>
    <link rel="stylesheet" href="stylesheets/stylesheet.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    <script src="javascripts/script.js"></script>
    <title>Your Title</title>
</head>
<body>
    <div class="wrapper">
        <header><h1 class="title">Site Title</h1></header>
        <div id="container">
            <div id="main">
                <article class="markdown-body">
                    <!-- Your content here -->
                </article>
            </div>
        </div>
    </div>
</body>
</html>
```

## 🔧 Common Customizations

### Change Color Scheme
```css
a { color: #your-color; }
body { background: #your-bg; }
```

### Modify Layout Width
```css
.wrapper { width: 800px; } /* Default: 675px */
```

### Custom Navigation
```javascript
// Custom header collection
$(".your-headers").each(collectHeaders);
```

### Add Smooth Scrolling
```javascript
$('html, body').animate({scrollTop: 0}, 800);
```

## 📱 Mobile Responsive

```css
@media (max-width: 768px) {
    .wrapper { width: 100%; padding: 0 15px; }
    h1.title { font-size: 36px; }
    .current-section { bottom: 0; position: fixed; }
}
```

## 🐛 Debug Checklist

- ✅ jQuery loaded?
- ✅ `<pre>` tags for line numbers?
- ✅ Headers (H1/H2/H3) for navigation?
- ✅ `.markdown-body` wrapper?
- ✅ Image paths correct?
- ✅ CSS files linked?

## 📊 Performance Tips

- Use CDN for jQuery
- Optimize images
- Minimize HTTP requests
- Enable compression
- Cache static assets

## 🔗 Dependencies

- **jQuery 1.7.1+** (required)
- **Modern browser** (IE 8+ minimum)
- **GitHub Pages** (optional hosting)

## 🚀 Quick Setup

1. **Clone/fork repository**
2. **Edit `params.json`** with your info
3. **Modify `index.html`** content
4. **Customize `stylesheet.css`** if needed
5. **Test locally** before deploying
6. **Push to GitHub Pages**

## 💡 Code Snippets

### Add New Section
```html
<section class="new-section">
    <h2>Section Title</h2>
    <div class="markdown-body">
        <p>Content here...</p>
    </div>
</section>
```

### Custom Button
```css
.custom-btn {
    background: #4CAF50;
    color: white;
    padding: 10px 20px;
    text-decoration: none;
    border-radius: 4px;
}
```

### Progress Bar
```javascript
$(window).scroll(function(){
    var scrollPercent = $(window).scrollTop() / ($(document).height() - $(window).height()) * 100;
    $('.progress-bar').css('width', scrollPercent + '%');
});
```

## 📚 Documentation Links

- **[API_DOCUMENTATION.md](API_DOCUMENTATION.md)** - Complete API reference
- **[COMPONENT_EXAMPLES.md](COMPONENT_EXAMPLES.md)** - Usage examples
- **[README.md](README.md)** - Project overview

---

*Keep this reference handy for quick development tasks!*