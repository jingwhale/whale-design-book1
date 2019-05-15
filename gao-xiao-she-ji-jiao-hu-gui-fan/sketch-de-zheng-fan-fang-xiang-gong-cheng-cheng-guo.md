# Sketch的正反方向工程成果

<a name="de0f46d9"></a>
### 一、由代码生成sketch
**宗旨：**不做多余的开发，利用现有的技术代码，提高交互设计或是视觉设计的效率。
<a name="86a3f797"></a>
#### 1.1、代码生成sketch文件的需求：
1）、通过组件库，生成设计的组件基础，保证设计组件与技术组件的统一性。

2）、利用技术组件与业务组件，通过配置快速实现智能交互<br />例如：通过配置，快速生成后台“增删查改”交互规范较为统一的交互设计。

3）、代码生成sketch文件，不要有技术的限制，任何Web类组件库都可以<br />例如：支持基于react、react-native、vue、jquery等技术的组件。

4）、使用一些技术组件，能更快的生成流程图、图表、复杂数学公式等复杂图形的绘制。<br />例如：使用[js-code-to-svg-flowchart](https://github.com/Bogdan-Lyashenko/js-code-to-svg-flowchart)生成快速流程图。

<a name="700584c1"></a>
#### 1.2、代码生成sketch文件的原理
代码生成sketch文件的主要需求是利用现有的技术代码，提高交互设计或是视觉设计的效率，并且不受技术限制。

现代Web前端技术开发的库很多，要不受技术限制的生成sketch文件，就要“以终为始”，从sketch文件的制作开始。

sketch文件的制作分为人工设计、重新编写代码生成、以及加载图像设计文件，其中人工设计、重新编写代码生成都不符合需求，只有加载图像设计文件的方向探寻。

这样就确定了研究的初始物与产物：
```
原始的物体：既有组件与业务组件库

目的产物：可载入sketch中的图像设计文件
```

代码与设计文件，是属于2个不同的范畴，需要其中一个向另外一个转化，并且是趋向目性的转化。图像设计文件是必须要的，只有转化代码，代码的表现形式是html（包含css与js的组合）。所以确定由html向设计文件转化。任何组件库都会渲染为dom结构，这样，就没有技术的限制，都可以转化成图像设计文件，加载到sketch中。

经过大量的研究发现，svg文件与sketch文件的图层元素，以及设计概念相近似；<br />sketch支持svg文件的导入与导出；<br />svg文件导入sketch中后，呈现出图层，可以在sketch中编辑修改；<br />以上三点说明svg文件是完美的图像设计文件目标产物。

其实前端技术都知道，SVG 即 Scalable Vector Graphics，是一种用来绘制矢量图的 HTML5 标签。你只需定义好XML属性，就能获得一致的图像元素。并且，它可以通过sketch插件插入sketch中。这，才是最令人兴奋的地方。

好了，一张图说明基础的原理与流程：<br />![屏幕快照 2019-04-23 下午10.38.10.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556030309155-f65af17d-8f68-4bc5-b891-e07f49bc3f2d.png#align=left&display=inline&height=300&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-23%20%E4%B8%8B%E5%8D%8810.38.10.png&originHeight=974&originWidth=600&size=84243&status=done&width=185)<br />

<a name="4286cf1a"></a>
#### 1.3、代码生成sketch文件的实现
**1.3.1、技术调研**<br />代码生成sketch文件，最主要的技术是组件渲染后的html转化成svg文件。

**1）组件渲染后的html转化成svg文件**<br />目前现有技术能实现html2svg，有以下几种：

**第一种：html2canvans->canvans2svg**<br />先把html转化成canvans，再有canvans转化成svg。<br />现有的技术：[html2canvas](https://github.com/niklasvh/html2canvas)，[canvas2svg](https://github.com/gliffy/canvas2svg)等。技术相对比较成熟。

但是，这个缺点比较明显，canvas不能直接转化成svg，现有的技术是同步canvas与svg的建立步骤，这样需要改动，并组合现有组件，开发和维护成本较高。

**第二种，html2image**<br />svg可以看做是一种图像文件，可以直接通过现有的组件[canvas2image](https://github.com/hongru/canvas2image)转化成svg。

但是，这种html2image的技术实现原理是，使用svg的一个特性，在<foreignobject>标签中可以包含任意的html内容。就是将要转换的html包含在svg文件的<foreignobject>标签中，这明显不符合代码生成sketch文件设计的需求，sketch不能识别foreignobject中的html标签。

**第三种，html2svg**<br />直接由html转化成Svg文件。这是最直接的方式，但是前端技术相对较少。

经过研究，发现一个java jar包[webvector](http://cssbox.sourceforge.net/webvector/)，它能将html转化为Svg文件。[webvector](http://cssbox.sourceforge.net/webvector/)简介如下：
```
WebVector is an HTML to SVG or PNG convertor. It converts a HTML document into a 
vector image in SVG format or a bitmap image in PNG format. 

The Standard Vector Graphics (SVG) files can be further edited by a variety of 
vector graphics editors such as Inkscape.
```

调用webvector代码：
```
java -jar webvector-<version>.jar <url> <output_file> <format>
```

```
-<url> is the URL of the page to convert, e.g. http://www.sf.net/ for a website or 
http://C:/myfile.html for a local file.

-<output_file> is the file name where the result will be stored, e.g. myoutput.svg.

-<format> is either svg or png.
```

下图是一个svg图片，由[webvector](http://cssbox.sourceforge.net/webvector/)转化的[button.svg](https://github.com/jingwhale/sketch-document/blob/master/button.svg)：

![button.svg](https://cdn.nlark.com/yuque/0/2019/svg/120638/1556074187744-5b4b72d0-8058-4e45-b873-0a8efd4e8720.svg#align=left&display=inline&height=571&name=button.svg&originHeight=1257&originWidth=1200&size=26505&status=done&width=545)<br />

在sketch中展示如下，可对图层进行编辑：<br />![屏幕快照 2019-04-24 上午11.00.36.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556074885713-fce0a701-50e6-4647-ab8b-65ec1c0d5e75.png#align=left&display=inline&height=453&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-24%20%E4%B8%8A%E5%8D%8811.00.36.png&originHeight=1884&originWidth=3104&size=1190161&status=done&width=746)

**2）html的渲染**<br />调研完代码生成sketch文件，html转化成svg文件的技术。其实，html的渲染也是需要关心的一个重要点。毕竟html转化成svg文件的效果基于html dom的完整性。

html转化成svg文件的前提是，要有完整的html dom（包含样式，以及js作用后的完整dom），这使用后端渲染模板最合适，它将渲染好的dom直接在前端展示。使用Nodejs可以很好的结合组件与业务组件，并且实现模板的渲染。

综上所述，现有的技术方案设计如下：<br />![技术架构.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1556034329662-f3fcc881-3bd0-411e-bbe2-d7be317dfdb0.jpeg#align=left&display=inline&height=250&name=%E6%8A%80%E6%9C%AF%E6%9E%B6%E6%9E%84.jpg&originHeight=453&originWidth=711&size=45370&status=done&width=393)<br />

**1.3.2、实现**<br />**1）、html渲染工程**<br />[**《**](https://github.com/easy-team/egg-react-webpack-boilerplate)[基于 Egg + React + Webpack 多页面和单页面服务器渲染工程骨架项目](https://github.com/easy-team/egg-react-webpack-boilerplate)[**》**](https://github.com/easy-team/egg-react-webpack-boilerplate)<br />[《Egg + React 工程化解决方案》](https://www.yuque.com/easy-team/egg-react)<br />**<br />**2)、htmltosvg工程**<br />[《html2svg》](https://github.com/jingwhale/html2svg)

**3）、流程图等库**<br />流程图：[js-code-to-svg-flowchart](https://github.com/Bogdan-Lyashenko/js-code-to-svg-flowchart)<br />图表：[apexcharts.js](https://github.com/apexcharts/apexcharts.js)<br />数学公式：[MathJax](https://github.com/mathjax/MathJax)<br />内容预加载：[react-content-loader](https://github.com/danilowoz/react-content-loader)，[react-native-svg-animated-linear-gradient](https://github.com/virusvn/react-native-svg-animated-linear-gradient)<br />terminal：[terminal-in-react](https://github.com/nitin42/terminal-in-react)

更多svg开源项目请看[《](https://www.yuque.com/jingwhale/blog/phsyzf)[Svg开源项目列表](https://www.yuque.com/jingwhale/blog/phsyzf)[》](https://www.yuque.com/jingwhale/blog/phsyzf)。

**1.4、Svg文件优化压缩**<br />有时文件比较大，可进行优化压缩。<br />**1）、工程**<br />[https://jakearchibald.github.io/svgomg/](https://jakearchibald.github.io/svgomg/)

**2）、工具**<br />[https://github.com/jakearchibald/svgo](https://github.com/jakearchibald/svgo)

**3）、在线工具**<br />[https://github.com/jakearchibald/svgomg](https://github.com/jakearchibald/svgomg)

<a name="9b7fd457"></a>
### 二、由sketch生成代码
<a name="d3c6feab"></a>
#### 2.1、由sketch生成代码的场景如下：
**1）、sketch UI样式的高效复用**<br />sketch UI样式是视觉设计师，精心设计的，它不差1px，为什么这些样式，还要前端技术再实现一遍？而且还原的亦不一定理想。

**2）、静态页面的专题系统**<br />可以直接输出静态的专题。

**3）、个人网页**<br />可以直接输出静态的个人网站。

**4）、前端组件参考**<br />可以生成react组件，共前端技术，前期的代码基础参考。

<a name="0453e677"></a>
#### 2.2、sketch生成代码产品与技术-[Sketch2React Code App](https://sketch2react.io/)
现在有很多的插件，能都实现sketch文件生成代码，著名的sketch标注插件Sketch Measure，就是一个典型的例子。

开源项目，如：[sketch-to-html](https://github.com/zhaoyueer/sketch-to-html)等。

这里主要介绍[Sketch2React Code App](https://sketch2react.io/)。可以在官网免费注册下载使用。

![屏幕快照 2019-04-24 上午12.13.34.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556036035335-22350a57-de6b-467f-a357-1e0fdc8654be.png#align=left&display=inline&height=223&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-24%20%E4%B8%8A%E5%8D%8812.13.34.png&originHeight=974&originWidth=2390&size=256207&status=done&width=548)

**1）特点如下：**

```
*Never Leave Sketch
You go from design to code components without ever leaving Sketch

*Design Components
Design and style your own components like text, buttons, form fields, navigation

*True React Export
React Vanilla or our version? The choice is yours…

*Design Grids
Since we run Bootstrap 4 in the background you candesign and export real code grids 
to your developers

*Add CSS plugins
Add custom made CSS animations, overrides and effects as easy as 1-2-3

*Fully Responsive Prototypes
A great way to get started learning our framework is to use it for what we call Quick
Responsive Prototyping

*Real Code Constraints
Since you're working withreal code you get real code constraints, which is a great 
thing.

*Export to HTML5
Pump out Bootstrap 4 powered websites for free like there's no tomorrow.Connect 
external CMS for even more awesomeness.

*Styled Components
V2 of our framework and code app will come with aComponent Inspector that outputs Styled Components. Booya.

```

详细的使用说明链接[《Sketch2ReactPocketGuide》](http://whalexplorer.coding.me/sketch-react/guide.pdf)。

**2）、界面如下：**<br />与sketch关联，sketch改动后，展示也会更新。

**Sketch2React Code App显示：**<br />
![屏幕快照 2019-04-24 上午12.21.39.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556036513126-ae1a7db0-5e0a-435d-8bf4-4bdf2b928476.png#align=left&display=inline&height=433&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-24%20%E4%B8%8A%E5%8D%8812.21.39.png&originHeight=1664&originWidth=2870&size=2821179&status=done&width=746)

点击“Download”按钮，可以选择“HTML”、“React”、“Vanilla React”三种代码风格的代码。

**sketch内显示**<br />![屏幕快照 2019-04-24 上午12.24.50.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556036736937-bb5839fa-943d-4557-a319-e05164a2f08c.png#align=left&display=inline&height=453&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-24%20%E4%B8%8A%E5%8D%8812.24.50.png&originHeight=1884&originWidth=3104&size=2914095&status=done&width=746)

**3）、Demo**<br />sketch文件：<br />[《TheJetsetHomeDemo》](https://sketch.cloud/s/aqpaz)

生成Html预览：<br />[《HtmlCode》](http://whalexplorer.coding.me/sketch-react/demos/TheJetsetHomeDemo/HtmlCode/)

Sketch2React Code App生成的React代码：<br />[《ReactCode》](https://dev.tencent.com/u/whalexplorer/p/sketch-react/git/tree/master/demos/TheJetsetHomeDemo/ReactCode)

Sketch2React Code App生成的Vanllina React代码：<br />[《VanllinaReactCode》](https://dev.tencent.com/u/whalexplorer/p/sketch-react/git/tree/master/demos/TheJetsetHomeDemo/VanllinaReactCode)

<a name="5cb796c7"></a>
#### 2.3、sketch生成react-native代码
工程[《](https://github.com/nanohop/sketch-to-react-native)[sketch-to-react-native](https://github.com/nanohop/sketch-to-react-native)[》](https://github.com/nanohop/sketch-to-react-native)可以将sketch生成react-native代码，原理是先由sketch导出svg，再由svg文件转化成react-native代码。

示例如下：<br />1）、选择要转化的图层：<br />![export_instructions.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556074504211-a4bd9eda-92e5-4512-b9c6-c295119c2e0d.png#align=left&display=inline&height=302&name=export_instructions.png&originHeight=1356&originWidth=1998&size=254249&status=done&width=445)

2）、导出为Svg<br />
![export_instructions_2.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556074545820-4e28f9b9-f0eb-404f-82fc-3de0e44c994d.png#align=left&display=inline&height=115&name=export_instructions_2.png&originHeight=250&originWidth=750&size=52842&status=done&width=344)

3）、Svg转化为react-native<br />
![sketch_conversion.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556074563248-6bcb0f76-62e5-434b-ba0d-717b205df2dd.png#align=left&display=inline&height=353&name=sketch_conversion.png&originHeight=900&originWidth=1200&size=109642&status=done&width=470)

更多使用说明，请查看[《](https://github.com/nanohop/sketch-to-react-native/blob/master/README.md)[sketch-to-react-native](https://github.com/nanohop/sketch-to-react-native/blob/master/README.md)[》](https://github.com/nanohop/sketch-to-react-native/blob/master/README.md)。

<a name="PJpTs"></a>
#### [2.4、svgs转化成React components](https://github.com/canvg/canvg)
Example：

```xml
<?xml version="1.0" encoding="UTF-8"?>
<svg
  width="48px"
  height="1px"
  viewBox="0 0 48 1"
  version="1.1"
  xmlns="http://www.w3.org/2000/svg"
  xmlns:xlink="http://www.w3.org/1999/xlink"
>
  <!-- Generator: Sketch 46.2 (44496) - http://www.bohemiancoding.com/sketch -->
  <title>Rectangle 5</title>
  <desc>Created with Sketch.</desc>
  <defs></defs>
  <g id="Page-1" stroke="none" stroke-width="1" fill="none" fill-rule="evenodd">
    <g
      id="19-Separator"
      transform="translate(-129.000000, -156.000000)"
      fill="#063855"
    >
      <g id="Controls/Settings" transform="translate(80.000000, 0.000000)">
        <g id="Content" transform="translate(0.000000, 64.000000)">
          <g id="Group" transform="translate(24.000000, 56.000000)">
            <g id="Group-2">
              <rect id="Rectangle-5" x="25" y="36" width="48" height="1"></rect>
            </g>
          </g>
        </g>
      </g>
    </g>
  </g>
</svg>
```

Run SVGR

```
npx @svgr/cli --icon --replace-attr-values "#063855=currentColor" icon.svg
```

