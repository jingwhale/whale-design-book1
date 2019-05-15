# 高效设计交互规范库

高效设计交互规范库由两部分组成，一是原型设计库，它使用插件技术固化某些交互，提高交互设计的效率；二是UI 设计库，基于市面上常用的UI库组成，是UI规范的最核心的固化产物。

主旨：Work Smart，Think more，Do Less，Get More。

<a name="95642182"></a>
## 一、原型设计库
<a name="6435e790"></a>
### 1.1、智能快速原型库
智能快速原型库是弱规范原型库，由Whale Kit插件库和FusionCool插件组成，注重原型设计的效率，不强限制规范。

Whale Kit主要负责布局与特定交互业务。它是一个基于高效设计理念的快速原型工具，基于Sketch开发。它包含两部分：一是 Base Components，包含原型最基础的组件；二是交互业务，如自动添加修订记等。特点是，能够快速的构建基础交互原型。详情请查看[《Whale Kit》](https://www.yuque.com/jingwhale/blog/hdvuwz)。

FusionCool主要是负责原型组件。嵌入式面板,如影随形。组件直接拖拽使用，令人震惊的组件编辑能力。其次，负责一些常用的复杂模板的管理。具有较强的整合设计资源能力。详情请查看[《](https://fusion.design/18642/)[Whale Design](https://fusion.design/18642/)[》](https://fusion.design/18642/)。

可以使用Axure元件库，[Axure原型库实现快速原型设计。](https://www.yuque.com/jingwhale/blog/rz1qzi)

<a name="77dd2161"></a>
### 1.2、Symbols GrayScale原型库
Symbols GrayScale原型库是强规范原型库，注重规范与效率，限制每个组件的规范。

Symbols GrayScale原型库实际上是一种Sketch交互设计原型库的解决方案，它包括基础一套基础原型设计库，一个原型库插件和一个动态原型设计组件库。原型库插件可以动态的将现有的视觉Symbols 库转化为原型设计库。

<a name="d3c530d3"></a>
#### 1.2.1、一套交互设计原型Whale Template
基于Ant Design的组件库，保持实时更新。

<a name="ab6e0b66"></a>
#### 1.2.2、原型库插件Convert to GrayScale
它可以将目前所有的Sketch组件库的symbols转化成交互色原型symbols，它的工作原理是将既有的组件去色，生成原型组件。这样有限度的公用视觉组件库，提高效率。

<a name="2f625ff6"></a>
#### 1.2.3、动态原型设计组件库Dynamic Whale Template
包含小程序原型库等。可以通过原型库插件继续增加。

<a name="aa4de8b6"></a>
## 二、UI 设计库
基于市面上常用的UI库组成。

<a name="5123f6f5"></a>
### 2.1、基础UI库
Web：Fusion Design UI库 + Ant Design UI库<br />mobile：Apple IOS UI + Material Design UI

<a name="5f9c5a84"></a>
### 2.2、动态UI库
如小程序UI库。根据业务需求持续加入。

<a name="2fb664a3"></a>
### 2.3、高效使用
Fusion Design UI库使用FusionCool插件。

其余UI库使用Runner Insert 快速插入Symbol使用UI组件。

<a name="b63732a0"></a>
## 三、使用场景
<a name="41b2bb44"></a>
#### 3.1、前台原型设计
智能快速原型库

前台原型设计的特点是：需要视觉重绘大部分的视觉，不局限既有的视觉组件库，设计偏于灵活。使用交互色原型设计，不影响视觉的设计创作。只产出交互稿，视觉稿需要视觉设计。

<a name="8de1af67"></a>
#### 3.2、中后台原型设计
Symbols GrayScale原型库 +  UI设计库

前台原型设计的特点是：注重功能逻辑，遵循统一的视觉组件，设计偏规范，直接使用视觉原型设计。直接产出交互和视觉稿。

当然在很多的项目中，这两种场景很多时候，并非是相互独立，根据情况使用即可。

<a name="de20dadc"></a>
## [四、Whale Design](https://fusion.design/18642/) 
高效设计交互规范库理念的产物，基于[Fusion Design](https://fusion.design/)设计。

主旨：Work Smart，Think more，Do Less，Get More。


