# 动效设计与落地

对设计师而言，你不仅需要动效设计能力，还要具备与开发之间有效沟通能力、推进动效设计落地能力。而开发人员写代码是以毫秒为单位，动效文件提供稍有误差，将导致 team 当前主要矛盾变为，开发人员日益增长的动效落地与 设计师动效设计之间的矛盾。

动画设计的原理是基于设计与实践要有统一的数据基础。交付产物是给开发所需的数据和动画的原型。

动画可分为非交互类动画和交互类动画。<br />1、非交互类动画<br />较少的技术限制，动画设计可以丰富些。<br />使用[AE](https://www.adobe.com/cn/products/aftereffects/free-trial-download.html) + [lottie-web](https://github.com/airbnb/lottie-web)实现json动画，可以快速建立非交互类动画。

2、交互类动画<br />本质是物体的属性变化<br />结合动画库开发 + 规范化库

动画设计原则需要一些顶层思维的原则：<br />1）、动画不应在最后添加<br />如果把用户体验看作是一个蛋糕，在大多数的情况下，动画被认为是蛋糕顶部的樱桃，不是完全不同意这个观点。动画应该是混入蛋糕糊的另一种原料。

2）、动画一定要有用<br />多余的动画会占用用户宝贵的时间，并且用户在获得初次愉悦之后就会厌倦，这就是为什么动画需要有功能性的原因。一般用于减轻生硬的切换、提供上下文、提供定位、提供及时反馈、让内容感觉是实时的、讲故事。

了解了在何时（When）、何处（Where）使用动画，接下来便是如何（How）使用了。

3）、动画必须反映品牌

4）、动画不应成为唯一的英雄<br />交互体验才是真英雄。

5）、动画必须感觉自然

6）、动画不应该浪费时间

除了动画设计顶层思维的原则以外，动画本身设计也需要设计原则，请查看[《](https://www.yuque.com/jingwhale/blog/ih6bpg)[运动与动画基础](https://www.yuque.com/jingwhale/blog/ih6bpg)[》](https://www.yuque.com/jingwhale/blog/ih6bpg)。

<a name="m5bxt"></a>
### 一、非交互类动画
<a name="sVEUK"></a>
#### 1.1、json动画
Lottie 是Airbnb开源的一个面向Android、 iOS、React Native 、Web的动画库，能分析 Adobe After Effects 导出的json文件并生成动画，使静态素材一样使用这些动画，完美实现动画效果。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556593171015-1729e557-3d6a-4874-8a4f-f046c4503b93.png#align=left&display=inline&height=150&name=image.png&originHeight=329&originWidth=1027&size=36653&status=done&width=466.8181717001704)<br />**1）、导出动画的json**<br />[参考《After Effects》](http://airbnb.io/lottie/#/after-effects)。

**2）、使用json动画**
```bash
npm i --save lottie-react-native
```

```javascript
import React from 'react';
import LottieView from 'lottie-react-native';

export default class BasicExample extends React.Component {
 render() {
   return <LottieView source={require('./animation.json')} autoPlay loop />;
 }
}
```

更多查看[《Lottie》](http://airbnb.io/lottie/)。

**3）、兼容性**

| **Web** | **Android** | **iOS/MacOS** | **React Native** |
| --- | --- | --- | --- |
| 调用Bodymovin提供的js库 — bodymovin.js。 | 支持API 16及以上。 | 支持iOS 8+和MacOS 10.10+。 | 要求Android支持库版本为26，即compileSdkVersion 26。 |

**4）、AEUX**<br />AEUX是由 Google 团队推出的，运用在 Sketch 和 AE 的一组高效插件，能将 Sketch 里的图层以及整个画板一键导入到 AE 里，同时能在 AE 里解决图形分组和分层的问题，减少导出图片或者转入 Illustrator 处理带来的不必要的重复动作。

<a name="nYg6f"></a>
#### 1.2、非交互类动画设计交付
非交互类动画设计交付需要交付技术，直接能使用的产物，比如lottie的json，gif动画等。

<a name="FFKbs"></a>
#### 1.3、非交互类动画设计原则
非交互类动画设计原则要遵循流行动画的设计原则，下面是迪士尼动画的十二个原则：<br />1）、Squash and Stretch压缩与伸展<br />物体受到力的挤压，产生拉长或者压扁的变形状况，再加上夸张的表现方式，使得物体本身看起来有弹性、有质量、富有生命力，因此较容易产生戏剧性。

2）、Anticipation 预备动作<br />动画角色的动作，必须让馆长能够产生“预期性”，透过肢体动作的表演，或者分镜构图的安排，让观众与之角色的下一步动作，也就是让观众更能融入剧情中。

3）、Staging演出布局<br />戏剧是经由编剧和导演设计安排出来的，动画更是如此，因为动画的所有动作安排与构图，都是需要靠动画师的手创造出来，所以在动画中的构图、运镜、动作、走位都需要仔细的设计安排，避免在同一时间又过多琐碎的动作与变化。最重要的还是精心设计好每一个镜头与动作，经过设计之后，不仅可让动画整体更好，也可以省去许多不必要的成本浪费。

4）、Straight Ahead Action and Pose to Pose连续运动与姿态对应<br />连续动作和姿态对应是两种动作动画的技巧，连续动作是将动作从第一张开始，依照顺序画到最后一张，通常是制作较简易的动态。<br />姿势对应，将动作拆解成一些重要的定格动作。补上中间的间补动画后，产生动态的效果，通常适用于较复杂的动作。

5）、Follow Through and Overlapping Action跟随与重叠动作<br />跟随动作，是将物体的各部位拆解，通常是没有骨架的部位较容易产生跟随的动作，例如动物的尾巴，头发，衣服的末梢等等。<br />重叠动作，是将一栋中物体的各部位拆解，将其动作的时间错开，产生分离重叠的时间差与夸张的变形，增加动画戏剧性与表现力，达到更容易吸引观众的目的，也强化了动画的趣味。

6）、Slow In and Slow Out 慢进慢出<br />一般动作在开始与结束时速度较慢，中间过程速度较快一些，因为一般动作并非等速度运动，这时正常的物理现象。静止的物体开始移动时由慢而快，而将要停止时的物体则会由快变慢，若以等速度方式开始或者结束动作，则会产生一种唐突的感觉。

7）、Arcs 弧形运动<br />动画中的动作，基本上除了机械的动作之外，几乎所有的动线都是以抛物线的方式进行，所以在绘制动线时，非机械式的物体，移动时不要完全以直线的方式运行，而机械式的物体，则使用较僵硬的直线运动，这样可以较容易的区别机械与非机械物体的属性，也可强化这两种完全不同的物体的个性。

8）、Secondary Action 第二动作<br />依附在主要动作之下的细微动作，虽然是属于比较微小的动作，但实际上却有画龙点睛的效果。第二动作并非不重要的动作，而是强化主要动作的关键，不仅可以使角色更生动真实，更可让角色感觉有生命。

9）、Timing and Weight 时间节奏与量感<br />动画的灵魂就是物体与角色的运动，而控制运动的关键就是动作的节奏与重量感。<br />动作的节奏就是速度的快慢，过快或者过慢都回让该动作看起来不自然，而不同的角色也会有不用的节奏，因为动作的节奏会影响到角色的个性，也会影响到动作自然与否。<br />另一个控制运动的关键就是指量感，因为所有的物体都是有质量的，而节奏可以表现物体的质量，这和一般人对自然界的认知有关。

10）、Exaggeration 夸张性<br />动画基本上就是夸张的表演方式，透过角色的表演，强化剧情起伏的情绪，让观众更容易融入剧情并且乐在其中。<br />夸张不是只把动作幅度扩大而已，而是巧妙且适当地将剧情所需要的情绪释放出来。在设计动作与脚本时，如何运用动画本身容易表现苦熬张德优势去安排剧情的段落，动画师在诠释角色时对夸张程度的拿捏，都是动画精彩与否的关键。

11）、Solid Drawing 扎实的描绘<br />动画的制作，视觉表现占了很大一部分，而视觉表现则需要非常扎实的绘画训练以及对美感的敏锐度，不论是制作传统动画或者是电脑动画都一样，动画师都需要有扎实的绘画基础训练，才能将动画中所需要的画面完整的表现出来。

12）、Appeale 吸引力<br />吸引力是任何一种艺术都必要具备的条件，动画是和电影一样，包含了许多不同的艺术类型在其中，不管是音乐、画面或者剧情，都必须相互搭配，才能交织整体感最好的动画作品。<br />动画通常最吸引人的地方，就是充满想象力的画面的表现方式。动画几乎所有都是经由动画师与导演的手“创造”出来的，对画面表现的“自由度”极高，所以动画总是给人一种充满想象的感觉，也是动画最吸引人的地方。

<a name="2h5E6"></a>
### 二、交互类动画
交互类动画一般需要技术使用当前技术，实现交互动画。需要有一套动画开发的基础框架，和动画设计的参数配置交付。

<a name="8K7Nt"></a>
#### 2.1、交互类动画的本质
物体对象属性的更改，比如Web中Dom的属性更改。<br />动效常更改的属性：位移，缩放，旋转，透明度等。

<a name="SE2NT"></a>
#### [2.2、Origami Studio](https://origami.design/)
```
Design Prototyping with Origami Studio

Explore, iterate, and test your ideas. A new tool for designing modern interfaces, 
built and used by designers at Facebook. 
```

更多使用请查看[《Introduction》](https://origami.design/documentation/index.html)。

**1）、基本逻辑**<br />每一个动画首先有一个交互触发动作，然后用一个开关来控制一个动作的两种状态，两种状态对应变换两个数值，然后表现在层上~ 数值变化前多一个弹性动画来控制动效。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556605869958-3c30ea3e-e459-4c67-b9a6-705d648e3113.png#align=left&display=inline&height=129&name=image.png&originHeight=243&originWidth=590&size=14145&status=done&width=314)

下图是最简单的图片放大缩小的例子，在数值变化的地方给图片大小一个初始值和结束值，就可以简单的实现点击图片放大缩小的效果了。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556605915295-20c6a56a-0a4f-4787-95ea-4bdd8f90a87d.png#align=left&display=inline&height=180&name=image.png&originHeight=238&originWidth=590&size=64635&status=done&width=445)

**2）、基本概念**<br />“模块”（Patches），是最基本的元素，不同的模块实现不同的功能，要搭建一个原型，实际上就是把不同的模块按照逻辑像搭积木那样拼装的过程。

Patches库包含大量Patches程序，但核心的15-20个Patches将支持大多数原型。 它们都具有单键键盘快捷键，可实现超快速迭代。

基础的Patches如下：<br />**math patches:**<br />![屏幕快照 2019-04-30 下午2.40.59.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556606470327-286bc89a-9feb-4956-ab6b-8f8ce8cfb396.png#align=left&display=inline&height=122&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-30%20%E4%B8%8B%E5%8D%882.40.59.png&originHeight=302&originWidth=1510&size=33608&status=done&width=608)

**… to patches that add interactions to layers:**<br />![屏幕快照 2019-04-30 下午2.42.00.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556606529303-2c382c86-49bd-4e6c-8fe4-46d70e552bcf.png#align=left&display=inline&height=161&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-30%20%E4%B8%8B%E5%8D%882.42.00.png&originHeight=402&originWidth=1510&size=66296&status=done&width=604)

**… to patches that manage states:**<br />**![屏幕快照 2019-04-30 下午2.42.40.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556606569580-3e5d5375-0d06-4912-81b1-6908247b020d.png#align=left&display=inline&height=135&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-30%20%E4%B8%8B%E5%8D%882.42.40.png&originHeight=338&originWidth=1510&size=45737&status=done&width=604)**

**… to patches that control layer properties:**<br />![屏幕快照 2019-04-30 下午2.43.12.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556606600351-22dbeac9-8745-4c59-91a7-f1bb796abcaa.png#align=left&display=inline&height=120&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-30%20%E4%B8%8B%E5%8D%882.43.12.png&originHeight=300&originWidth=1510&size=45563&status=done&width=602)

更多请查看[《Patches》](https://origami.design/documentation/basics/Patches.html)，快捷键请查看[《KeyboardShortcuts》](https://origami.design/documentation/workflow/KeyboardShortcuts.html)。

[**3）、Animations**](https://origami.design/documentation/basics/Animations.html)<br />Origami中的动画片段设计为流畅且可逆的：它们可以使用任何不断变化的数字，并使其变得平滑。

Animation patches<br />**Pop Animation**<br />一种在Facebook应用程序中常见的自然弹性动画，可以通过iOS的弹出框架，Android的Rebound和Web的Rebound JS轻松地将值传递给开发人员。

**Classic Animation**<br />传统的缓和曲线，如线性，缓入和缓出。

**Repeating Motion **<br />使用缓动曲线重复运动重复，来回动画。

[**4）、Patches Components**](https://origami.design/documentation/workflow/PatchGroups.html)<br />通过抽象常用的Patches和图层，构建可重用组件库并与团队共享来节省时间。

[**5）、《Origami Studio教程》**](https://www.jianshu.com/p/4427a0b0601e)

<a name="TvgIS"></a>
#### 2.3、交互类动画的设计交付
**1）、分类描述**<br />适合较为复杂的动画设计<br />**![2019-04-30 18-47-48.2019-04-30 18_48_20.gif](https://cdn.nlark.com/yuque/0/2019/gif/120638/1556621422553-3cc7b12b-94ac-411c-8b9f-bcc173993ff7.gif#align=left&display=inline&height=201&name=2019-04-30%2018-47-48.2019-04-30%2018_48_20.gif&originHeight=774&originWidth=2000&size=573008&status=done&width=519)**

**2）、过程的描述**<br />适合较为简单的动画设计<br />![屏幕快照 2019-04-30 下午6.52.38.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556621577511-79be79d4-e6b9-4b6e-9737-757e5f3673de.png#align=left&display=inline&height=264&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-30%20%E4%B8%8B%E5%8D%886.52.38.png&originHeight=1154&originWidth=2708&size=1713126&status=done&width=620)

<a name="KXoIN"></a>
#### 2.4、交互类动画设计原则

<a name="2uEu9"></a>
### 三、动画技术实现讨论-Web动画
现在，用户对于前端页面的要求已经不能满足于实现功能，更要有颜值，有趣味。除了整体 UI 的美观，在合适的地方添加合适的动画效果往往比静态页面更具有表现力，达到更自然的效果。比如，一个简单的 loading 动画或者页面切换效果不仅能缓解用户的等待情绪，甚至通过使用品牌 logo 等形式，默默达到品牌宣传的效果。

<a name="ppnkZ"></a>
#### 3.1、前端模版
当今前端模版主要有三类：
```
-String-based 模板技术 (基于字符串的parse和compile过程)

-Dom-based 模板技术 (基于Dom的link或compile过程)

-杂交的Living templating 技术 (基于字符串的parse 和 基于dom的compile过程)。
```

所有动画的本质都是连续修改 DOM 元素的一个或者多个属性，使其产生连贯的变化效果，从而形成动画。所以不管现代前端技术如何发展，实现动画的方式，仍然是两种： 通过 css3 动画实现和通过 js 修改元素属性。只不过在具体实现时，需要找到适合模板框架特性的实现技术。

<a name="nIsm0"></a>
#### 3.2、JS与Css实现动画的区别
**1）、JS与Css实现动画的优缺点**

|  | 优点 | 缺点 |
| --- | --- | --- |
| JS动画 | (1)JavaScript动画控制能力很强, 可以在动画播放过程中对动画进行控制：开始、暂停、回放、终止、取消都是可以做到的。<br /><br />(2)动画效果比css3动画丰富,有些动画效果，比如曲线运动,冲击闪烁,视差滚动效果，只有JavaScript动画才能完成<br /><br /> (3)CSS3有兼容性问题，而JS大多时候没有兼容性问题 | (1)JavaScript在浏览器的主线程中运行，而主线程中还有其它需要运行的JavaScript脚本、样式计算、布局、绘制任务等,对其干扰导致线程可能出现阻塞，从而造成丢帧的情况。<br /><br /> (2)代码的复杂度高于CSS动画 |
| Css动画 | (1)浏览器可以对动画进行优化。<br />浏览器使用与 requestAnimationFrame 类似的机制，requestAnimationFrame比起setTimeout，setInterval设置动画的优势主要是:<br />1)requestAnimationFrame 会把每一帧中的所有DOM操作集中起来，在一次重绘或回流中就完成,并且重绘或回流的时间间隔紧紧跟随浏览器的刷新频率,一般来说,这个频率为每秒60帧。<br /><br />2)在隐藏或不可见的元素中requestAnimationFrame不会进行重绘或回流，这当然就意味着更少的的cpu，gpu和内存使用量。<br />强制使用硬件加速 （通过 GPU 来提高动画性能）<br /><br />(2)代码相对简单,性能调优方向固定<br /><br />(3)对于帧速表现不好的低版本浏览器，CSS3可以做到自然降级，而JS则需要撰写额外代码 | (1)运行过程控制较弱,无法附加事件绑定回调函数。CSS动画只能暂停,不能在动画中寻找一个特定的时间点，不能在半路反转动画，不能变换时间尺度，不能在特定的位置添加回调函数或是绑定回放事件,无进度报告<br /><br />  (2)代码冗长。想用 CSS 实现稍微复杂一点动画,最后CSS代码都会变得非常笨重。 |

**2）、CSS动画流畅的原因**<br />渲染线程分为main thread(主线程)和compositor thread(合成器线程)。

如果CSS动画只是改变transform和opacity，这时整个CSS动画得以在compositor thread完成（而JS动画则会在main thread执行，然后触发compositor进行下一步操作）。在JS执行一些昂贵的任务时，main thread繁忙，CSS动画由于使用了compositor thread可以保持流畅。

在主线程中，维护了一棵Layer树（LayerTreeHost），管理了TiledLayer，在compositor thread，维护了同样一颗LayerTreeHostImpl，管理了LayerImpl，这两棵树的内容是拷贝关系。因此可以彼此不干扰，当Javascript在main thread操作LayerTreeHost的同时，compositor thread可以用LayerTreeHostImpl做渲染。当Javascript繁忙导致主线程卡住时，合成到屏幕的过程也是流畅的。<br />为了实现防假死，鼠标键盘消息会被首先分发到compositor thread，然后再到main thread。这样，当main thread繁忙时，compositor thread还是能够响应一部分消息，例如，鼠标滚动时，加入main thread繁忙，compositor thread也会处理滚动消息，滚动已经被提交的页面部分（未被提交的部分将被刷白）。

**CSS动画比JS流畅的前提：**
```
JS在执行一些昂贵的任务

同时CSS动画不触发layout或paint
在CSS动画或JS动画触发了paint或layout时，需要main thread进行Layer树的重计算，这时CSS动画或
JS动画都会阻塞后续操作。
```

只有如下属性的修改才符合“仅触发Composite，不触发layout或paint”：
```
backface-visibility

opacity

perspective

perspective-origin

transfrom
```

所以只有用上了3D加速或修改opacity时，css3动画的优势才会体现出来。

<a name="h70nJ"></a>
#### 3.3、React中常见的动画实现的几种方式
符合 React 的框架特性，可以概括为几类：
```
基于定时器或 requestAnimationFrame(RAF) 的间隔动画；

基于 css3 的简单动画；

React 动画插件 CssTransitionGroup；

结合 hook 实现复杂动画；

其他第三方动画库。
```

**1）、基于定时器或 RAF 的间隔动画**<br />最早，动画的实现都是依靠定时器 setInterval ， setTimeout 或者 requestAnimationFrame (RAF) 直接修改 DOM 元素的属性。

不熟悉 React 特性的开发者可能会习惯性地通过 ref 或者 findDOMNode() 获取真实的 DOM 节点，直接修改其样式。然而，通过 ref 直接获取真实 DOM 并对其操作是是不被提倡使用，应当尽量避免这种操作。

因此，我们需要将定时器或者 RAF 等方法与 DOM 节点属性通过 state 联系起来。首先，需要提取出与变化样式相关的属性，替换为 state ，然后在合适的生命周期函数中添加定时器或者 requestAnimationFrame 不断修改 state ，触发组件更新，从而实现动画效果。

示例：[《react-基于定时器或 RAF 的间隔动画》](https://gist.github.com/jingwhale/eab008f15190b0ce1f98ebb915cac217)

在示例中，我们在 increase 和 decrease 函数中构建线性过渡函数 animation ， requestAnimationFrame 在浏览器每次重绘前执行会执行过渡函数，计算当前进度条 width 属性并更新该 state ，使得进度条重新渲染。

这种实现方式在使用 requestAnimationFrame 时性能不错，完全使用纯 js 实现，不依赖于 css，使用定时器时可能出现掉帧卡顿现象。此外，还需要开发者根据速度函数自己计算状态，比较复杂。

**2）、基于 css3 的简单动画**<br />当 css3 中的 animation 和 transition 出现和普及后，我们可以轻松地利用 css 实现元素样式的变化，而不用通过人为计算实时样式。

基于 css3 的实现方式具有较高的性能，代码量少，但是只能依赖于 css 效果，对于复杂动画也很难实现。此外，通过修改 state 实现动画效果，只能作用于已经存在于 DOM 树中的节点。如果想用这种方式为组件添加入场和离场动画，需要维持至少两个 state 来实现入场和离场动画，其中一个 state 用于控制元素是否显示，另一个 state 用于控制元素在动画中的变化属性。在这种情况下，开发者需要花费大量精力来维护组件的动画逻辑，十分复杂繁琐。

**3）、React 动画插件react-transition-group**<br />该插件可以方便地实现组件的入场和离场动画，使用时需要开发者额外安装。 react-transition-group 包含 CSSTransitionGroup 和 TransitionGroup 两个动画插件，其中，后者是底层 api，前者是后者的进一步封装，可以较为便捷地实现 css 动画。

示例：[《](https://gist.github.com/jingwhale/6decb07dfe4529d86e3190d3f6562ed4)[React 动画插件](https://gist.github.com/jingwhale/6decb07dfe4529d86e3190d3f6562ed4)[react-transition-group](https://gist.github.com/jingwhale/6decb07dfe4529d86e3190d3f6562ed4)[》](https://gist.github.com/jingwhale/6decb07dfe4529d86e3190d3f6562ed4)

CSSTransitionGroup 可以为其子节点添加额外的 css 类，然后通过 css 动画达到入场和离场动画效果。为了给每个 tab 节点添加动画效果，需要先将它们包裹在 CSSTransitionGroup 组件中。

CSSTransitionGroup 支持以下7个属性：<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556626135458-9307d361-9cdc-45af-bc4f-859494f870af.png#align=left&display=inline&height=127&name=image.png&originHeight=214&originWidth=550&size=47164&status=done&width=326)

其中，入场和离场动画是默认开启的，使用时需要设置 transitionEnterTimeout 和 transitionLeaveTimeout 。值得注意的是， CSSTransitionGroup 还提供出现动画（appear），使用时需要设置 transitionAppearTimeout 。那么，出现动画和入场动画有什么区别呢？当设定 transitionAppear 为 true 时， CSSTransitionGroup 在 初次渲染 时，会添加一个出现阶段。在该阶段中， CSSTransitionGroup 的已有子节点都会被相继添加 css 类 'tabs-wrapper-appear' 和 'tabs-wrapper-appear-active' ，实现出现动画效果。因此， 出现动画仅适用于 CSSTransitionGroup 在初次渲染时就存在的子节点 ，一旦 CSSTransitionGroup 完成渲染，其子节点就只可能有入场动画（enter），不可能有出现动画（appear）。

此外，使用 CSSTransitionGroup 需要注意以下几点：<br />-CSSTransitionGroup 默认在 DOM 树中生成一个 span 标签包裹其子节点，如果想要使用其他 html 标签，可设定 CSSTransitionGroup 的 component 属性；<br />-CSSTransitionGroup 的子元素必须添加 key 值才会在节点发生变化时，准确地计算出哪些节点需要添加入场动画，哪些节点需要添加离场动画；<br />-CSSTransitionGroup 的动画效果只作用于直接子节点，不作用于其孙子节点；<br />-动画的结束时间不以 css 中 transition-duration 为准，而是以 transitionEnterTimeout ， transitionLeaveTimeout ， TransitionAppearTimeout 为准，因为某些情况下 transitionend 事件不会被触发，详见 MDN transitionend 。

CSSTransitionGroup 实现动画的优点是：
```
简单易用，可以方便快捷地实现元素的入场和离场动画；

与 React 结合，性能比较好。
```

CSSTransitionGroup 缺点也十分明显：
```
局限于出现动画，入场动画和离场动画；

由于需要制定 transitionName ，灵活性不够；

只能依靠 css 实现简单的动画。
```

**4）、结合 hook 实现复杂动画**<br />在实际项目中，可能需要一些更炫酷的动画效果，这些效果仅依赖于 css3 往往较难实现。此时，我们不妨借助一些成熟的第三方库，如 jQuery 或 GASP，结合 React 组件中的生命周期钩子方法 hook 函数，实现复杂动画效果。除了 React 组件正常的生命周期外， CSSTransitionGroup 的底层 api TransitonGroup 还为其子元素额外提供了一系列特殊的生命周期 hook 函数，在这些 hook 函数中结合第三方动画库可以实现丰富的入场、离场动画效果。

```
TransisitonGroup 分别提供一下六个生命周期 hook 函数：

componentWillAppear(callback)

componentDidAppear()

componentWillEnter(callback)

componentDidEnter()

componentWillLeave(callback)

componentDidLeave()
```

它们的触发时机如图所示：<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1556626314335-eb2da13e-dca7-4890-81c9-4120a951b799.png#align=left&display=inline&height=248&name=image.png&originHeight=339&originWidth=550&size=45943&status=done&width=402)

示例：[《react-结合 hook 实现复杂动画》](https://gist.github.com/jingwhale/c722b85e12a56ee2033e2e9561cb0b44)<br />GASP 是一个 flash 时代发展至今的动画库，借鉴视频帧的概念，特别适合做长时间的序列动画效果。本文中，我们用 TransitonGroup 和 react-gsap-enhancer （一个可以将 GSAP 应用于 React 的增强库）完成一个图片画廊。

结合 hook 实现动画可以支持各种复杂动画，如时间序列动画等，由于依赖第三方库，往往动画效果比较流畅，用户体验较好。但是第三方库的引入，需要开发者额外学习对应的 api，也提升了代码复杂度。

**5）、其他第三方动画库**<br />此外，还有很多优秀的第三方动画库，如[Ant Motion](https://motion.ant.design/index-cn)、 [react-motion](https://github.com/chenglou/react-motion) ，[Animated](https://github.com/animatedjs/animated)， [velocity-react](https://github.com/google-fabric/velocity-react) 等，这些动画库在使用时也各有千秋。
