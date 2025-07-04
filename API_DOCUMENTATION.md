# 🔧 Comprehensive API Documentation

## 📋 Overview

This documentation covers all public APIs, functions, and components for **Wangzhao.GitHub.io** - a personal blog website built with GitHub Pages using the Time Machine theme.

**Site URL**: https://faxiubite.github.io/blog/  
**Repository**: https://github.com/faxiubite/wangzhao.github.io  
**Theme**: Time Machine by Jon Rohan  

---

## 📁 File Structure

```
wangzhao.github.io/
├── index.html                 # Main webpage
├── README.md                  # Project documentation  
├── params.json               # Site configuration
├── images/                   # Static assets
│   ├── code.png
│   ├── pattern.png
│   ├── tar.png
│   ├── top.png
│   └── zip.png
├── javascripts/
│   └── script.js            # Interactive functionality
└── stylesheets/
    ├── stylesheet.css       # Main styling
    └── github-dark.css      # Code syntax highlighting
```

---

## 🎯 JavaScript APIs

### Core Functions

#### 1. Code Line Number Generator

**Function**: Automatic line numbering for code blocks

```javascript
$("pre").each(function(){
    var pre = $(this).text().split("\n");
    var lines = new Array(pre.length+1);
    // ... line numbering logic
    $(this).before("<pre class='lines'>" + lines.join("\n") + "</pre>");
});
```

**Purpose**: Adds line numbers to all `<pre>` code blocks on the page  
**Dependencies**: jQuery 1.7.1+  
**Auto-executed**: Yes (on document ready)

**Features**:
- Handles line wrapping at 70 characters
- Removes empty final lines
- Creates numbered line display

---

#### 2. Navigation System

**Function**: Dynamic header-based navigation

```javascript
var headings = [];
var collectHeaders = function(){
    headings.push({
        "top": $(this).offset().top - 15,
        "text": $(this).text()
    });
}
```

**Purpose**: Creates floating navigation based on page headers  
**Dependencies**: jQuery 1.7.1+  
**Auto-executed**: Yes (on document ready)

**API Methods**:

| Method | Description | Parameters |
|--------|-------------|------------|
| `collectHeaders()` | Gathers header positions and text | `this` (DOM element) |
| `$(window).scroll()` | Updates navigation on scroll | None |
| `$(".current-section a").click()` | Handles scroll-to-top | None |

**Configuration**:
- Supports H1, H2, H3 headers (in priority order)
- 15px offset for better positioning
- Automatic visibility toggle

---

#### 3. Scroll-to-Top Functionality

**Function**: Smooth page navigation

```javascript
$(".current-section a").click(function(){
    $(window).scrollTop(0);
    return false;
})
```

**Purpose**: Provides quick return to page top  
**Trigger**: Click on navigation area  
**Behavior**: Instant scroll to top, prevents default link behavior

---

## 🎨 CSS Components

### Layout Components

#### 1. Main Wrapper

**Class**: `.wrapper`

```css
.wrapper {
    width: 675px;
    margin: 0 auto;
}
```

**Purpose**: Centers main content with fixed width  
**Responsive**: No (fixed layout)

---

#### 2. Container

**Class**: `#container`

```css
#container {
    border: 1px solid #2a2a2a;
    background: #ddd url(../images/pattern.png);
    box-shadow: 0 0 5px #b1b1b1;
}
```

**Purpose**: Main content container with styled background  
**Features**: Pattern background, border, shadow effects

---

#### 3. Header Section

**Class**: `h1.title`

```css
h1.title {
    margin: 30px 20px 10px;
    font-size: 60px;
    font-weight: bold;
    font-style: italic;
    font-family: Georgia, serif;
    text-align: center;
}
```

**Purpose**: Site title styling  
**Font**: Georgia serif, 60px, bold italic

---

### Interactive Components

#### 1. Current Section Navigator

**Class**: `.current-section`

```css
.current-section {
    position: fixed;
    top: 50%;
    right: 20px;
    /* ... additional styling */
}
```

**Purpose**: Fixed navigation element  
**Position**: Right side, vertically centered  
**Behavior**: Shows/hides based on scroll position

**Sub-components**:
- `.current-section .name` - Current section title
- `.current-section a` - Action buttons (scroll, download)

---

#### 2. Download Bar

**Class**: `.download-bar`

```css
.download-bar {
    background: #222;
    border: 5px solid #444;
    padding: 10px;
    margin: 0 -35px 20px;
    position: relative;
}
```

**Purpose**: GitHub repository links and actions  
**Features**: Dark theme, negative margins for full-width effect

---

### Content Styling

#### 1. Markdown Body

**Class**: `.markdown-body`

```css
.markdown-body h1, .markdown-body h2, .markdown-body h3 {
    font-family: Georgia, serif;
    font-weight: normal;
    /* ... additional styling */
}
```

**Purpose**: Styles for markdown-rendered content  
**Supports**: Headers, paragraphs, lists, tables, code blocks

**Features**:
- Typography hierarchy
- Code syntax highlighting
- Table styling
- List formatting

---

#### 2. Code Blocks

**Classes**: `.markdown-body pre`, `.markdown-body pre.lines`

```css
.markdown-body pre {
    background: #f8f8ff;
    border: 1px solid #dedede;
    /* ... additional styling */
}

.markdown-body pre.lines {
    color: #afafaf;
    /* ... line number styling */
}
```

**Purpose**: Code block styling with line numbers  
**Features**: Background colors, borders, line number support

---

## ⚙️ Configuration API

### Site Parameters

**File**: `params.json`

```json
{
    "name": "Wangzhao.GitHub.io",
    "tagline": "法修的个人博客", 
    "body": "# wangzhao.github.io\r\n## 法修的个人博客\r\n...",
    "note": "Don't delete this file! It's used internally to help with page regeneration."
}
```

**Parameters**:

| Parameter | Type | Description | Example |
|-----------|------|-------------|---------|
| `name` | String | Site title | "Wangzhao.GitHub.io" |
| `tagline` | String | Site subtitle | "法修的个人博客" |
| `body` | String | Main content (markdown) | Markdown formatted text |
| `note` | String | Internal usage note | Warning message |

**Usage**: GitHub Pages uses this for automatic page regeneration

---

## 📚 Usage Instructions

### Adding New Content

1. **Edit HTML Content**:
   ```html
   <article class="markdown-body">
       <h2>Your new content here</h2>
       <p>Content description...</p>
   </article>
   ```

2. **Update Configuration**:
   ```json
   {
       "name": "Your Site Name",
       "tagline": "Your tagline",
       "body": "Updated markdown content"
   }
   ```

### Customizing Styles

1. **Modify Colors**:
   ```css
   /* In stylesheet.css */
   a { color: #your-color; }
   ```

2. **Update Layout**:
   ```css
   .wrapper { width: your-width; }
   ```

### Adding New JavaScript Features

1. **Extend Existing Functions**:
   ```javascript
   $(document).ready(function(){
       // Your custom code here
       // Use existing patterns for consistency
   });
   ```

---

## 🔗 Dependencies

### External Libraries

| Library | Version | CDN URL | Purpose |
|---------|---------|---------|---------|
| jQuery | 1.7.1 | https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js | DOM manipulation |

### Internal Dependencies

- `stylesheets/stylesheet.css` - Main styling
- `stylesheets/github-dark.css` - Code highlighting
- `images/pattern.png` - Background texture
- `javascripts/script.js` - Interactive functionality

---

## 🚀 Development Guidelines

### Code Standards

1. **JavaScript**:
   - Use jQuery for DOM manipulation
   - Wrap code in `$(document).ready()`
   - Follow existing naming conventions

2. **CSS**:
   - Use class-based selectors
   - Maintain existing color scheme
   - Follow BEM-like naming for new components

3. **HTML**:
   - Maintain semantic structure
   - Use existing class names for consistency
   - Keep accessibility in mind

### Performance Considerations

- Images are optimized for web
- CSS is concatenated in single file
- JavaScript is minimized
- CDN used for jQuery

---

## 🐛 Troubleshooting

### Common Issues

1. **Line numbers not showing**:
   - Check jQuery is loaded
   - Verify `<pre>` tags exist
   - Check console for JavaScript errors

2. **Navigation not working**:
   - Ensure headers (H1, H2, H3) exist
   - Check scroll event binding
   - Verify `.current-section` CSS

3. **Styling issues**:
   - Check CSS file paths
   - Verify image URLs
   - Clear browser cache

### Browser Support

- **Supported**: Chrome, Firefox, Safari, Edge
- **Minimum**: IE 8+ (with limitations)
- **Mobile**: Basic support (not responsive)

---

## 📄 License

This project uses the MIT License. See `LICENSE` file for details.

---

## 🤝 Contributing

1. Fork the repository
2. Create feature branch
3. Make changes following guidelines above
4. Test across browsers
5. Submit pull request

---

*Last updated: [Current Date]*  
*Documentation version: 1.0.0*