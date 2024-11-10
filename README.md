 # web-development-roadmap

> 非线性成长

**WebAPI**

技术栈分级: 框架和库  -->  语言和平台  -->  模式和思想  -->  软能力

## 目标和方法论

> 便签和定时任务

**领域知识（通用和专用）**

知识体系和系统学习：

- 整理法(脑图): 顺序关系、组合关系、维度关系和分类关系
- 追溯(追本溯源)法：论文、邮件列表讨论和代码提交记录

[whatwg](https://whatwg.org/)

[ecma-262](https://262.ecma-international.org/15.0/index.html)

无障碍富互联网应用（Accessible Rich Internet Applications，ARIA）

> UMD模块化

[browserslist](https://browsersl.ist/)

> 经验性知识和原理性知识

能力模型和知识地图

站点地图


> V8垃圾回收

RFC文档


## 微前端

<https://single-spa.js.org/>

<https://qiankun.umijs.org/zh>

> 沙箱技术和容器化技术


## 云服务

> 服务端接入层、分布式架构和同构网络

```js
const cluster = require('node:cluster')
const numCPUs = require('node:os').availableParallelism()

if(cluster.isPrimary) {

 cluster.on('exit', ()=>{
  
 })
} else {

}

```

云存储: 对象存储(OSS)和文件存储(NAS)

[七牛云](https://www.qiniu.com/)

> FaaS(Function As A service，函数即服务)和BaaS(Backend As A Service, 后端即服务)

web应用架构:

- 单体架构

- 微服务架构

> 领域驱动设计(DDD)和职责驱动设计(RDD)


## AI助手


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

![](https://img.picui.cn/free/2024/09/27/66f6afc816a46.png)

<http://test-ipv6.com/>

相关概念:

- 局域网和公网
- 网关
- 子网

回环地址: `127.0.0.1`、`::1` 或 `localhost`

> TCP/IP四层模型

[域名注册商](https://www.cloudflare-cn.com/)

DNS服务的端口号: TCP/UDP 53

DNS缓存：浏览器缓存 -> 操作系统缓存 -> 路由器缓存 -> ISP缓存

> 浏览器内置预加载`HSTS`列表

<img src="https://img.picui.cn/free/2024/09/17/66e96cdf78e8b.png" width="80%" />


```sh
nc 92.168.19.10 80

# -i 显示响应头
# -v 显示详细信息
# -X 指定请求方法
# -d 指定请求体
curl "https://httpbin.org/post" -i -v -X POST -d "username=rose"

ping6 -c 4 fe80::f2de:f1ff:fe3f:307e

nslookup -query=txt www.baidu.com

```

> Dos攻击和中间人攻击

B/S架构通信: 

- 轮询
- `websocket`全双工

与websocket通信相关的HTTP头字段:

- `Upgrade`
- `Connection`
- `Sec-Websocket-Key`
- `Sec-Websocket-Version`
- `Sec-Websocket-Extensions`

> 心跳机制


### XSS

> 网络钓鱼攻击

- 存储型攻击

- 反射型攻击

```html
<script src="https://polyfill.io/v3/polyfill.min.js?features=es2022"></script>
<div style="width: expression(alert(0))"></div>

<a href="java
script: alert(0)"></a>

```

```js
String.fromCharCode(34) // "

String.fromCharCode(39) // '

Object.freeze()

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

> TLS证书和CA、mTLS

## 研发流程

主流的软件开发模式:

- 瀑布模式
- 迭代增量模式
- 螺旋模式
- **敏捷开发**模式

> 数据（状态数据和动态数据）驱动设计

### 背景与调研

项目排期和复盘


### 排版和设计

`UI Design`工具和设计稿

```css
@media screen and (-webkit-min-device-pixel-ratio: 2) {

}

```

> webview和jsbridge

JS与移动端原生语言通信：

- Android

```java
webView = new WebView(this);

// android version < 4.4 
webView.loadUrl("javascript: function_name(params)");

runOnUiThread(new Runnable(){
	@Override
	public void run() {
		webView.loadUrl("");

	}
})

// android version >= 4.4
webView.evaluateJavascript("javascript: function_name(params)", new ValueCallbak() {
	@Override
	public void onReceiveValue(String value) {

	}
})

```

```java
// inject global object
Object getJSBridge() {
	Object innerObj = new Object() {
		@JavascriptInterface
		public String bar() {

		}

		@JavascriptInterface
		public String foo() {

		}
	};

	return innerObj; 
}

WebSettings settings = webView.getSettings();

settings.setJavascriptEnabled(true);

webView.addJavascriptInterface(getJSBridge(), "JSBridge");

```

- IOS

> `URL Scheme`


#### 原型设计

原型图和线框图

> 泳道图

产品需求文档（PRD）

- 战略: 产品定位、目标市场和用户画像以及竞品等
- 战术: 产品结构、核心业务流程、具体用例描述、功能&内容描述等

组成要素:

- 命名、编号
- 历史版本、修订记录和目录
- 引言（产品背景、产品规划和名词解释）
- 需求概述
- 功能性需求说明
- 非功能描述（性能需求、运营需求和风险分析）

> MRD（市场需求文档）和 BRD（商业需求文档）

#### UI设计

> canvas截图和暗水印


#### 交互设计


#### API设计

API: 一组用于构建和集成应用程序的定义和协议

> SOAP（Single Object Access Protocol）协议和rpc（Remote Procedure Call）技术机制


- [grpc](https://grpc.io/)

- [trpc](https://trpc.io/)

> Protocol Buffers


### 重构

> SDK

### 架构

BFF(Backends For Frontends，服务于前端的后端)

> JAM(Jamstack, JavaScript、API & Markup)架构和微内核架构

元框架

> `multirepo` vs. `monorepo`


#### 技术选型

#### 设计模式和代码组织

#### 构建和部署

> 灰度发布和快速回滚


### 测试

> 回归测试、冒烟测试

#### 单元测试

单元测试框架: 基础类库 + 测试运行器

> 测试覆盖率和`Snapshot`快照测试

```js
// support async function test

test('', (done)=>{
 expect.assertions(1)

 const callback = ()=>{
   done()
 }
 
))

test('', ()=>{
 expect.assertions(1)

 return fn().then((res)=>{
  
 })
))

test('', async ()=>{
 expect.assertions(1)

 await fn()
 
))

```

```sh
jest --coverage

# snapshot测试的结果需要随着源代码一起提交
jest --updateSnapshot

```


#### e2e测试

> headless chrome 

#### UI测试


#### api测试


### 自动化

[ledge平台](https://devops.phodal.com/home)

<img src="https://www.delta-n.nl/wp-content/uploads/2019/07/DevOps-Pipeline-800.png" width="500" />

#### 持续集成

#### 持续部署

> 灰度发布

## 性能

> 垃圾回收、时间切片(Time Slicing)和Bundleless

用户体验指标:

- `TTI`
- `FID`
- `TBT`
- `FP`
- `FCP`
- `LCP`
- `CLS`

获取用户数据指标的方式: Devtools、[Lighthouse](https://github.com/GoogleChrome/lighthouse)、浏览器插件和PerformanceAPI

第三方CDN服务平台:

- [jsdelivr](https://www.jsdelivr.com/)
- [unpkg](https://unpkg.com/)
- [cdnjs](https://cdnjs.com/)

懒加载:

```js
const intersectionObserver = new IntersectionObserver((entries) => {
  if (entries[0].intersectionRatio <= 0) return

  // TODO ...

})

intersectionObserver.observe(document.querySelector(".scrollerFooter"))

```

```html
<meta name="referrer" content="no-referrer" />

```

> Gzip压缩

接口性能优化：

- 关键指标:
  - QPS（每秒查询）
  - TPS（每秒事务）
  - RT（响应时间）

- 优化手段:
  - 批量
  - 异步
  - 空间换时间

浏览器缓存策略: 

- 强缓存
 
- 协商缓存

和浏览器缓存相关的请求和响应头:

 - `Expires` 
 - `Cache-Control`
 - `If-Modified-Since`
 - `Last-Modified`
 - `Etag`
 - `If-None-Match`

```js
window.chrome.loadTimes()


```

> DNS预解析

白屏和无样式内容闪烁

```html
<img src="" alt="" loading="lazy">

```
 
### 代码质量

> 富客户端

提升用户体验的方法:

- 及时反馈和提示
- 兜底措施

### 工程化

> 工具链(toolchain)包括: parser、transformer、resolver、 linter、formatter和minifier等

**AI赋能**和**定制化脚手架**

```sh
npm link

```

### Ajax

> REST(REpresentational State Transfer, 表现层状态转换)

- [XMLHttpRequest](https://developer.mozilla.org/zh-CN/docs/Web/API/XMLHttpRequest)

- [fetch](https://developer.mozilla.org/zh-CN/docs/Web/API/fetch)

## 编译原理

<https://astexplorer.net/>


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

## 标准和规范

<https://tc39.es/>

<https://www.w3.org/>


## 国际化

> 本地化和全球化


## Git & Github

Git工作流

> github copilot 

```sh
git diff 

git rm --cached

git mv 

git check-ignore -v file
git chery-pick <commitHash> 

git log --stat --all -n3

git show <id>

git show-branch

git add -A
git commit --amend --no-edit
git push origin --delete main 

git rebase

git stash save
git stash pop

git clone --depth=1

git config core.hooksPath <path>

git help --web log

gitk

```

[.gitignore模板](https://github.com/github/gitignore)

[commit message规范](https://www.ruanyifeng.com/blog/2016/01/commit_message_change_log.html)

[semver规范](https://semver.org/lang/zh-CN/)

> 裸版本库

## 开源

> 开源(open source) vs. 自由(free)

[github1s](https://github1s.com/)

**费曼学习法**

解决Github托管平台的DNS服务器污染问题:

- 更新DNS服务器（`223.5.5.5`或`223.6.6.6`）
- 配置本地静态映射hosts

```txt
140.82.112.3 github.com
140.82.112.3 www.github.com
199.232.68.133 raw.github.com

```

[在线域名ip查询](https://www.ipaddress.com/ip-lookup)

<https://github.com/search/advanced>

> github cli

开源许可证(LICENSE):

- GPL
- Unlicense

<https://creativecommons.org/share-your-work/cclicenses/>
<https://creativecommons.org/licenses/by/4.0/legalcode.txt>

### issue

> good-first-issue

### pull request

```sh
git commit -s -m <message>

git cherry-pick id

```

> 代码评审（code review）和复盘

### wiki

### discussion


## 个人技术品牌

> 技术概括分享、博客、书籍和会议文档[^1]写作

**画白板和作品集**

> RSS订阅和技术影响力

Markdown规范:

- [CommonMark规范](https://spec.commonmark.org/0.31.2/)
- [Github规范](https://github.github.com/gfm/)
- [Typora规范](https://support.typora.io/)

```sh
# 安装markdown解析器
npm i markdown-it -D

find path -name pattern

hexdump file -C -n 1024

2 > file

& > file

```

<https://www.tablesgenerator.com/>

<https://ohmyz.sh/>

<https://explainshell.com/>

<https://imagemagick.org/script/download.php>

> 播客和个人订阅号

**数字花园**

<https://flomoapp.com/>

> 视觉笔记（抽象化和具象化）


## 软技能

<https://www.oreilly.com/>

> 自驱和刻意练习（目标和反馈）

### 英文

--- 

[^1]: 略...

