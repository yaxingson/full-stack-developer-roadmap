# web-development-roadmap

> 非线性成长

**WebAPI**

## 微前端

## 搜索技巧

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

## web安全

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

## CSRF

- GET型攻击

- POST型攻击

防范: referer头字段、token

## SQL注入

## 文件上传漏洞







