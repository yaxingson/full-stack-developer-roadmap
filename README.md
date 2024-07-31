# web-development-roadmap

> 非线性成长

**WebAPI**

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

## 个人品牌

> 技术概括分享、博客、书籍和会议文档写作


