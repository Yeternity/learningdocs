# docsify

动态运行时生成html，优雅简洁，速度稍慢。

对比GitBook、Hexo、Docute、VuePress、Nuxt等

## 快速开始

### 安装

```bash
$ npm i docsify-cli -g
```

### 初始化

```bash
$ docsify init 
```

### 生成文件介绍

- `index.html` 入口
- `README.md` 主页
- `.nojekyll` 阻止 GitHub Pages 忽略下划线开头的文件

> 也可以把这三个文件放到docs文件夹外，GitHub Pages 直接从master 分支读取

### 预览

http://localhost:3000

```bash
$ docsify serve
```

> `Ctrl + C` 退出监听

## 个性化配置

通过修改 index.xml

### 搜索

```diff
  <script>
    window.$docsify = {
+     search: 'auto',
    }
  </script>
  <!-- Docsify v4 -->
  <script src="//cdn.jsdelivr.net/npm/docsify@4"></script>
+ <script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>
```

> 存在查找不能定位到小标题的问题，只能到该页面，无法到其中某个标题

### 代码高亮

https://cdn.jsdelivr.net/npm/prismjs@1/components/

```html
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-bash.min.js"></script>
<script src="//cdn.jsdelivr.net/npm/prismjs@1/components/prism-php.min.js"></script>
```

### 侧边栏（自定义目录）

```html
<script>
    window.$docsify = {
      loadSidebar: 'contents.md', // 侧边栏
      auto2top: true,            // 切换页面后是否自动跳转到页面顶部
      subMaxLevel: 3,            // 侧边栏自动生成目录的最大层级（md文件的目录）
      alias: {                   // 嵌套侧边栏
        '/java/.*/contents.md': '/java/contents.md',
        '/leetcode/.*/contents.md': '/leetcode/contents.md',
      },
    }
</script>
```

### 常用配置属性

```html
<head>
  <title>LearningDocs</title>  <!-- 浏览器标签页标题 -->
</head>
<script>
    window.$docsify = {
      name: 'LearningDocs',              // 左侧顶部文档的名字
      repo: 'Yeternity/learningdocs',    // github地址
    }
</script>
```

### 主题

```html
<head>
  <!-- 日夜主题 -->
  <link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify-darklight-theme@latest/dist/style.min.css">
</head>
<body>
  <div id="app"></div>
  <script>
    window.$docsify = {
      darklightTheme: {                  //  日夜主题配置
        defaultTheme: 'light',
        siteFont: 'Source Sans Pro,Helvetica Neue,Arial,sans-serif',
        codeFontFamily: 'Roboto Mono, Monaco, courier, monospace',
        bodyFontSize: '15px',
        dark: {
          background: '#191919',
          highlightColor: '#e96900',
          codeBackgroundColor: '#202020',
          codeTextColor: '#b4b4b4',
        },
        light: {
          highlightColor: '#e96900',
        }
      },
    }
  </script>
  <!-- 日夜主题 -->
  <script src="//cdn.jsdelivr.net/npm/docsify-darklight-theme@latest/dist/index.min.js"></script>
</body>
```



## 部署到 GitHub Pages

项目主页->Settings->Pages->选择main分支->选择从根目录开始渲染（也可以选择从docs文件夹，我把docs删了）

设置好后会自动生成链接 https://yeternity.github.io/learningdocs/

## 自动化



### 图片路径



### Gitee 同步



## 参考

1. [docsify 官网文档](https://docsify.js.org/)

2. [doocs项目实例]( https://github.com/doocs/leetcode/blob/main/index.html)



