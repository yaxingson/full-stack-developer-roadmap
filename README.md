# web-development-roadmap

> 非线性成长

**WebAPI**

## 目标

> 便签和定时任务

## 微前端

## Chrome搜索技巧

> 浏览器扩展插件: vimium

[everything](https://www.voidtools.com/zh-cn/support/everything/installing_everything/)

chrome浏览器设置搜索快捷键: `chrome://settings/searchEngines`

```txt
filetype:pdf ***

site:<domain> ***

sunrise:beijing
sundown:beijing

time in beijing

cache:<url>


```

## web网络和安全

### XSS

> 网络钓鱼攻击

- 存储型攻击

- 反射型攻击

```html
<div style="width: expression(alert(0))"></div>

<a href="java
script: alert(0)"></a>

```

```js
String.fromCharCode(34) // "

String.fromCharCode(39) // '

```

防范: 过滤、转义

### CSRF

> cookie

- GET型攻击

- POST型攻击

防范: referer头字段、token

### SQL注入

### 文件上传漏洞

> window系统文件命名规范

防范: 权限防御、随机生成文件名

### 网络设备

#### 交换机

#### 无线AP

#### 路由器

#### 防火墙

### VPN

## 研发流程

> PRD文档

### 重构

> SDK

### 架构

#### 技术选型

#### 设计模式和代码组织

#### 构建和部署

### 自动化

[ledge平台](https://devops.phodal.com/home)

<img src="https://www.delta-n.nl/wp-content/uploads/2019/07/DevOps-Pipeline-800.png" width="500" />

#### 持续集成

#### 持续部署

## Chrome浏览器

[console-importer插件](https://github.com/pd4d10/console-importer)

自定义打印页面样式：

```css
@page {
  size: A3 landscape;
  margin: 3.7cm 2.6cm 3.5cm;

  @bottom-left, @bottom-right {
  
  }

  @bottom-center {

  }
}

@media print {
  div {
    page-break-after: always;
    page-break-inside: avoid;
  }

  a::after {
    content: attr(href);
  }
}

```

```html
<link rel="stylesheet" type="text/css" src="style.css" media="print" />

```

阻止打印当前页面:

```js
window.addEventListener('beforeprint', ()=>{})

window.matchMedia('print').addListener(()=>{

})

```



## 个人技术品牌

> 技术概括分享、博客、书籍和会议文档写作

**画白板和作品集**

> RSS订阅

## 软技能

