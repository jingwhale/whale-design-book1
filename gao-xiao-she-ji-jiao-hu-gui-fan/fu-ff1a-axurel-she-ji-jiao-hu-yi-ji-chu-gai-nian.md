# 附：Axure设计交互一基础概念

<a name="9fbbad03"></a>
### 一、Axure RP是原型设计软件
Axure RP是一款专业的原型设计软件，是最流行的原型设计工具之一。它能快速、高效地演示产品，准确地表达产品设计人员的意图和想法。

Axure RP的特点是交互功能非常强大，不需要写一行代码，就能实现非常复杂的交互效果。其逼真的交互效果能准确地传达设计者的意图。

在互联网公司，原型贯穿于整个产品开发流程中。

**需求分析阶段：**产品经理根据用户需求通过Axure RP制作出产品的原型。

**产品讨论阶段：**原型制作完成后，产品经理可以给客户、领导和同事演示原型。相比随手绘制的草图、示意图，可交互的Axure RP原型可以让大家更加直观地看到未来产品的样子，便于团队进行讨论和修改。在获取反馈后，可在Axure RP中即时修改原型，快速形成一个大家共同认可的产品设计。

**UI设计阶段：**设计部门的同事会参考原型，做出界面的设计图。

**研发阶段：**研发部门的同事会参考原型，实现产品的各项功能。

**测试阶段：**测试部门的同事会参考原型，编写测试用例。

产品开发就这么一步一步实现了。可以说，制作原型是产品经理必备的技能。学习制作优秀的原型是成为产品经理的第一步。

<a name="375cc8a0"></a>
### 二、软件界面概述
在学习制作原型之前，先来了解一下Axure RP软件的界面。<br />如图所示，Axure RP的界面包括如下几部分。![屏幕快照 2019-04-07 下午3.21.43.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554621768822-d588dd9e-2b7d-4644-a31b-32ece768d1b3.png#align=left&display=inline&height=368&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.21.43.png&originHeight=1050&originWidth=2130&size=932259&status=done&width=746)

**（1）菜单：**包括文件、编辑、视图、项目、布局、发布、团队、账户和帮助。文件的管理、软件的设置等功能可以在菜单中找到。<br />**（2）快捷功能：**画笔、对齐等常用的功能按钮都平铺在这里。<br />**（3）站点地图：**Axure RP可以制作多个页面的原型。在站点地图里可展示多个页面的层级关系。<br />**（4）元件库：**“文字”“图片”“输入框”“按钮”等所有元件都放在这里。原型就是由这些元件组成的。<br />**（5）母版：**多个元件可以组成一个母版。母版可以在多个页面中重复使用。例如，网站导航栏就可以组成一个母版在每个页面中使用。<br />**（6）画布：**画布是用来画原型的地方。画原型的过程就是把元件从元件库中拖曳到画布上组成原型。<br />**（7）属性设置：**设置元件的样式和动作属性。动作属性是实现交互动画的主要手段。<br />**（8）元件地图：**元件地图可展示页面上所有元件的层级关系。元件的层级关系一般是通过一个叫做“动态面板”的元件来管理的。所以这里主要用来查看和管理“动态面板”。

<a name="f3c9dbb7"></a>
### 三、基础概念
按顺序介绍Axure RP软件界面上各个区域的功能，熟悉Axure RP的基础操作。然后对涉及的功能进行解释，掌握Axure RP的基础概念。

<a name="f53c2374"></a>
#### 3.1、画布
Axure RP软件界面中心区域就是画布，如图所示。一般把制作原型的过程叫做“画原型图”。原型就是在画布上画出来的。<br />![](https://cdn.nlark.com/yuque/0/2019/png/120638/1554622381817-7090e177-5385-45e2-9335-80145dfb6f8e.png#align=left&display=inline&height=274&originHeight=1476&originWidth=2130&status=done&width=396)

画布分为以下3部分。<br />（1）中间空白区域用来放置“元件”。Axure RP是所见即所得的，画布上元件摆成的样子基本上就是最终原型的样子。<br />（2）顶部是页面标签。标签上显示页面的标题。页面的标题可以在站点地图中修改。<br />（3）左边和上边是标尺。上面的刻度是坐标（单位：像素），与计算机显示器的分辨率（单位：像素）对应。

设计原型前就应该考虑好原型要在什么设备上展示，按目标设备的分辨率规划原型的大小。

计算机显示器的分辨率与原型的坐标值是对应的。但是，手机的分辨率与原型的坐标值不是1∶1的。例如，如果想让原型在iPhone 7上的显示效果最佳，那么原型应该做成多大好呢？第9章会给出答案。

**小知识：**<br />画布上有一些快捷操作：<br />（1）Ctrl+鼠标滚轮，用于放大缩小页面。<br />（2）Shift+鼠标滚轮，用于横向滑动页面。

<a name="48d65227"></a>
#### 3.2、坐标
元件是放置在画布上的。元件在画布上的位置通过坐标来描述。元件的坐标值指的是元件左上角那个点的坐标值。例如图中文本框的坐标是x=0，y=0。按钮的坐标是x=212，y=130。<br />![屏幕快照 2019-04-07 下午3.32.32.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554622419889-b0e16c86-51e7-4ec8-b77e-05ddb2ef7a95.png#align=left&display=inline&height=147&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.32.32.png&originHeight=734&originWidth=2130&size=454339&status=done&width=428)

光标停在元件边缘时，Axure RP会自动提示元件的坐标、尺寸。x为横坐标，y为纵坐标，w为宽度，h为高度。

从标尺上可以看出，横坐标越向右值越大，纵坐标越向下值越大。坐标值为负数时，元件会超出屏幕显示范围。

<a name="e04d5c52"></a>
#### 3.3、元件库
做原型的过程就像是搭积木——把元件库里的元件拖曳到画布上，设好颜色、大小，就能“搭”出想做的网站/APP的样子。

Axure RP默认的元件库中提供了多种元件，如图所示。<br />![屏幕快照 2019-04-07 下午3.35.12.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554622523869-dbda59fc-10ae-4677-8199-1dc21d0e091b.png#align=left&display=inline&height=367&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.35.12.png&originHeight=1396&originWidth=2126&size=959611&status=done&width=559)

| **1）、图形类元件** | 如图中的矩形1、矩形2、矩形3、椭圆形和后面的占位符都属于图形类的元件。<br />![屏幕快照 2019-04-07 下午3.38.12.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554622898986-d31133a2-eecb-4e94-9d2e-f6b876ad6c9c.png#align=left&display=inline&height=181&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.38.12.png&originHeight=1010&originWidth=2134&size=432429&status=done&width=382) |
| --- | --- |
|  | 在快捷功能区（如图所示）可以设置元件的文字格式，元件本身的颜色、阴影效果，以及边缘线的颜色、形式。<br />![屏幕快照 2019-04-07 下午3.39.21.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554622770671-cddeb9da-0049-406c-b0de-c3f0ebb589c2.png#align=left&display=inline&height=66&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.39.21.png&originHeight=276&originWidth=2102&size=311880&status=done&width=512) |
|  | 图形类元件可以用来制作原型中的分隔框、背景、按钮等，其他用途有待用户在使用中发掘。其中，占位符常常用来代表图片。如图1-12中的占位符用来表示页面顶部的轮播图。<br />![屏幕快照 2019-04-07 下午3.40.42.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554622853601-aa003b2c-9fb7-48b7-8044-cc581daa4fab.png#align=left&display=inline&height=301&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.40.42.png&originHeight=1564&originWidth=1814&size=818376&status=done&width=349) |
|  | 图形类元件可以改变形状，如图1-13所示。单击矩形，右上角会出现一个“小圆球”。单击小圆球，弹出形状菜单。单击其中任意一个图形（如五角星），矩形就会变为五角星。所有的图形类元件都可以相互转换。<br />![屏幕快照 2019-04-07 下午3.42.42.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554622972960-1ec1aa77-2a90-4f09-be70-5c2b035a9f6f.png#align=left&display=inline&height=209&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.42.42.png&originHeight=872&originWidth=2134&size=883360&status=done&width=512) |
|  | 除了上述图形，Axure RP还支持用“钢笔”功能画出任意形状。<br />![屏幕快照 2019-04-07 下午3.45.25.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623136037-c3ea9cef-4b6d-448f-9f57-3571b185fec6.png#align=left&display=inline&height=359&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.45.25.png&originHeight=1434&originWidth=2044&size=713106&status=done&width=512) |
| **2）、按钮类元件** | 按钮类元件包括按钮、主要按钮和链接按钮，添加到画布上后如图所示。<br />·按钮：是预先设置了倒角、加了文字的矩形。<br />·主要按钮：是预先设置了填充颜色的按钮。<br />·链接按钮：是没有边缘线的按钮。<br /><br />![屏幕快照 2019-04-07 下午3.47.20.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623250607-40580ca4-d795-4977-9f6a-b9019da3f67f.png#align=left&display=inline&height=55&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.47.20.png&originHeight=370&originWidth=2036&size=316406&status=done&width=305)<br /> |
|  | 其实，按钮类元件也属于图形类元件，只是样式不同而已。 |
| **3）、图片元件** | 把图片元件添加到画布上后如图所示。<br />![屏幕快照 2019-04-07 下午3.48.56.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623344909-0a42c2fb-dd97-4d14-b5aa-0b0b0d1eb39b.png#align=left&display=inline&height=123&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.48.56.png&originHeight=1204&originWidth=2098&size=406139&status=done&width=215)<br />图片元件可以像“占位符”一样用来代表图片。 |
|  | 双击图片元件，会弹出文件对话框，选择一张图片即可添加图片到原型中。不过，Axure RP也支持直接将图片复制（Ctrl+C）、粘贴（Ctrl+V）到画布上。所以，实际工作中，除非有动态加载的需求，否则很少通过图片元件来添加图片。 |
|  | 举一个通过图片元件来动态加载图片的例子。<br />如图a是一个照片编辑工具的原型。这个页面需要动态加载上一个页面中用户选择的照片。原型中，这个页面上放置了4个图片元件来占位。上一个页面中通过交互动作记录用户选中的照片。读取这个页面时，设置交互动作动态加载照片，如图b所示。<br />![屏幕快照 2019-04-07 下午3.51.16.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623485568-2a066de3-4326-47bc-a9b1-7d11d18ea37e.png#align=left&display=inline&height=275&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.51.16.png&originHeight=1382&originWidth=2024&size=1449872&status=done&width=402)<br /> |
| **4）、文字元件** | 把一级标题、二级标题、三级标题、文本标签、文本段落添加到画布上后如图所示。<br />![屏幕快照 2019-04-07 下午3.53.08.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623598399-4bc18fd9-2555-4ab5-85e2-c62d21da8f04.png#align=left&display=inline&height=227&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.53.08.png&originHeight=1434&originWidth=2072&size=1706134&status=done&width=328) |
|  | 文字元件通常用来制作原型中的标题、简介和正文等。 |
|  | 双击文字元件，即可直接修改文字。通过快捷功能区（如图1-19所示），可以设置文字的字体、颜色和格式。<br />![屏幕快照 2019-04-07 下午3.54.23.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623675364-a640b8ff-e76a-468f-b1cf-4456591c1fbb.png#align=left&display=inline&height=37&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.54.23.png&originHeight=154&originWidth=2142&size=164451&status=done&width=512) |
|  | 原型中通常要将文字设置为不同的样式，以此强调或弱化不同信息的重要程度，如图所示。<br />![屏幕快照 2019-04-07 下午3.55.16.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623724925-f91865f6-20ca-4acc-98bc-4718c4f474cf.png#align=left&display=inline&height=284&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.55.16.png&originHeight=1544&originWidth=1974&size=1338874&status=done&width=364) |
| **5）、水平线和垂直线** | 水平线和垂直线通常用来制作原型中的分隔线和箭头等。<br />水平线和垂直线可以改变线的粗细、虚实、颜色，并且可以增加箭头，如图所示。<br />![屏幕快照 2019-04-07 下午3.57.10.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623839412-726fe307-5f9f-4dab-bf12-23aeb70d8ac6.png#align=left&display=inline&height=176&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.57.10.png&originHeight=1000&originWidth=2080&size=334072&status=done&width=367) |
| **6）、热区** | 热区”在Axure RP的画布上看起来是一个浅绿色矩形，如图所示。其实原型发布之后，热区是透明的。<br />![屏幕快照 2019-04-07 下午3.58.20.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554623909296-cbbab885-1af9-40a0-be7f-281c67869eb1.png#align=left&display=inline&height=239&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%883.58.20.png&originHeight=1538&originWidth=1296&size=345017&status=done&width=201) |
|  | 热区有什么作用呢？其可以扩大点击区域。<br />例如图的原型交互效果是用户点击“标签”那一行进入个人相册页面。如果没有热区，要实现这个效果需要把“小机册”4个字、图片及底部白框都设置上交互动作。有了热区则可以在3个元件上放一层透明的热区，然后只在热区上设置交互动作即可。<br />![屏幕快照 2019-04-07 下午4.00.07.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624014900-947747e2-a485-4529-bfc2-d573918e1f31.png#align=left&display=inline&height=376&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.00.07.png&originHeight=1150&originWidth=688&size=342492&status=done&width=225)<br /> |
| **7）、内联框架** | 内联框架放在画布上如图所示。<br />![屏幕快照 2019-04-07 下午4.01.58.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624186595-d361a949-db0e-4b41-bbed-61fc08dd525c.png#align=left&display=inline&height=234&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.01.58.png&originHeight=1468&originWidth=2092&size=396562&status=done&width=334) |
|  | 内联框架可以链接到原型内的页面或外部网页。双击内联框架，会弹出设置链接的对话框，如图所示。<br />![屏幕快照 2019-04-07 下午4.02.23.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624202142-cd5f1e41-96b3-4fde-a464-73a16631880e.png#align=left&display=inline&height=410&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.02.23.png&originHeight=1550&originWidth=1202&size=508964&status=done&width=318)<br />**·链接到当前项目的某个页面**：可以让当前原型中其他页面出现在内联框架所在的位置。<br />**·链接到URL或文件**：可以让任意网站的网页出现在内联框架所在的位置，包括网络视频。通过视频网站的视频分享功能获取分享链接，在超链接输入框中填写视频的分享链接，就可以实现在原型中显示视频的效果。 |
| **8）、动态面板** | 动态面板放在画布上后如图所示<br />![屏幕快照 2019-04-07 下午4.04.21.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624274870-24640a17-6280-4659-ace0-6b4a970a84c7.png#align=left&display=inline&height=193&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.04.21.png&originHeight=808&originWidth=2140&size=583324&status=done&width=512)

新建的动态面板在元件地图上显示为两行，如图中的标注框所示。其中，第一行是动态面板，第二行是动态面板的一个状态，名称为State1。动态面板可以添加多个状态。 |
|  | 动态面板和状态是什么关系呢？打个比方，动态面板相当于一个卡片盒，状态相当于卡片。一个卡片盒可以装多张卡片，但只有最上面的一张卡片可以被人看到。<br />动态面板常用来制作子页面。如图所示案例中，需要给APP制作3个子页面，分别是“慈善项目”“跑团”“我的”页面。<br />![屏幕快照 2019-04-07 下午4.08.47.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624539740-85459007-3a00-490f-8bb4-df136d6905b7.png#align=left&display=inline&height=201&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.08.47.png&originHeight=1160&originWidth=2112&size=1203550&status=done&width=367)<br /><br /><br />制作原型时，先添加一个动态面板，然后在动态面板中添加3个状态，再分别在每个状态中制作一个子页面，如图所示。<br />![屏幕快照 2019-04-07 下午4.09.28.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624578387-520e967b-14ac-4d30-adb9-f6807868c6be.png#align=left&display=inline&height=225&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.09.28.png&originHeight=1246&originWidth=2136&size=1270230&status=done&width=386)<br /><br /><br />在元件地图中双击状态名称可以进入状态的页面，如图所示。<br />![屏幕快照 2019-04-07 下午4.10.03.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624613254-2b5ec56e-9b4c-4bd8-a68a-3099614c10b4.png#align=left&display=inline&height=198&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.10.03.png&originHeight=1010&originWidth=2132&size=1223664&status=done&width=417)<br /><br /><br />“制作完3个状态之后。默认情况下，“慈善项目”状态在最上层，所以只能看到“慈善项目”页面。通过一些交互设置，可以实现点击底部导航栏，切换显示其他两个子页面的效果。 |
| **9）、中继器** | 中继器在画布上的样子如图所示。<br /><br />中继器的作用就是“复制”，其实中继器翻译为“复制器”更准确些。中继器可以设置复制的次数、新的复制品如何摆放，以及每次复制时如何对元件做调整。例如，图1-30中的中继器的复制次数是3，新的复制品纵向排列，每次复制时改变矩形元件上的数字。<br />![屏幕快照 2019-04-07 下午4.14.24.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624915255-0d2f29d7-afc3-496c-bb57-fbb1cba0b9ea.png#align=left&display=inline&height=190&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.14.24.png&originHeight=1500&originWidth=1270&size=493276&status=done&width=161) |
|  | 可以看到，中继器元件有3个矩形。双击中继器，进入中继器的页面，如图1-31所示。<br />在中继器页面中只有一个矩形。<br />![屏幕快照 2019-04-07 下午4.14.46.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554624896707-e12d2d62-a3e9-46ee-935a-c6123f344410.png#align=left&display=inline&height=124&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.14.46.png&originHeight=1186&originWidth=2112&size=616455&status=done&width=221) |
|  | 中继器还可以存储管理数据。如果原型需要输入、编辑数据，则可以用中继器来实现。在下面的章节中会有更详细的介绍。 |
| **10）、表单元件** | Axure RP把一些常见的网页中用于输入、选择的元件统称为表单元件，包括文本框、多行文本框、下拉列表框、列表框、复选框、单选按钮和提交按钮。这些元件在画布上的样子如图所示。<br /><br />![屏幕快照 2019-04-07 下午4.19.49.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625341521-59699582-1c7d-42d4-bfc8-887a087820c6.png#align=left&display=inline&height=196&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.19.49.png&originHeight=816&originWidth=2130&size=443698&status=done&width=512)<br /> |
|  | 双击文本框和多行文本框可以直接编写内容。<br /><br />双击下拉列表框和列表框，会弹出编辑窗口。在窗口中可以添加列表项、上下调整列表项顺序、删除列表项、清除全部列表项。还可以一次添加多个列表项（如图所示），每行算作一个列表项。<br />![屏幕快照 2019-04-07 下午4.20.05.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625354239-945c1e4c-78c3-402d-a2d4-d4c692e958e9.png#align=left&display=inline&height=236&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.20.05.png&originHeight=1174&originWidth=2032&size=871721&status=done&width=410)

单击复选框或单选按钮，则选中或取消选中复选框或单选按钮。双击复选框或单选按钮，可以编辑文字 |
|  | **提示：**<br />“提交按钮”与前面提到的按钮的区别是，提交按钮拥有默认Web交互样式，包括正常的样式、光标悬停的样式、鼠标单击的样式等，如图所示。而前面提到的按钮只是类似矩形的元件，没有默认的样式。所以，提交按钮适用于Web网站原型，其他按钮适用于APP原型。<br />![屏幕快照 2019-04-07 下午4.23.09.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625403890-a937680c-cc85-454c-bf45-ce7d9f0bfa9d.png#align=left&display=inline&height=47&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.23.09.png&originHeight=314&originWidth=2032&size=335112&status=done&width=306)

单选按钮可以设置成“组”。例如，选择3个单选按钮，如图所示，可以在属性栏设置“组”名称。原型中同一组单选按钮，在同一时间内只能有一个处于选中状态。 |
| **11）、表格元件** | 表格元件在画布上的样子如图所示。<br />![屏幕快照 2019-04-07 下午4.25.46.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625583242-cb3c9474-b46a-4a40-9594-348af60bd93d.png#align=left&display=inline&height=92&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.25.46.png&originHeight=272&originWidth=858&size=64572&status=done&width=292) |
|  | 表格元件除了制作表格，还可以用来做列表，如图所示。<br />![屏幕快照 2019-04-07 下午4.26.08.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625590240-f1f20c0f-a07f-4a58-87e8-33e2070243ec.png#align=left&display=inline&height=77&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.26.08.png&originHeight=366&originWidth=2124&size=209589&status=done&width=450) |
| **12）、菜单类元件** | Axure RP中有3个菜单类元件，分别是树状菜单、水平菜单和垂直菜单。<br />（1）树状菜单在画布上的样式如图所示。在树状菜单上右击，在弹出的快捷菜单中可以添加、编辑树状菜单上的节点。树状菜单自带了展开、收起子节点的交互效果。如果菜单层级比较多，用树状菜单表示会更清晰。<br /><br />![屏幕快照 2019-04-07 下午4.27.50.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625716842-6fd6fa8d-3a54-4fa4-a07a-0ac2d0c1d395.png#align=left&display=inline&height=204&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.27.50.png&originHeight=538&originWidth=866&size=214585&status=done&width=329) |
|  | （2）水平菜单和垂直菜单在画布上的样式如图所示。<br /><br />![屏幕快照 2019-04-07 下午4.27.59.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625730542-21f046cc-fb6f-406c-be38-7c2749b778fe.png#align=left&display=inline&height=169&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.27.59.png&originHeight=336&originWidth=866&size=110167&status=done&width=435) |
|  | 在水平菜单、垂直菜单上右击，在弹出的快捷菜单中可以添加、编辑子菜单。这两种元件自带了交互效果：光标悬停时将弹出子菜单，光标移出时子菜单将隐藏。 |
|  | **提示：**<br />水平菜单和垂直菜单适合制作层级比较简单的菜单，使用时可以根据整体页面布局来选择水平样式或垂直样式。 |

<a name="f9c43647"></a>
#### 3.4、站点地图
站点地图可以管理原型中所有页面的层级。

新建原型时会默认添加4个页面，如图1-40所示。图1-40中可以看到顶层有一个index页面。index页面下有3个子页面page1、page2、page3。

右击页面会弹出快捷菜单，通过快捷菜单命令，可以添加、删除、重命名页面，如图所示。<br />![屏幕快照 2019-04-07 下午4.31.44.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625951061-c0c046a5-5aff-48a2-b2fc-694513b2aa17.png#align=left&display=inline&height=106&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.31.44.png&originHeight=432&originWidth=692&size=140601&status=done&width=170)

双击某一个页面，就可以在画布上打开这个页面，进行编辑、添加元件、添加交互等操作。<br />![屏幕快照 2019-04-07 下午4.31.56.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625926172-7a20cd06-2095-46a6-bbdc-1fc9be649bba.png#align=left&display=inline&height=199&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.31.56.png&originHeight=430&originWidth=874&size=220944&status=done&width=404)

如图是一个实际的游戏后台原型的站点地图。要做一个复杂的原型，需要先建立一个条理清晰的站点地图。很难想象如果没有站点地图，如何管理上百个页面。<br />![屏幕快照 2019-04-07 下午4.31.21.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554625969603-fa790348-f71b-46d9-a33e-57fab0740cce.png#align=left&display=inline&height=386&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.31.21.png&originHeight=1564&originWidth=1658&size=1400719&status=done&width=409)

<a name="76d06f61"></a>
#### 3.5、母版
先看图中的两个页面，可以发现两个页面的导航栏是相似的。如果查看整个原型的上百个页面，可以发现每个页面的导航栏都是相似的。<br />![屏幕快照 2019-04-07 下午4.35.45.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626207434-09b610de-a35c-44c2-b4fe-66274da7e205.png#align=left&display=inline&height=224&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.35.45.png&originHeight=840&originWidth=2148&size=731191&status=done&width=573)

如果原型中的多个页面都拥有相同的模块，那么最好将这个模块做成母版。<br />![屏幕快照 2019-04-07 下午4.36.02.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626172217-70c01b65-a82d-40f3-9fbb-cc8c6dd0354b.png#align=left&display=inline&height=79&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.36.02.png&originHeight=320&originWidth=756&size=115072&status=done&width=186)

母版的好处有以下两点。
```
（1）快速复制：母版可以像元件一样直接拖曳到画布上。

（2）方便维护：双击母版即可修改。
例如，导航栏中有一个字错了，没用母版就要去所有页面改这个字，如果用了母版，则只需要在母版中修改，
那么引用了母版的所有页面会随之自动更新。
```

Axure RP为了方便区分母版和其他元件，在母版上加了一层红色遮罩。如果感觉母版的遮罩颜色有干扰，则可以在菜单栏中选择“视图”∣“遮罩”命令，勾掉母版的遮罩。

<a name="a03ab8b8"></a>
#### 3.6、属性
Axure RP的属性设置区域有3个小窗口。如图是选中一个矩形元件时，3个窗口的状态。<br />**·属性：**设置元件的动作和交互。第4章会详细解释Axure RP中交互的原理，以及如何设置交互。

**·说明：**如果原型比较复杂，元件上的交互较多，可以在说明窗口中写下一些备注信息，以防几个月后再打开原型时不记得元件的作用了。

**·样式：**设置元件的位置、尺寸、填充颜色、阴影、圆角、字体等视觉方面的属性。

**3.7、元件地图**<br />元件地图以列表形式展示页面上的所有元件。如图中可以看到页面上的矩形、占位符、动态面板3个元件都显示在右侧的元件地图上了。<br />![屏幕快照 2019-04-07 下午4.40.24.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626485338-9be572b2-a755-4717-b8bc-5aab57b77693.png#align=left&display=inline&height=218&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.40.24.png&originHeight=480&originWidth=864&size=116937&status=done&width=392)

单击元件地图右上角的筛选按钮，在弹出的菜单中可以选择是否显示所有的元件，如图所示。<br />![屏幕快照 2019-04-07 下午4.40.36.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626501311-0e819d3c-b14a-4278-9380-d82eb7ba826e.png#align=left&display=inline&height=246&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.40.36.png&originHeight=800&originWidth=456&size=264249&status=done&width=140)

下面通过实例来看看过滤的效果，如图所示。图a显示所有元件，图b只显示动态面板。<br />![屏幕快照 2019-04-07 下午4.40.58.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626518359-c8a9a9ea-8caa-49b8-abfc-3d5ec876d315.png#align=left&display=inline&height=227&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.40.58.png&originHeight=1102&originWidth=2052&size=971636&status=done&width=422)

**提示：**<br />复杂的原型会使用多个动态面板，每个动态面板又会有多个状态，从而形成一个复杂的层次关系。用元件地图可以更方便地查看这种层次关系。

<a name="1965bf13"></a>
#### 3.7、发布原型
在画布上做好的原型，可以发布成HTML网页，让其他人看到。

在Axure RP界面右上角菜单下面的区域，放置的是发布相关的按钮，如图所示。<br />![屏幕快照 2019-04-07 下午4.42.51.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626707988-77345a62-2ec9-402e-b7ce-6a7e335978d6.png#align=left&display=inline&height=50&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.42.51.png&originHeight=212&originWidth=828&size=106739&status=done&width=196)

**1）、预览**<br />单击“预览”按钮后，Axure RP会根据原型生成一个临时网页，并通过浏览器展示该原型的网页，如图所示。<br />![屏幕快照 2019-04-07 下午4.44.19.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626743647-fb9c72c4-fb48-4fde-b628-31b128b07676.png#align=left&display=inline&height=504&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.44.19.png&originHeight=1570&originWidth=1572&size=1713631&status=done&width=505)

Axure RP生成的网页中左侧是导航栏，对应Axure RP原型中的站点地图。单击导航栏，可以切换原型中的不同页面。网页中右侧是原型，对应Axure RP原型画布上的所有元件。

**提示：**<br />仔细观察图，可以发现Axure RP界面与网页并不完全相同。这是因为Axure RP界面对动态面板和母版做的遮罩在网页中是不显示的。另外，Axure RP中设置的背景、100%宽度等效果只有在网页中才会显示。

**2）、共享**<br />共享功能与预览功能类似，但也有不同，主要表现在以下两点。

```
·预览功能生成的是临时网页，关闭Axure RP后网页就失效了。

·共享功能生成的是长期网页，上传到Axure官方平台的服务器上，生成一段长期有效的网址。
```

**3）、发布**<br />单击“发布“按钮后会弹出如图所示的菜单。<br />![屏幕快照 2019-04-07 下午4.48.11.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554626901648-44e9e6d2-953b-4061-8992-26e86961d787.png#align=left&display=inline&height=181&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-07%20%E4%B8%8B%E5%8D%884.48.11.png&originHeight=488&originWidth=866&size=359768&status=done&width=321)

**·预览：**前面已经介绍过，这里不再赘述。

**·预览选项：**与共享时的配置网页样式一样。

**·发布到AxShare：**就是之前介绍的“共享”功能。

**·生成HTML文件：**会在本地生成HTML文件。可以调整本地存储地址，如图1-57中标注框所示。HTML文件可以直接打包分享给同事查看。

**·在HTML文件中重新生成当前页面**：含义如字面所述。当原型页面很多时，每次生成整个原型的HTML文件都要几分钟或十几分钟。如果只修改了一个页面，重新生成整个原型的HTML文件显然不合算。用这个选项可以只更新一个页面，几乎瞬间完成。相比“生成HTML文件”功能，它可以提高生成的效率。

**·生成Word说明书：**可以生成Word文档。看起来很方便的功能，但如果没有给每个元件做好命名和备注，Word文档几乎没法看明白。实际工作中也很少有人用这个功能。

**·更多生成器和配置文件**：可以配置Word文档、CSV文档、打印的样式。属于与生成文档配套的配置功能，同样比较“鸡肋”。

**提示：**<br />Chrome浏览器和用了Chrome内核的浏览器无法直接打开Axure RP生成的HTML文件。可以依照提示下载相应插件，解决这个问题。

如果读者觉得下载安装插件的过程比较麻烦，笔者推荐使用微软的Edge浏览器，可以直接打开Axure RP网页。

