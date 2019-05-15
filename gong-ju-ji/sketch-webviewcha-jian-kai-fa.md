# Sketch webView插件开发

相信大家都对Sketch有一定的了解和认识。除了基础的矢量设计功能以外，插件更是让Sketch保持强大的独门秘籍。Sketch开放了第三方插件接口，设计师可以在几百种的插件中轻松找到适合自己工作方式的插件，并且他们都非常容易获得和安装。这里主要介绍使用Javascript API for Sketch开发Sketch插件。

Sketch成为梦想中的“设计师工具箱”。但是每个人都有不同的需求，也许你需要一个我们还没有实现的功能。不要担心：插件已经可以满足您的需求，或者你可以轻松创建一个插件。

## 一、Sketch插件可以做什么？

Sketch中的插件可以做任何用户可以做的事情（甚至更多！）。例如：

| 根据复杂的规则选择文档中的图层 |
| :--- |
| 操作图层属性 |
| 创建新图层 |
| 以所有支持的格式导出资产 |
| 与用户交互（要求输入，显示输出） |
| 从外部文件和Web服务获取数据 |
| 与剪贴板交互 |
| 操作Sketch的环境（编辑指南，缩放等...） |
| 通过从插件调用菜单选项来自动化现有功能 |
| 设计规格 |
| 内容生成 |
| 透视转换 |

## 二、插件简介

Sketch 插件都是 \*.sketchplugin 的形式，其实就是一个文件夹，通过右键显示包内容，可以看到最普通的内部结构式是这样的：

![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-03-12 &#x4E0B;&#x5348;8.23.50.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552393441316-708d19c6-2895-4bae-bea9-8ccdd241f117.png#align=left&display=inline&height=99&name=屏幕快照%202019-03-12%20下午8.23.50.png&originHeight=226&originWidth=1198&size=41539&status=done&width=527)

manifest.json用来声明插件配置信息，commands 定义所有可执行命令，每条 command 有唯一标志符，identifier，menu 定义插件菜单，通过 identifier 关联到执行命令。  
my-commond.js是插件逻辑的实现代码实现文件。

## 三、Javascript API for Sketch

这是Sketch的原型Javascript API。 原生Javascript，Sketch的完整内部结构的一个易于理解的子集。它仍然是一项正在进行中的工作。

Javascript API for Sketch 原理：  
![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552392039065-098a212a-d33a-4b99-9c56-d8b50d8bf574.png#align=left&display=inline&height=211&name=image.png&originHeight=371&originWidth=745&size=58453&status=done&width=424)  


## 四、[开发文档](https://developer.sketchapp.com/)

### 1、开发文档

[https://developer.sketchapp.com/](https://developer.sketchapp.com/)

### 2、API

[https://developer.sketchapp.com/reference/api/](https://developer.sketchapp.com/reference/api/)

### 3、Action API

[https://developer.sketchapp.com/guides/action-api/](https://developer.sketchapp.com/guides/action-api/)  
[https://developer.sketchapp.com/reference/action/](https://developer.sketchapp.com/reference/action/)

### 4、Sketch Source

[https://github.com/BohemianCoding/SketchAPI/tree/develop/Source](https://github.com/BohemianCoding/SketchAPI/tree/develop/Source)

### 5、Demo

[https://github.com/BohemianCoding/SketchAPI/tree/develop/examples](https://github.com/BohemianCoding/SketchAPI/tree/develop/examples)

## 五、[Sketch webView](https://github.com/skpm/sketch-module-web-view)

Sketch模块，用于使用webview创建复杂的UI。有别于一般的插件页面，可以使用webview模块加载一个复杂的Web应用，使其与Sketch进行交互。 

### [1、BrowserWindow](https://github.com/skpm/sketch-module-web-view/blob/master/docs/browser-window.md)

在浏览器窗口中创建和控制Sketch：

```javascript
// In the plugin.
const BrowserWindow = require('sketch-module-web-view');
const identifier = "identifier";//webview 标识

let win = new BrowserWindow({identifier, width: 800, height: 600, alwaysOnTop: true})
win.on('closed', () => {
  win = null
})

// Load a remote URL
win.loadURL('https://github.com')

// Or load a local HTML file
win.loadURL(require('./index.html'))
```

### 2、获取已存在的BrowserWindow

```javascript
import { getWebview } from 'sketch-module-web-view/remote';
const = identifier = "identifier";

const existingWebview = getWebview(identifier);
if (existingWebview) {
  if (existingWebview.isVisible()) {
  // close the devtool if it's open
    existingWebview.close()
  }
}
```

### 3[、webContents](https://github.com/skpm/sketch-module-web-view/blob/master/docs/web-contents.md)

```javascript
const BrowserWindow = require('sketch-module-web-view')

let win = new BrowserWindow({ width: 800, height: 1500 })
win.loadURL('http://github.com')

let contents = win.webContents
console.log(contents)
```

### 4[、skech与webview的通信](https://github.com/skpm/sketch-module-web-view/blob/master/docs/communication-plugin-webview.md)

1）Sending a message to the WebView from your plugin command  
On the WebView:

```javascript
window.someGlobalFunctionDefinedInTheWebview = function(arg) {
  console.log(arg)
}
```

On the plugin:

```javascript
browserWindow.webContents
  .executeJavaScript('someGlobalFunctionDefinedInTheWebview("hello")')
  .then(res => {
    // do something with the result
  })
```

2）Sending a message to the plugin from the WebView  
On the plugin:

```javascript
var sketch = require('sketch')

browserWindow.webContents.on('nativeLog', function(s) {
  sketch.UI.message(s)
})
```

On the webview:

```javascript
window.postMessage('nativeLog', 'Called from the webview')

// you can pass any argument that can be stringified
window.postMessage('nativeLog', {
  a: b,
})

// you can also pass multiple arguments
window.postMessage('nativeLog', 1, 2, 3)
```

## [六、构建开发工程](https://github.com/jingwhale/sketch-webview-kit)

### 1、确立技术栈

使用[Sketch webView](https://github.com/skpm/sketch-module-web-view)的方式开发插件。用户通过操作插件界面，webview与Sketch通信解决用户的问题。这样插件界面可以使用现今所有的前端框架与组件库。  
1）[webView](https://github.com/skpm/sketch-module-web-view)框架选择[Umi ](https://umijs.org/zh/guide/)+ [Ant Design](https://ant.design/index-cn)  
注：WebView框架也可以单独的工程与部署。

2）使用Sketch 官方skpm插件工程

[3）调试工具](https://github.com/skpm/sketch-dev-tools)  
A、使用官方的[**sketch-dev-tools**](https://github.com/skpm/sketch-dev-tools) ****sketch内作为调试工具  
下载代码，代码运行安装插件即可：

```text
npm install
npm run build
```

调试界面如下：  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-03-19 &#x4E0B;&#x5348;2.21.17.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552976510855-f9639c89-04bb-4c05-8abb-f099b4ab63eb.png#align=left&display=inline&height=430&name=屏幕快照%202019-03-19%20下午2.21.17.png&originHeight=1650&originWidth=2862&size=630583&status=done&width=746)

B、使用浏览器的开发者模式调试[webView](https://github.com/skpm/sketch-module-web-view)。  
在sketch webView中右击显示调试器即可：![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-03-12 &#x4E0B;&#x5348;9.34.10.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552397733159-b8ac6ca0-5315-42a2-a3dc-6fb49b1a4d8d.png#align=left&display=inline&height=417&name=屏幕快照%202019-03-12%20下午9.34.10.png&originHeight=1524&originWidth=2728&size=769588&status=done&width=746) 

4）服务端技术方案  
[轻量级服务器部署方案 -（阿里云CenOS+宝塔）](https://www.cnblogs.com/jingwhale/p/10659357.html) 

### 2、构建工程

1\)创建Sketch插件基础工程  
首先，创建sketch-webview-kit插件工程：

```bash
npm install -g skpm
skpm create sketch-webview-kit //创建sketch-webview-kit插件工程
```

其次，依赖sketch-module-web-view：

```text
npm install sketch-module-web-view
```

2）创建webView工程（[Umi ](https://umijs.org/zh/guide/)+ [Ant Design](https://ant.design/index-cn)）  
首先，创建webView工程目录，

```bash
$ mkdir webapp && cd webapp
```

然后，创建webView工程

```bash
yarn create umi
```

依次：  
选择 app, 然后回车确认；  
选上 antd 和 dva，然后回车确认；

最后，安装依赖：

```text
$ yarn
```

3）配置webView工程  
[A.部署打包配置](https://umijs.org/zh/guide/deploy.html#静态化)  
.umirc.js文件中，添加：

```javascript
outputPath:'../src/dist', //打包后的目录
exportStatic: {
  htmlSuffix: true,
    dynamicRoot: true //静态自由部署
},
```

[B.HTML 模板](https://umijs.org/zh/guide/html-template.html)  
由于Umi生成没有Html文件，可以自己配置。新建 src/pages/document.ejs，umi 约定如果这个文件存在，会作为默认模板，内容上需要保证有 ，比如：

```markup
<!doctype html>
<html>
<head>
  <meta charset="utf-8" />
  <title>Your App</title>
</head>
<body>
  <div id="root"></div>
</body>
</html>
```

C.添加新页面  
直接在pages文件夹下建立页面的js与css样式文件即可。

D.[《基于 umi 的 React 项目结构介绍》](https://www.jianshu.com/p/0b536e66ac61)

### 3、sketch加载webView工程与联调

1）sketch加载webView  
第一种方法：  
直接部署webView工程，通过Url加载：

```javascript
win.loadURL('https://github.com')
```

第二种方法：  
加载webView工程打包后的文件：

```javascript
win.loadURL(require('./dist/index.html'))
```

**注意：**  
此方法，由umi打包后的静态资源（css、js）需要拷贝到  
pannel3/pannel3.sketchplugin/Contents/Resources/\_webpack\_resources下。

2）联调加载方法：  
本地启动webView工程，本地webView工程会在8000端口起一个服务，加载此服务即可：

```javascript
const Panel = `http://localhost:8000#${Math.random()}`;
win.loadURL(Panel)
```

### [4、项目成果](https://github.com/jingwhale/sketch-webview-kit)

文件目录如下：  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-03-12 &#x4E0B;&#x5348;9.38.58.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552397948059-2d1431ea-e8d1-44a0-93e8-0231085dc953.png#align=left&display=inline&height=675&name=屏幕快照%202019-03-12%20下午9.38.58.png&originHeight=1342&originWidth=716&size=150177&status=done&width=360)

## 七、发布sketch 插件

前提确保manifest.json的version参数已经修改为想要发布的版本。

```javascript
{
  "name": "Whale Kit",
  "identifier": "whale-sketch-webview-kit",
  "description": "A quick prototype tool library for sketch. ",
  "author": "jingwhale",
  "authorEmail": "jingwhale@yeah.net",
  "compatibleVersion": 3,
  "bundleVersion": 1,
  "icon": "icon.png",
  "version": "0.4.3",
  "commands": [
    {
      "name": "Efficient design spec",
      "identifier": "sketch-webview-kit.my-command",
      "script": "whaleHomepage.js"
    },
    {
      "name": "Make Layout",
      "identifier": "sketch-webview-kit.my-command2",
      "script": "makeLayoutCommand.js",
      "shortcut" : "shift control a"
    },
    {
      "name": "Generate Button",
      "identifier": "sketch-webview-kit.my-command3",
      "script": "generateButtonCommand.js",
      "shortcut" : "shift control z"
    },
    {
      "name": "Operate Image",
      "identifier": "sketch-webview-kit.my-command4",
      "script": "operateImageCommand.js",
      "shortcut" : "shift control q"
    },
    {
      "name": "Flow Page",
      "identifier": "sketch-webview-kit.my-command5",
      "script": "flowPageCommand.js",
      "shortcut" : "control option shift p"
    },
    {
      "name": "Screen Shot",
      "identifier": "sketch-webview-kit.my-command6",
      "script": "screenshotCommand.js",
      "shortcut" : "control option shift j"
    },
    {
      "name": "Toggle State",
      "identifier": "sketch-webview-kit.my-command7",
      "script": "toggleStateCommand.js",
      "handler" : "onRun",
      "shortcut" : "control option shift k"
    },
    {
      "name": "Convert to Grayscale",
      "identifier": "sketch-webview-kit.my-command8",
      "script": "convertToGrayscaleCommand.js",
      "handler" : "onRun",
      "shortcut" : "control option shift g"
    },
    {
      "name": "Generate QR Code",
      "shortcut": "ctrl shift option q",
      "identifier": "sketch-webview-kit.my-command9",
      "script": "generateQrcode.js",
      "handler" : "onRun"
    },
    {
      "name": "Generate Cover",
      "shortcut": "ctrl shift option c",
      "identifier": "sketch-webview-kit.my-command10",
      "script": "generateCover.js",
      "handler" : "onRun"
    },
    {
      "name": "Generate Radar Chart",
      "shortcut": "ctrl shift option f",
      "identifier": "sketch-webview-kit.my-command11",
      "script": "generateRadarChart.js",
      "handler" : "onRun"
    },
    {
      "name": "Generate Tags",
      "shortcut": "ctrl shift option t",
      "identifier": "sketch-webview-kit.my-command12",
      "script": "generateTags.js",
      "handler" : "onRun"
    },
    {
      "name": "Generate Signifiers",
      "shortcut": "ctrl shift option s",
      "identifier": "sketch-webview-kit.my-command13",
      "script": "generateSignifiers.js",
      "handler" : "onRun"
    }
  ],
  "menu": {
    "title": "Whale Kit",
    "items": [
      "sketch-webview-kit.my-command",
      "-",
      "sketch-webview-kit.my-command2",
      "sketch-webview-kit.my-command3",
      "sketch-webview-kit.my-command4",
      "sketch-webview-kit.my-command7",
      "-",
      "sketch-webview-kit.my-command12",
      "sketch-webview-kit.my-command13",
      "-",
      "sketch-webview-kit.my-command6",
      "sketch-webview-kit.my-command8",
      "sketch-webview-kit.my-command9",
      "-",
      "sketch-webview-kit.my-command5",
      "sketch-webview-kit.my-command10"
    ]
  }
}
```

**首先，**需要把你的插件代码放到 Github仓库；

**其次，**使用开通[GitHub Token](https://help.github.com/en/articles/creating-a-personal-access-token-for-the-command-line)；  
因为，skpm需要一个GitHub令牌才能发布版本，需要`repo`权限才能创建版本。  
设置完后，使用命令：

```text
skpm login
```

将GitHub Token填进去，回车即可。

**最后，**使用命令，等待发布完成即可：

```text
skpm publish <bump>
```

bump为patch, minor, or major其中之一，分别表示补丁，小改，大改

```text
若是patch，变为1.0.1

若是minor，变为1.1.0

若是major，变为2.0.0
```

一旦你的插件被发布，它就会在sketch进行新的部署时出现在[sketch插件官网](https://www.sketch.com/extensions/plugins/)上（可能需要几分钟到几天），部署成功后，可以在[sketch插件官网](https://www.sketch.com/extensions/plugins/)查看发布的插件。

## 八、拓展

### [1、](https://www.yuque.com/jingwhale/blog/rt5aci)[React - SketchApp ](https://github.com/airbnb/react-sketchapp)

是一个开源库，为设计系统量身定制。它通过将 React 元素渲染到 Sketch 来连接设计和开发之间的鸿沟。  
Sketch Javascript API 是源生代码，React - SketchApp 使用react对Javascript API 进行了二次封装。  
[1\)API](http://airbnb.io/react-sketchapp/docs/API.html)  
[http://airbnb.io/react-sketchapp/docs/API.html](http://airbnb.io/react-sketchapp/docs/API.html)

[2\)Demo](https://www.yuque.com/jingwhale/blog/do37mc)  
[https://www.yuque.com/jingwhale/blog/do37mc](https://www.yuque.com/jingwhale/blog/do37mc)

