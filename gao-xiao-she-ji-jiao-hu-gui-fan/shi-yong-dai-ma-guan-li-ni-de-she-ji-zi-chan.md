# 使用代码管理你的设计资产

![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552047225454-9b2a9660-faf3-4181-b0a0-518f67c2c34e.png#align=left&display=inline&height=638&name=image.png&originHeight=1275&originWidth=1920&size=795829&status=done&width=960)<br />最近在整理设计规范的过程中，尝试使用了 Airbnb 公司发布的 [react-sketchapp](https://github.com/airbnb/react-sketchapp) 工具。从react-sketchapp公布之初，它就迅速被设计师和前端工程师们所关注，作为非主流边缘设计师，我被它所吸引，得知后便进行了了解并进行了体验。

这个跨界的工具提供了一种很新颖的思路，在某些特定情况下有其应用场景。

<a name="3bc7380d"></a>
### 一、React - SketchApp 是啥？
React - SketchApp 是一个开源库，为设计系统量身定制。它通过将 React 元素渲染到 Sketch 来连接设计和开发之间的鸿沟。<br />这个神奇的开源库给设计师们提供了一个全新的设计工作流程：在时下最流行的 React 前端框架下用代码进行设计，并实时渲染到 Sketch 中审阅设计。细思恐极，在设计圈大红大紫的 Sketch 虽说占了开源库的一半名字，但其实担当的只是一个浏览器的角色。真正留下的设计文档则成了代码。

<a name="268fa667"></a>
### 二、为啥？？为啥？？
你一定在想，为什么好好的，突然让所有设计师用起代码做设计了？为啥又要用前段框架了？这成本对我们来说有多高？听听 Airbnb 怎么说。

一个设计系统可以让设计师复用样式、组件、图形，这可以给设计师更多的时间去进行更高层次的思考。同时，一个好的设计系统也让工程师自信地添加新功能，而不用去看密密麻麻的标注线，痛苦地和设计师来回调整像素。而同样的，一个完善的设计系统一般都是非常庞大而复杂的，想有序地构建和发展这个系统，本身就有着巨大的工作量。在我们团队中，瓶颈就在 Sketch Template 上。

就拿 Airbnb 的设计系统 DLS 举例，它从字体、颜色、间隙的规范开始，逐渐发展成了跨平台、跨屏幕尺寸、跨语言的丰富设计库。当然作为一个设计系统，永远也不会有完成的时候，我们持续的向其中增加内容，更改和调整已有的组件，让每一个人都可以使用它。

但是在这个过程中，每一点对这个系统的增加和更改，都会产生很大的工作量。文档需要更新，每个 App 都需要调整，Sketch Template 又要重新绘制。而所有这些工作还必须协同进行。

基于图形的设计工具在版本控制上有着先天的劣势，所有的可以拖来拖去的元素经常让我们对设计系统的状态产生不确定感。「移动端 Title 字体是多大来着？」「现在最新的方案还是这样子么？」「这个组件在不同屏幕上怎么显示？」诸如此类的问题在办公室中几乎是时时出现 。相反，代码相对来说就更容易管理，同时我们已经有了对代码版本管理的积累和基础。而维护 Sketch Template 还只能依靠劳动密集的人工管理。因此我们希望通过代码来优化整个工作流程。

Sketch 文件本身倒是可以直接用代码组织，但是提供的 API 却经常变化。相反 React 框架给可复用文档提供了完美的封装形式，同时有前端基础的设计师可能已经比较熟悉了。

<a name="d9c7c83f"></a>
### 三、核心优势
剔除 Airbnb，在仔细看了相关文档和项目样例后，总结出了一下这个开源工具在构建设计系统时的核心优势：

**稳定的文档：**用成熟的前端框架作为设计系统基础，可以保证整个设计系统长期的可用性。

**数据的清晰准确：**以代码为描述设计的形式，杜绝了基于图片描述设计时容易产生的数据不稳定。

**可进行响应式设计：**比起 Sketch 略显简陋的 Resizing，React 提供了功能完备的布局系统，可以在设计端进行准确完整的响应式设计。

**版本管理：**避开了基于图片设计的版本管理难点，git 等工具组织设计系统，让系统更实时、可考。

**跨平台开发：**因为和 ReactNative 采用同一套布局系统，配合 ReactNative 可以很好地进行跨平台工作。

**引入真实数据 & API：**可以和任何前端开发一样引入真实的数据和 API 实现例如、等有趣的功能。

以上这些优势，确实可以切中很多团队在构建大型设计系统时的痛点。

相比之下 React - SketchApp 在这些问题下，跳出了原有的思考方式，用超前全新的方案解决目前方案的痛点。

<a name="3a15ec6d"></a>
### 四、使用React-Sketchapp制作styleguide模板
说了这么多概念上的东西，大家一定很期待从实用角度看看它到底是怎么工作的，接下来就让我们对 React - SketchApp 做一个初步的体验。对它同样感兴趣的也可以根据下面步骤一起尝试。

<a name="1dc3d3a5"></a>
#### 1、[code-sketch-resource](https://github.com/jingwhale/code-sketch-resource) 工程项目简介
使用React-Sketchapp制作调色板和文字模板，效果如下：<br />**1）调色板**<br />![Color.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552048817637-6e5333e1-2958-4740-8029-f6f4714cabbb.png#align=left&display=inline&height=1927&name=Color.png&originHeight=3719&originWidth=1440&size=558794&status=done&width=746)<br />**2）字体**<br />![Text副本.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1552049054577-d9c13c5f-fe5d-4a1f-af47-577ed3e7596d.png#align=left&display=inline&height=1637&name=Text%E5%89%AF%E6%9C%AC.png&originHeight=3159&originWidth=1440&size=448843&status=done&width=746)
<a name="63c99a7c"></a>
#### 2、调色板与文字原理
1）调色板<br />调色板是一组规律的16进制码。可以将色彩体系解读成两个层面：系统级色彩体系和产品级色彩体系。系统级色彩体系主要定义了中台设计中的基础色板、中性色板和数据可视化色板。产品级色彩体系则是在具体设计过程中，基于系统色彩进一步定义符合产品调性以及功能诉求的颜色。这里选用的是Ant Design的色彩系统。

Ant Design 的基础色板共计 120 个颜色，包含 12 个主色以及衍生色。这些颜色基本可以满足中后台设计中对于颜色的需求。

色板生成算法 主要代码：源代码：[ant-design-colors](https://github.com/ant-design/ant-design-colors)

```typescript
function main(color, index) {
    var isLight = index <= 6;
    var hsv = tinycolor(color).toHsv();
    var i = isLight ? lightColorCount + 1 - index : index - lightColorCount - 1;
    // i 为index与6的相对距离
    console.log(hsv)
    return tinycolor({
        h: getHue(hsv, i, isLight),// getHue 获取色相渐变
        s: getSaturation(hsv, i, isLight),// getSaturation 获取饱和度渐变
        v: getValue(hsv, i, isLight),// getValue 获取明度渐变
    }).toHexString();
};
```

根据颜色值、色号与主色色号(6)差的绝对值、减淡/加深这三个参数获取渐变后的色值，其中 HSV 的三个值分别经过了渐变调整：<br />**“Hue”(色相)**的渐变核心代码如上，首先判断冷暖色调；<br />**“Saturation”饱和度**的渐变核心代码如上，对于减淡与加深的饱和度进行了不同的处理，其中减淡递减的值更大，说明减淡的过程中饱和度迅速下降，而由于主色的饱和度一般较高，因此加深的时候饱和度不必增张过快，尤其是最深的颜色，进行了特殊处理。<br />**“Value”明度**的渐变核心代码如上，对于减淡与加深的明度进行了不同的处理，其中加深递减的值更大，说明加深的过程中明度迅速下降，这是由于主色的明度一般较高，因此减淡的时候明度不宜增长过多。

综合来看 3.x 色板生成算法的实现可以看到，主色的选取很重要，一般主色选取饱和度较高、明度较高的颜色才能更好地匹配这个色板生成算法。

2）字体<br />字体是体系化界面设计中最基本的构成之一。我们的用户通过文本来理解内容和完成工作，科学的字体系统将大大提升用户的阅读体验及工作效率。Ant Design 字体方案，是基于『动态秩序』的设计原则，结合了自然对数以及音律的规则得出。 在中后台视觉体系中定义字体系统，建议从下面五个方面出发：<br />**字体家族**<br />**主字体**<br />**字阶与行高**<br />**字重**<br />**字体颜色**<br />**
<a name="b20152f5"></a>
#### 3、制作原理
调用的[API](http://airbnb.io/react-sketchapp/docs/API.html)，在编辑器中通过React代码绘制SketchUI规范。

具体的，通过调用Ant Design 的色板生成算法[ant-design-colors](https://github.com/ant-design/ant-design-colors)产生出基础色板和中性色板的颜色值，然后使用React-Sketchapp基础组件编写代码渲染到Sketch的当前页面中。字体模板亦是如此。

具体步骤如下：

1）、确保，本地安装Node，git。

2）、本地Clone code_sketch_resource 工程项目<br />code_sketch_resource项目依据React-Sketchapp官方项目的styleguide例子基本框架。

```bash
git clone https://github.com/jingwhale/code_sketch_resource
```

3）运行项目，进入styleguide文件夹

```
npm install
npm run render
```

<a name="e7a3599a"></a>
#### 4、关键代码分析
**1）获取调色板色值：**<br />首先，依赖[ant-design-colors](https://github.com/ant-design/ant-design-colors)组件库

```bash
$ npm install @ant-design/colors --save
```

其次，获取调色板色值

```typescript
import { generate, presetPalettes } from '@ant-design/colors';

// Generate color palettes by a given color
const colors = generate('#1890ff');
console.log(colors); // ['#E6F7FF', '#BAE7FF', '#91D5FF', ''#69C0FF', '#40A9FF', '#1890FF', '#096DD9', '#0050B3', '#003A8C', '#002766']

console.log(presetPalettes);
/*
{
  red: [...],
  volcano: [...],
  orange: [...],
  gold: [...],
  yellow: [...],
  lime: [...],
  green: [...],
  cyan: [...],
  blue: [...],
  geekblue: [...],
  purple: [...],
  magenta: [...],
}
*/
```

**2）调色色板UI开发**<br />调色色板UI：父组件Palette_new.js和子组件Swatch_new.js。代码如下：<br />**父组件Palette_new.js**

```typescript
// @flow
import * as React from 'react';
import { View,Text} from 'react-sketchapp';
import SwatchN from './Swatch_new';

const SWATCH_WIDTH = 285;

type P = {
  colors: any,
};
const PaletteN = ({ name,colors}: P) => (

  <View
     name={name}
    style={{
      width: SWATCH_WIDTH,
      flexWrap: 'wrap',
      marginRight: 33,
      marginBottom: 64
    }}
  >
      <Text style={{width:SWATCH_WIDTH,textAlign:"center",marginBottom:16}}>{name}</Text>
      {Object.keys(colors).map(index => (
      <SwatchN color={colors[index]} index={+index+1} name={name}/>
    ))}
  </View>
);

export default PaletteN;

```

**子组件Swatch_new.js**

```typescript
// @flow
import * as React from 'react';
import { View,Text} from 'react-sketchapp';
import type { Color } from '../processColor';

const SWATCH_WIDTH = 285;
const SWATCH_HEIGHT = 56;

type P = {
  name: string,
  color: Color,
};
const SwatchN = ({ color ,index,name}: P) => (
    <View
      name={name+"-"+index}
      style={{
        width: SWATCH_WIDTH,
        height: SWATCH_HEIGHT,
        backgroundColor: color,
        flexDirection: 'row',
      }}

    >
      <Text style={{width: 128,height: "20",color:index<6?"#000":"#fff",marginLeft:"12",marginTop:"18"}}>{name+"-"+index}</Text>
      <Text style={{width: 128,height: "20",color:index<6?"#000":"#fff",textAlign:"right",marginTop:"18"}}>{color}</Text>
  </View>
);

export default SwatchN;

```

**3）**[**react-sketchapp主要Components**](http://airbnb.io/react-sketchapp/docs/API.html#components)**：**

- [`<Document>`](http://airbnb.io/react-sketchapp/docs/API.html#document)
- [`<Page>`](http://airbnb.io/react-sketchapp/docs/API.html#page)
- [`<Artboard>`](http://airbnb.io/react-sketchapp/docs/API.html#artboard)
- [`<Image>`](http://airbnb.io/react-sketchapp/docs/API.html#image)
- [`<RedBox>`](http://airbnb.io/react-sketchapp/docs/API.html#redbox)
- [`<Svg>`](http://airbnb.io/react-sketchapp/docs/API.html#svg)
- [`<Text>`](http://airbnb.io/react-sketchapp/docs/API.html#text)
- [`<View>`](http://airbnb.io/react-sketchapp/docs/API.html#view)

更多具体代码请参考[code-sketch-resource](https://github.com/jingwhale/code-sketch-resource)项目库。

<a name="f5e882ad"></a>
### 五、总结
1、系统设计资源不仅需要，而且非常需要使用react-sketchapp创建。用代码组织管理系统设计资源Sketch 文件，是最好的方式。系统设计资源包括设计规范，它是有规律且相对固定的思维产物，这非常适合用代码管理。

2、React-sketchapp 只是提供了一个思路，打通程序与设计后，诸如此类的工具还有非常大的空间等待挖掘。<br />例如：使用代码进行交互设计中页面流程图的绘制，亦或者是使用代码进行自动配色系统。

3、人工智能交互设计？<br />既然组件是固定的，设计原则是固定的，为什么不能让代码进行交互设计并产出交互稿呢？你只需要输入关键字，依次进行页面布局，功能设计等，偶尔手动调整局部组件位置大小即可。当然这种设想在中后台设计系统中可省去50%-90%的设计和制作原型的时间；前台设计需要更多的用户体验设计，可以先设计初稿，再加强优化用户体验的设计。

当然，我已经在设计并实现这个系统了，是不是很令人激动呢！我们拭目以待吧！


附：<br />[https://github.com/jingwhale/](https://github.com/jingwhale/code_sketch_resource)[code-sketch-resource](https://github.com/jingwhale/code-sketch-resource) <br />[https://github.com/airbnb/react-sketchapp](https://github.com/airbnb/react-sketchapp)<br />[https://github.com/ant-design/ant-design-colors](https://github.com/ant-design/ant-design-colors)
