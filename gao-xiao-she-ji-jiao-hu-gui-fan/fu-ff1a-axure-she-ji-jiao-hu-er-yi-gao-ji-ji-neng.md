# 附：Axure设计交互二一高级技能

<a name="987af6f0"></a>
## 一、母版
如果原型中有多个页面都要用到某个相同的模块，则可以把这个模块做成母版。需要用到这个模块时，直接把母版插入到页面中即可。

相比直接在各个页面复制、粘贴元件，使用母版可以做到统一管理，重复使用。修改母版时，所有用到该母版的页面都会随之自动改变，省去了逐个修改的麻烦。

<a name="82b94ad4"></a>
### 1.1、创建母版
创建母版有两种方法——在母版栏直接添加，或者将元件转换为母版。有经验的设计者一般用第一种方法，没有经验的设计者都是在原型设计过程中才发现有些元件可以转换为母版。

提示：<br />在Axure RP中剪切一个元件，不论是否粘贴回来，所有引用这个元件的动作都会失效。<br />将元件转换为母版时，所有引用这个元件的动作也会失效。可能是在转换时，将元件剪切、粘贴到新的母版中导致的。

将元件转换为动态面板时，没有经历剪切的过程，不会导致引用这个元件的动作失效。

<a name="c5dc6a9d"></a>
### 1.2、使用母版
一般，直接拖曳母版即可把母版添加到画布上。本节主要介绍母版的不同拖放行为，以及如何查看使用情况。

<a name="5ed4f286"></a>
#### 1.2.1　拖放行为
将母版从母版栏拖曳到画布上时，根据不同的设置有不同的行为。<br />在母版上右击，在弹出的快捷菜单中，可以看到母版的拖放行为有3种。
```
·任意位置：母版拖到画布上之后，可以任意拖动改变位置。

·固定位置：母版拖到画布上之后，不能拖动，只能留在创建母版时母版所在的固定位置。

·脱离母版：母版拖到画布上之后，分散成一个个元件，不以母版形式留在画布上。
```

<a name="975abf9f"></a>
#### 1.2.2　使用情况
在母版上右击，在弹出的快捷菜单中选择“使用情况”命令。在弹出的对话框中可以看到哪些页面使用了该母版，如图所示。<br />![屏幕快照 2019-04-08 下午3.14.35.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554707686972-ceed675d-f386-4d06-ac4f-a413d02e2f38.png#align=left&display=inline&height=273&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.14.35.png&originHeight=1182&originWidth=824&size=183612&status=done&width=190)

删除母版时，如果母版正被使用，也会弹出窗口，正在使用中的母版无法删除。

<a name="3b41f553"></a>
### 1.3、案例
利用母版，解决“积分商城”的重复建设<br />[《](https://pan.baidu.com/s/1Azmha5FZ5LcEi97AlL9VRA)[积分商城](https://pan.baidu.com/s/1Azmha5FZ5LcEi97AlL9VRA)[》](https://pan.baidu.com/s/1Azmha5FZ5LcEi97AlL9VRA)提取码: jjwj

<a name="0402f687"></a>
## 二、元件库
在第1章中介绍的元件都属于Axure RP自带的默认元件库。Axure RP用户可以创建满足自己需求的元件，甚至创建自己的元件库。本章将介绍如何创建和使用自定义的元件库，并介绍一些常用元件的创建方法。

<a name="a2323b0d"></a>
### 2.1、使用元件库
在学习创建元件库之前，先来学习如何下载、使用网友共享的元件库，拥有多个元件库时如何切换使用元件库。

<a name="9630d1cf"></a>
#### 2.1.1、下载元件库
单击在元件库右上角的按钮，在弹出菜单中选择“下载元件库”命令，如图所示，就会打开Axure官网的元件库列表。<br />![屏幕快照 2019-04-08 下午3.20.44.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554708053658-f18925c3-5bb3-42bf-afe9-b1f964bcfed2.png#align=left&display=inline&height=221&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.20.44.png&originHeight=656&originWidth=868&size=315208&status=done&width=293)

“元件库文件的后缀名为.rplib。”

<a name="5e713696"></a>
#### 2.1.2、加载元件库
下载完的元件库需要加载才能在Axure RP中使用。单击元件库右上角的按钮，在弹出菜单中：<br />·选择“载入元件库”命令，可以加载本地的元件库文件。<br />·选择“从Axure Share载入元件库”命令，可以加载之前传到Axure Share平台上的元件库文件。查找时，可以输入元件库项目ID或通过浏览文件夹来选择。

<a name="a0b65108"></a>
#### 2.1.3、切换元件库
单击元件库上的下拉菜单，在其中选择想要使用的元件库，即可切换使用该元件库。

<a name="b53fd097"></a>
#### 2.1.4、元件库的其他操作
加载新的元件库之后，可以对新的元件库进行编辑、刷新和卸载。

```
·编辑元件库：打开元件库文件进行编辑。

·刷新元件库：重新加载元件库。如果对元件库进行了修改，会把修改内容同步到Axure RP中。

·卸载元件库：取消加载该元件库。
```

<a name="4077fe19"></a>
### 2.2、创建元件库
本节介绍如何在Axure RP中创建自己的元件库，以及如何在元件库中添加元件，编辑元件的样式、图标等。<br />（1）单击元件库右上角的按钮，在弹出菜单中选择“创建元件库”命令。<br />（2）在弹出的对话框中，选择新建元件库文件的保存位置和名称。单击“保存”按钮后，会自动打开元件库的编辑界面，如图所示。<br />![屏幕快照 2019-04-08 下午3.25.49.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554708359041-b3b6ff69-cc5b-400f-a0be-da40001bba7c.png#align=left&display=inline&height=288&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.25.49.png&originHeight=1092&originWidth=2136&size=698047&status=done&width=563)

（3）元件库编辑界面与原型编辑界面类似，不同之处有以下几点。<br />·页面：界面左上角是元件库页面窗口。元件库的页面与原型的页面概念不同。这里的一个页面对应了一个元件库栏里的元件。<br />·样式：元件库与母版一样不能设置“页面”样式。<br />·属性：元件库的“页面”属性栏中不能设置交互动作。可以设置元件的提示信息，以及元件库中元件的缩略图。<br />（4）进入“新元件1”页面，选择“属性”标签，如图所示。<br />![屏幕快照 2019-04-08 下午3.28.35.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554708588447-04adce0d-5334-4d77-9d1b-c79559e39d66.png#align=left&display=inline&height=272&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.28.35.png&originHeight=1070&originWidth=786&size=393106&status=done&width=200)<br />·页面顶部可以选择使用页面缩略图作为图标，或者导入一个图标文件。<br />·页面底部可以设置元件的提示信息。提示信息会展示在元件库中元件右上角的小问号里，如图所示。<br />（5）在“新元件1”页面中添加一个矩形元件，选中该元件，然后选择“属性”标签，如图所示。元件的“属性”和“样式”设置与原型界面一致。<br />![屏幕快照 2019-04-08 下午3.29.16.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554708613444-e64cbddf-f8cf-4d29-8ae6-fd23a75c18fb.png#align=left&display=inline&height=151&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.29.16.png&originHeight=390&originWidth=876&size=124306&status=done&width=340)<br />（6）单击“发布”按钮，弹出菜单与原型界面一致，如图所示。元件库发布到Axure Share平台上之后，可以通过“从Axure Share载入元件库”命令加载到Axure RP中。<br />![屏幕快照 2019-04-08 下午3.29.28.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554708691510-9dc1ad0d-11e2-4031-a861-b6c72befbab5.png#align=left&display=inline&height=164&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.29.28.png&originHeight=498&originWidth=876&size=320168&status=done&width=289)<br />（7）在一个新建原型中加载这个元件库。可以看到元件库中有一个元件“新元件1”。缩略图上是一个“确定按钮”。单击“新元件1”右上角的小问号会弹出提示信息。

<a name="897904e8"></a>
### 2.3、案例
[《自定义元件库》](https://pan.baidu.com/s/1tgnK9GNvPJoEUeeT5PWAgQ)提取码: tdgi

<a name="addabd5c"></a>
## 三、数据操作
在Axure RP中，可以很方便地设置常用的交互动画。有了交互动画，原型就可以“动”起来了，但原型里的数据并不会真正发生变化。本章将介绍如何通过设置变量、函数和中继器，来控制和修改原型中的数据。

<a name="ff7f1650"></a>
### 3.1、变量
变量是Axure RP中存储数据的抽象概念。可以通过采用变量名称来引用变量，使用变量中存储的数据。Axure RP中元件的位置、宽度等元件数据是变量，页面的名称、窗口大小等系统数据也是变量。用户还可以输入数据并定义变量。
<a name="cf690c24"></a>
#### 3.1.1 使用变量
变量主要应用于动作和条件的设置中。在配置动作时，通常可以直接输入数值来修改参数、改变特定的变量。例如，配置“移动”动作时，可以直接输入数字，来改变元件的位置；配置“设置文本”动作时，可以直接输入文字，来改变元件上的文本。

但在有些时候，直接输入数值并不能满足需求。例如，希望把元件移动到另一个元件底部；或希望将“矩形”上的文字设为“输入框”里的文字。无论是获得元件底部的坐标值，还是获得“输入框”里的文字，都需要使用变量。

使用变量就需要用到fx按钮功能。

（1）在配置动作界面、设置条件界面等许多需要输入“值”的界面都可以看到fx按钮，如图所示。<br />![屏幕快照 2019-04-08 下午3.47.39.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554709673719-1e1c14bd-03e5-44e8-83b7-bdaf89ff3af5.png#align=left&display=inline&height=213&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.47.39.png&originHeight=854&originWidth=2142&size=418833&status=done&width=534)

（2）单击fx按钮，进入“编辑文本”对话框，如图所示。<br />![屏幕快照 2019-04-08 下午3.48.24.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554709717118-8c1d1d74-2a1d-4cf4-b70b-82de8de78e62.png#align=left&display=inline&height=320&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.48.24.png&originHeight=1278&originWidth=2142&size=949990&status=done&width=536)<br />·第1个输入框中可以插入变量或包含变量的表达式。<br />·第2个输入框中可以添加局部变量，后文会有详细介绍。<br />提示：<br />变量名或包含变量名的表达式，必须写在括号“[[]]”内。括号外的表达式都会被当成普通文字。

（3）单击“插入变量或函数”按钮，会弹出如图所示的菜单。<br />其中包含了Axure RP中所有种类的变量和函数，前6类是变量，后5类是函数。<br />![屏幕快照 2019-04-08 下午3.49.59.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554709811287-82b4bdb4-48ff-432c-a1ea-9e6bf4b30329.png#align=left&display=inline&height=263&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.49.59.png&originHeight=874&originWidth=728&size=207363&status=done&width=219)

下面具体介绍Axure RP中的每种变量和函数。

<a name="0e0844b7"></a>
#### 3.1.2 全局变量
通常，全局变量是用来临时存储数据的。使用全局变量前，需要先创建全局变量，创建后，即可将要存储的数据赋值给全局变量。

1.案例说明<br />用户先在搜索框中输入xxx，单击“搜索”按钮后，下面的文字元件显示结果提示“找不到xxx”。这个过程需要用全局变量来存储用户输入的文字。<br />![屏幕快照 2019-04-08 下午3.55.44.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554710215220-cbbbb8c5-078b-4b90-828f-64f0d52f8a72.png#align=left&display=inline&height=130&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.55.44.png&originHeight=338&originWidth=872&size=115118&status=done&width=336)

实现思路是：将“搜索框”元件上的文字内容传给全局变量，再将全局变量的数据加工后传给“文字提示”元件。

2.设置全局变量的值<br />（1）在“搜索”按钮的“鼠标单击时”事件中添加动作——设置变量值，如图所示。<br />![屏幕快照 2019-04-08 下午3.56.19.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554710232173-a4d9a5c2-1fc7-46fa-9ad8-a0364c36700b.png#align=left&display=inline&height=271&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.56.19.png&originHeight=1292&originWidth=2142&size=520401&status=done&width=449)<br />提示：<br />图中可以看到已经有一个变量OnLoadVariable，这个变量是系统自动创建的。<br />输入新变量名称时需要注意字数限制，而且只能输入英文字母或数字。

（3）单击“确定”按钮，进入“配置动作”窗口。在其中选中input，设置input值为“搜索框”元件上的文字，如图所示。<br />![屏幕快照 2019-04-08 下午3.58.10.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554710299142-608274c2-6acb-487d-94d3-96d47429ac07.png#align=left&display=inline&height=393&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.58.10.png&originHeight=1034&originWidth=862&size=182733&status=done&width=328)

**3、使用全局变量**<br />（1）打开添加动作界面，添加动作——设置文本，如图所示。设置“搜索结果”（文字元件）的“值”为“找不到[[input]]”，其中，“找不到”是一段文字，“[[input]]”是变量。<br />![屏幕快照 2019-04-08 下午3.59.49.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554710437806-b0d0ffa0-0160-4fd6-a2c8-a7d79db4febb.png#align=left&display=inline&height=344&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%883.59.49.png&originHeight=1064&originWidth=2106&size=698734&status=done&width=681)<br />（2）预览原型，可以在浏览器中查看原型的效果。在输入框中输入“王者荣耀”，单击“搜索”按钮，会出现文字提示结果“找不到王者荣耀”，如图所示。“王者荣耀”四个字通过全局变量，从输入框传给了文字提示元件。<br />![屏幕快照 2019-04-08 下午4.00.07.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554710419008-790f9ba7-a987-4bde-aee4-b04e6354af3d.png#align=left&display=inline&height=82&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.00.07.png&originHeight=266&originWidth=850&size=104817&status=done&width=263)

**4.全局变量的生命周期**<br />全局变量这个名称翻译是不准确的，因为它并不存在于“全局”。全局变量只在当前页面有效，当跳转到其他页面或者页面刷新之后，全局变量就会清零。

<a name="995a5656"></a>
#### 3.1.3 元件变量
元件变量分为两类：代表“某个元件”的变量、代表元件某个“属性”的变量。<br />**1.元件本身也是变量**<br />元件本身也是一个变量。如图所示，This和Target就代表元件。This代表当前元件，Target代表目标元件。例如，用例是单击A移动B，那么A就是当前元件，B就是目标元件。<br />![屏幕快照 2019-04-08 下午4.03.50.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554710650618-cc5352ff-7a5f-488e-acea-a00cd0318e1d.png#align=left&display=inline&height=309&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.03.50.png&originHeight=1274&originWidth=2126&size=871676&status=done&width=515)

**2.元件属性变量**<br />在元件变量中，除了This和Target，其他变量都是代表元件属性的变量。下面列出Axure RP中所有元件属性变量的含义。

```
·x：元件的横坐标。

·height：元件的高度。

·scrollX：元件横向滚动距离。

·scrollY：元件纵向滚动距离。

·text：元件上的文字。

·name：元件的名称。

·top：元件所占位置的最顶点的y值。

·left：元件所占位置的最左点的x值。

·right：元件所占位置的最右点的x值。

·bottom：元件所占位置的最底点的y值。

·opacity：元件的不透明度。

·rotation：元件的旋转角度。
```

提示：<br />使用元件属性变量时，输入框中默认插入[[This. 属性名]]，例如[[This.x]]。这是因为属性必须属于某个元件才有意义。属性和元件之间以点“.”连接。下面看一个案例，来深入了解元件中各个属性的含义。

<a name="13e75c0a"></a>
#### 3.1.4 局部变量
3.1.2节介绍了如何使用“当前元件”或“目标元件”的属性。本节来介绍如何使用“任意元件”的属性。

局部变量的有效范围很小，只在一个fx编辑界面内有效。

案例：[《局部变量》](https://pan.baidu.com/s/1bOhfcbAOvOVSUpKENouW1w)提取码: zisi

<a name="4f6f42ba"></a>
#### 3.1.5 页面、窗口和鼠标指针变量
Axure RP中可以通过变量来获取原型页面、浏览器窗口和鼠标指针的相关信息。
```
·PageName：页面名称，可以在站点地图中设置。

·Window.width：预览时，当前浏览器窗口的宽度。

·Window.height：预览时，当前浏览器窗口的高度。

·Window.scrollX：窗口纵向滚动距离。

·Window.scrollY：窗口横向滚动距离。

·Cursor.x：当前鼠标的x坐标。

·Cursor.y：当前鼠标的y坐标。

·DragX：当前瞬间拖曳的横向距离。

·DragY：当前瞬间拖曳的纵向距离。

·TotalDragX：元件本次总共被拖曳的横向总距离。

·TotalDragY：元件本次总共被拖曳的纵向总距离。

·DragTime：元件本次拖曳总时间。
```

<a name="ca6f5b02"></a>
### 3.2、函数
Axure RP中有5类函数。但一般情况下，只要用好“加、减、乘、除”函数就能解决95%的问题了。
<a name="ebc5d571"></a>
#### 3.2.1 数字函数
| ·toFixed： | 控制变量的小数点位数。在[[LVAR.toFixed（decimalPoints）]]中，LVAR代表变量，decimalPoints代表小数点位数； |
| --- | --- |
| ·toExponential： | 将变量值转换为指数计数法表示。在[[LVAR.toExponential（decimalPoints）]]中，LVAR代表变量，decimalPoints代表保留位数； |
| ·toPrecision： | 控制变量的精确位数。在[[LVAR.toPrecision（length）]]中，LVAR代表变量，length代表精确位数。 |

<a name="3d126174"></a>
#### 3.2.2 字符串函数
| ·length： | 返回变量的字符长度。在[[LVAR.length]]中，LVAR代表变量。 |
| --- | --- |
| ·charAt： | 返回指定位置的字符。在[[LVAR.charAt（index）]]中，LVAR代表变量，index代表位置。 |
| ·charCodeAt： | 返回指定位置的字符Unicode编码。在[[LVAR.charCodeAt（index）]]中，LVAR代表变量，index代表位置。 |
| ·Concat： | 在变量后接上指定字符串。在[[LVAR.concat（'string'）]]中，LVAR代表变量，'string'是指定字符串。 |
| ·indexOf： | 搜索指定字符在变量中的位置。在[[LVAR.indexOf（'searchValue'）]]中，LVAR代表变量，'searchValue'是指要搜索的字符串。 |
| ·lastIndexOf： | 从后向前搜索指定字符在变量中的位置。在[[LVAR.lastIndexOf（'searchvalue'）]]中，LVAR代表变量，'searchvalue'是指要搜索的字符串。 |
| ·Slice： | 按指定位置截断变量字符串。在[[LVAR.slice（start，end）]]中，LVAR代表变量，start是开始截断位置，end是结束截断位置。 |
| ·Split： | 按指定的分隔符号把变量字符串分割为几段。在[[LVAR.split（'separator'，limit）]]中，LVAR代表变量，'separator'是指定的分隔符号，limit限制了分割后留下前几段字符串。例如a=1.2.3.4.5，[[a.split（'.'，2）]]为1和2。 |
| ·Substr： | 从指定位置开始，截取变量字符串中指定长度的字符。在[[LVAR.substr（start，length）]]中，LVAR代表变量，start是开始位置，length是指定长度。 |
| ·Substring： | 截取变量中两个指定位置间的字符。在[[LVAR.substring（from，to）]]中，LVAR代表变量，from和to分别是指定的起止位置。 |
| ·toLowerCase： | 把变量中的字符转换为小写。在[[LVAR.toLowerCase（）]]中，LVAR代表变量。 |
| ·toUpperCase： | 把变量的中字符转换为大写。在[[LVAR.toUpperCase（）]]中，LVAR代表变量。 |
| ·toString： | 把变量转换为字符格式。在[[LVAR.toString（）]]中，LVAR代表变量。 |
| ·trim： | 去除字符串两端空格。在[[LVAR.trim（）]]中，LVAR代表变量。 |

<a name="b974e151"></a>
#### 3.2.3 数学函数
Axure RP中提供了一些数学函数，可以进行常见的数值计算。另外，在做交互动画时，可以用来计算动画轨迹。

```
·%：取余，如[[5%2]]=1。

·abs（x）：[[Math.abs（x）]]，取x的绝对值。

·asin（x）：[[Math.asin（x）]]，取x的反、正弦值。

·acos（x）：[[Math.acos（x）]]，取x的反余弦值。

·atan（x）：[[Math.atan（x）]]，取x的反正切值。

·atan2（y，x）：[[Math.atan（x）]]，返回原点至点（x，y）的方位角（弧度）。

·sin（x）：[[Math.sin（x）]]，取x的正弦值。

·cos（x）：[[Math.cos（x）]]，取x的余弦值。

·tan（x）：[[Math.tan（x）]]，取x的正切值。

·pow（x，y）：[[Math.pow（x）]]，返回x的y次幂。

·exp（x）：[[Math.exp（x）]]，返回e的x次方。

·log（x）：[[Math.log（x）]]，返回x的自然对数。

·sqrt（x）：[[Math.sqrt（x）]]，取x的平方根。

·ceil（x）：[[Math.ceil（x）]]，对x向上取整。

·floor（x）：[[Math.floor（x）]]，对x向下取整。

·max（x，y）：[[Math.max（x）]]，返回x和y中的最高值。

·min（x，y）：[[Math.min（x）]]，返回x和y中的最低值。

·random（）：[[Math.random（x）]]，返回一个大于0小于1的随机数。
```

<a name="f8c7951a"></a>
#### 3.2.4 日期函数
Axure RP提供了一些日期函数，用于日期的查询、计算和格式转换。制作选择日期、时间的原型时会用到这些函数。

```
·now：[[Now]]，返回当前日期和时间。

·genDate：[[GenDate]]，返回原型生成的日期和时间。

·getFullYear：[[Now.getFullYear（）]]，返回当前年份yyyy。

·getMonth：[[Now.getMonth（）]]，返回当前是第几月。

·getMonthName：[[Now.getMonthName（）]]，返回当前月份名称。

·getDate：[[Now.getDate（）]]，返回当前日期的“日”。

·getDay：[[Now.getDay（）]]，返回当前是一周中的第几天。

·getDayOfWeek：[[Now.getDayOfWeek（）]]，返回当前是星期几。

·getHours：[[Now.getHours（）]]，返回当前时间的“时”。

·getMinutes：[[Now.getMinutes（）]]，返回当前时间的“分”。

·getSeconds：[[Now.getSeconds（）]]，返回当前时间的“秒”。

·getMilliseconds：[[Now.getMilliseconds（）]]，返回当前时间的“毫秒”。

·getTime：[[Now.getTime（）]]，返回1970年1月1日至今的毫秒数。

·getTimezaneOffset：[[Now.getTimezoneOffset（）]]，
返回当地时间与格林威治标准时间（GMT）的分钟差。

·getUTCFullYear：[[Now.getUTCFullYear（）]]，返回当前全球标准日期的“年”。

·getUTCMonth：[[Now.getUTCMonth（）]]，返回当前全球标准日期的“月”。

·getUTCDate：[[Now.getUTCDate（）]]，返回当前全球标准日期的“日”。

·getUTCDay：[[Now.getUTCDay（）]]，返回当前全球标准日期是星期几。

·getUTCHours：[[Now.getUTCHours（）]]，返回当前全球标准时间的“时”。

·getUTCMinutes：[[Now.getUTCMinutes（）]]，返回当前全球标准时间的“分”。

·getUTCSeconds：[[Now.getUTCSeconds（）]]，返回当前全球标准时间的“秒”。

·getUTCMilliseconds：[[Now.getUTCMilliseconds（）]]，返回当前全球标准时间的“毫秒”。

·parse：返回1970年1月1日午夜到指定日期的毫秒数，在[[Date.parse（datestring）]]中，
datestring为指定日期，格式为yyyy/mm/dd。

·toDateString：[[Now.toDateString（）]]中，把当前日期转换为字符串格式。

·toISOString：[[Now.toISOString（）]]中，把当前日期转换为ISO格式的字符串。

·toJSON：[[Now.toJSON（）]]中，把当前日期进行JSON序列化。

·toLocaleDateString：[[Now.toLocaleDateString（）]]中，把当前日期转换为本地时间格式的字符串。

·toLocaleTimeString：[[Now.toLocaleTimeString（）]]中，把当前时间转换为本地时间格式的字符串。

·toLocaleString：[[Now.toLocaleString（）]]中，把当前日期和时间转换为本地时间格式的字符串。

·toTimeString：[[Now.toTimeString（）]]中，把当前时间转换为字符串。

·toUTCString：[[Now.toUTCString（）]]中，把当前全球标准时间转换为字符串。

·UTC：[[Date.UTC（year，month，day，hour，min，sec，millisec）]]，
根据世界时间返回1970年1月1日到指定日期的毫秒数。

·valueOf：[[Now.valueOf（）]]，返回当前日期的原始值（类似getTime）。

·addYears（years）：[[Now.addYears（years）]]，在当前日期上增加指定年数。

·addMonths（months）：[[Now.addYears（months）]]，在当前日期上增加指定月数。

·addDays（days）：[[Now.addYears（days）]]，在当前日期上增加指定天数。

·addHours（hours）：[[Now.addYears（hours）]]，在当前日期上增加指定小时数。

·addMinutes（minutes）：[[Now.addYears（minutes）]]，在当前日期上增加指定分钟数。

·addseconds（seconds）：[[Now.addYears（seconds）]]，在当前日期上增加指定秒数。

·addMilliseconds（ms）：[[Now.addYears（ms）]]，在当前日期上增加指定毫秒数。
```


<a name="89917ee0"></a>
#### 3.2.5 布尔函数
布尔是一种数据类型。布尔值包括两个，即true和false。若一个表达式为真，则这个表达式返回布尔值true；若一个表达式为假，则这个表达式返回布尔值false。
```
·==：例[[a==b]]，a等于b则表达式为true。

·！=：例[[a！=b]]，a不等于b则表达式为true。

·<：例[[a< li="">

·<=：例[[a<=b]]，a小于等于b则表达式为true。

·>：例[[a>b]]，a大于b则表达式为true。

·>=：例[[a>=b]]，a大于等于b则表达式为true。

·&&：例[[a&&b]]，a和b都为true，则表达式才为true。

·||：例[[a||b]]，a和b中只要有一个为true，则表达式就为true。
```

<a name="120f78c2"></a>
### 3.3、中继器 Repeater
<a name="bf232245"></a>
#### 3.3.1 复制
中继器的英文叫做Repeater。中继器的作用就是“复制”。<br />把中继器拖曳到画布上，可以看到默认有三个矩形，分别写着1、2、3，如图所示。在右侧，中继器的属性栏中有一个表格，一共3行，分别写着1、2、3。这不是巧合。属性栏中的表格是中继器的“数据集”。数据集有多少行，中继器就会复制几次。<br />![屏幕快照 2019-04-08 下午4.33.26.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554712428262-900ecc3d-500e-4fa7-a8f4-7c7c97f598b4.png#align=left&display=inline&height=245&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.33.26.png&originHeight=1092&originWidth=2126&size=651893&status=done&width=477)

双击中继器，进入中继器的页面。中继器会复制这个页面中的所有元件。例如在图中，中继器里只有一个矩形，所以中继器复制了3次这个矩形。<br />![屏幕快照 2019-04-08 下午4.34.14.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554712467892-cb7bd49c-f038-4b5c-8991-9c97f0489a27.png#align=left&display=inline&height=107&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.34.14.png&originHeight=520&originWidth=862&size=154367&status=done&width=178)

中继器每次复制的复制品可以称为一个复制项。

<a name="604b7cc0"></a>
#### 3.3.2 数据集
数据集在中继器的属性栏中。<br />·双击“列名称”可以直接修改列名称。列名称只能使用英文。<br />·双击“添加列”、“添加行”按钮，可以添加新的行或列。<br />·双击列表中的数据可以直接修改数据。<br />数据集顶部的按钮可以添加、删除、移动任意一行或一列。<br />按如图所示添加数据并修改名称。第一列id中有5个值1、2、3、4、5。第二列content中有5个值a、b、c、d、e。<br />![屏幕快照 2019-04-08 下午4.36.34.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554712655649-038a22ad-0f2e-472f-be29-a86108286c80.png#align=left&display=inline&height=172&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.36.34.png&originHeight=616&originWidth=862&size=231978&status=done&width=241)

数据集中可以填写数字或文字，也可以添加图片和页面。在数据集表格上右击，在弹出的快捷菜单中选择“引用页面”命令（如图所示），即可在数据集中保存页面的链接；在弹出的快捷菜单中选择“导入图片”命令，即可在数据集中导入图片。<br />![屏幕快照 2019-04-08 下午4.36.45.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554712630529-2bae11f8-ebe3-4d77-9d67-749fe20b6e00.png#align=left&display=inline&height=218&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.36.45.png&originHeight=918&originWidth=556&size=263973&status=done&width=132)

可以用中继器实现不同复制项以加载不同图片，或者单击不同复制项打开不同页面的效果。

<a name="f6114e26"></a>
#### 3.3.3 样式
中继器的背景色、边框、圆角（背景的圆角）、填充等样式的设置与其他元件类似。中继器独有的样式选项有布局、背景、分页和间距等，如图所示。<br />![屏幕快照 2019-04-08 下午4.38.37.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554712789617-f2bd85a7-fa45-4038-95b1-2f24b44b557a.png#align=left&display=inline&height=408&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.38.37.png&originHeight=1204&originWidth=818&size=472628&status=done&width=277)<br />·布局：复制项的布局排列方式。默认选择垂直布局。还可以选择水平布局。网格排布功能可以控制每行或每列的数量，多余项目另起一行或另起一列。

·背景：中继器可以为每一个复制项设置背景，甚至可以选择交替切换背景色。每个项目的“背景”设置会覆盖整个中继器的“背景色”设置。

·分页：设置了分多页显示后，中继器会将复制项分页，只显示其中一页。样式栏中可以设置每页项目数和起始展示哪一页。Axure RP有一个交互动作“中继器-设置当前显示页面”可以调整中继器显示的页数。原型中可以添加一些分页按钮，再添加交互动作进行切换。<br />·间距：设置每行每列之间的间距。它与“填充”样式有所区别。“填充”样式给中继器整体设置间距，而“间距”样式给每个复制项设置间距。

<a name="ad89b5b0"></a>
#### 3.3.4 触发事件
中继器有以下3个触发事件。
```
·载入时：预览原型时，中继器刚刚加载出来时触发这个事件，与其他元件类似。

·每项加载时：每次复制时都会触发这个事件。

·项目调整尺寸时：当复制项尺寸改变时会触发这个事件。
```

“每项加载时”事件中有一个默认的用例。设置矩形上的文字为[[item.Column0]]，如图所示。其中，Column0是数据集中第1列的名称。在前几节中改过列名称后，这里已经变成[[Item.id]]了。<br />![屏幕快照 2019-04-08 下午4.41.56.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554712970143-d06306f6-ebc1-4156-a252-1fa01e9f5033.png#align=left&display=inline&height=131&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.41.56.png&originHeight=402&originWidth=854&size=201822&status=done&width=279)

“每项加载时”事件发生时，当前是第几个复制项，[[Item.id]]就代表数据集中id列的第几行数据。例如，案例中第1个矩形上的文字是id列的第1个数据1。第2个矩形上的文字是id列的第2个数据2，依次类推。

通常在“每项加载时”事件中做初始化工作。例如，用中继器实现图文列表时，可以在中继器中添加文字、图片元件，设好样式，在“每项加载时”设置每行的具体文字和图片。

<a name="fdd95de6"></a>
#### 3.3.5 中继器变量
打开“每项加载时”动作设置界面，然后再打开“设置文本”动作的fx编辑界面，单击“插入变量或函数”链接，可以看到中继器的变量，如图所示。<br />**![屏幕快照 2019-04-08 下午4.43.42.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554713031076-e957c78d-2173-4cae-a8cd-47768ab5aef6.png#align=left&display=inline&height=371&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.43.42.png&originHeight=1204&originWidth=840&size=437780&status=done&width=259)**

```
·Item：代表当前复制项，很少直接使用。

·Item.id\Item.content：代表数据集中某列某行的值，前面介绍过。

·index：单击后插入[[Item.index]]。代表当前是第几个复制项，对应了数据集的第几行。

·isFirst：单击后插入[[Item.isFirst]]。如果当前是第1个复制项，这个变量为true，否则为false。

·isLast：单击后插入[[Item.isLast]]。如果当前是最后一个复制项，这个变量为true，否则为false。

·isEven：单击后插入[[Item.isEven]]。如果当前是第2、4、6等第偶数个复制项，
这个变量为true，否则为false。

·isOdd：单击后插入[[Item.isOdd]]。如果当前是第1、3、5等第奇数个复制项，
这个变量为true，否则为false。

·isMarked：单击后插入[[Item.isMarked]]。如果当前元件被交互动作“标记行”标记过，
则这个变量为true，否则为false。

·isVisible：单击后插入[[Item.isVisible]]。如果当前元件可见，则这个变量为true，否则为false。
```

提示：<br />以上几个is开头的变量，通常用于条件判断中。
```
·repeater：单击后插入[[Item.repeater]]。代表中继器元件，很少直接使用。

·visibleItemCount：单击后插入[[Item.repeater.visibleItemCount]]。等于中继器中可见项目数。

·itemCount：单击后插入[[Item.repeater.itemCount]]。等于中继器中正在显示的项目数
（有些项目会被交互动作“添加筛选”过滤掉）。

·dataCount：单击后插入[[Item.repeater.dataCount]]。等于中继器中的所有项目数。

·pageCount：单击后插入[[Item.repeater.pageCount]]。等于中继器中的总页数。

·pageIndex：单击后插入[[Item.repeater.pageIndex]]。等于中继器中的当前页数。
```

<a name="337d3f9d"></a>
#### 3.3.6　交互动作
打开任意动作编辑界面，可以看到中继器独有的交互动作，如图所示。<br />![屏幕快照 2019-04-08 下午4.47.12.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554713244383-f956495e-24da-49d2-98e7-93c2cecd8fe4.png#align=left&display=inline&height=296&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.47.12.png&originHeight=950&originWidth=818&size=385251&status=done&width=255)<br />1.排序<br />排序将会对整个中继器产生影响，按数据集中的某列，对所有复制项进行升序或降序排列。

2.筛选<br />中继器允许对数据集中某列或某几列设置条件，符合条件的复制项显示，不符合条件的复制项隐藏。

3.数据集<br />Axure RP可以通过交互动作在数据集中添加、修改、删除数据。

<a name="dd3862c6"></a>
### 3.4、案例
[《模拟制作“奇妙清单”APP》](https://pan.baidu.com/s/1pnrueXDgBMbPAABttdEJIQ)提取码: 8qxk<br />[《](https://pan.baidu.com/s/1fy0FgYoTTgO37Qb8x__agA)[ Layout 图片编辑](https://pan.baidu.com/s/1fy0FgYoTTgO37Qb8x__agA)[》](https://pan.baidu.com/s/1fy0FgYoTTgO37Qb8x__agA)提取码: kr5a<br />[《雅虎天气》](https://pan.baidu.com/s/1EB4yqTGqOGgmwFjrlc0fLw)提取码: 8c7r

<a name="08a27a09"></a>
## 四、团队协作
Axure RP 8.0之前的版本只能基于SVN创建团队项目，所以使用团队功能的人不多。Axure RP 8.0推出了基于Axure Share平台的团队项目功能，使用非常便捷，值得一用。本章就来介绍如何使用团队项目功能，进行团队协作。

<a name="9133fcc4"></a>
### 4.1　团队项目介绍
团队项目功能核心的逻辑是：<br />**·共享。**在Axshare平台上创建一个“团队项目”。团队的成员通过项目ID访问项目。<br />**·使用权。**想修改原型时，将要用到的页面“签出”，获得页面的使用权。修改之后，再将页面“签入”，归还页面使用权。同一时间只有一个人可以获得使用权，让团队的修改不会相互影响。<br />**·记录。**修改原型后需要写好修改说明。其他人查看说明时，可以随时了解项目的进展。<br />这样团队成员分工协作，项目就可以顺利进行了。

<a name="63710596"></a>
### 4.2　创建团队项目
假设某人已经制作出了一个原型的草稿，希望接下来由团队成员一起来完善，那么他应该创建一个团队项目，将原型共享给团队成员。<br />（1）打开已经做出了几个页面的原型。<br />（2）打开“团队”菜单，选择“从当前文件创建团队项目”命令，如图所示。<br />![屏幕快照 2019-04-08 下午4.59.27.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714010156-399a9522-a789-401b-8d6b-07150b2720c7.png#align=left&display=inline&height=368&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%884.59.27.png&originHeight=1120&originWidth=862&size=602532&status=done&width=283)<br />（3）在弹出的对话框中，“团队项目位置”选择Axure Share，“团队项目名称”填写“公众号后台”，如图所示。<br />![屏幕快照 2019-04-08 下午5.00.54.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714061989-07a6aaee-2c2c-4f94-a622-cf1d4c370059.png#align=left&display=inline&height=372&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.00.54.png&originHeight=1102&originWidth=862&size=318416&status=done&width=291)<br />**·本地目录：**Axure Share平台上的项目文件是团队共享的，而本地目录中的项目文件是自己的。只有将共享的项目文件下载到本地才能进行修改。注意，一个目录只能存放一个项目。<br />**·URL加密：**这个密码是指打开原型网址的密码。<br />（4）单击“创建”按钮后，会将本地文件上传到Axure Share平台。上传之后，会弹出对话框提示团队项目已创建。
<a name="1d2359a0"></a>
### 4.3　获取团队项目文件
<a name="d57283b2"></a>
#### 4.3.1　查看团队项目ID
其他成员获取团队项目前，创建者首先要把项目ID分享出来。项目ID是创建团队项目时自动生成的一段字母。<br />（1）创建团队项目完成之后，打开“团队”菜单，选择“管理团队项目”命令，如图所示。<br />![屏幕快照 2019-04-08 下午5.03.04.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714225509-dbfe16e3-d5f1-4286-9ffe-addd6388fa60.png#align=left&display=inline&height=397&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.03.04.png&originHeight=1198&originWidth=736&size=585920&status=done&width=244)<br />（2）在弹出的“管理团队项目”对话框中，可以在团队项目的网址中看到团队项目的ID，如图所示。<br />![屏幕快照 2019-04-08 下午5.03.18.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714243258-fc66ed66-acb0-4daf-9768-c7a2ce2ceb54.png#align=left&display=inline&height=144&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.03.18.png&originHeight=242&originWidth=874&size=154994&status=done&width=521)
<a name="e1759c52"></a>
#### 4.3.2　获取团队项目
获取团队项目ID之后，就可以开始获取团队项目了。在Axure RP中提交项目ID，Axure RP会自动下载项目ID对应的团队项目文件。<br />（1）在团队其他成员的计算机上打开Axure RP，新建一个空的原型。<br />（2）打开“团队”菜单，选择“获取并打开团队项目”命令，弹出对话框如图所示。<br />![屏幕快照 2019-04-08 下午5.05.22.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714337299-dcb994bc-3092-4e92-9916-5a30e0ffded8.png#align=left&display=inline&height=288&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.05.22.png&originHeight=806&originWidth=874&size=259272&status=done&width=312)

```
·填写团队项目ID。

·选择本地目录。
```

（3）单击“获取”按钮后，会自动从Axure Share平台上下载原型文件到本地。下载成功后，弹出对话框提示团队项目文件获取成功。

<a name="ef9230a2"></a>
#### 4.3.3　查看本地文件
获取团队项目后，可以在本地查看到团队项目的文件。这些文件是团队项目在本地的一个复制版本。<br />（1）在本地目录中可以看到多了一个新的文件夹。文件夹的名称为团队项目的名称。<br />（2）打开这个文件夹，可以看到一个文件和一个文件夹，如图所示。<br />![屏幕快照 2019-04-08 下午5.07.00.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714428525-41a993a5-be3f-4786-b33b-19efac0432a4.png#align=left&display=inline&height=55&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.07.00.png&originHeight=292&originWidth=706&size=185872&status=done&width=132)

```
·DO_NOT_EDIT文件夹，这个文件夹中存储了团队项目的配置信息和临时文件，请不要随意编辑。

·.rpprj文件是团队项目文件，以后直接打开这个文件即可打开团队项目。
```

<a name="0caadff6"></a>
### 4.4　修改团队项目
在团队项目中，只有获取了使用权的成员才能修改页面。团队可以随时查看所有页面正在被谁使用，还可以查看所有成员的修改记录。
<a name="2701807b"></a>
#### 4.4.1　签出
签出一个页面就是获取一个页面的使用权。有一个原型页面的使用权时，才能修改这个原型页面。<br />**1.未签出时无法修改**<br />获取项目之后，查看原型页面时会发现此时原型是无法修改的，页面上多了一个蓝色的菱形标志。同时，画布右上角会出现“签出”提示。<br />**2.签出后可以修改**<br />继续上文的案例。单击画布右上角的签出按钮后，Axure RP会在Axure Share平台上将项目中的这个页面标记为已被“签出”。签出后的页面可以任意修改，该页面上的标志变成绿色的圆形。<br />**3.已签出的无法再次签出**<br />页面被一个人签出后，其他人再“签出”这个页面时，会弹出“无法签出”提示对话框。对话框中会列出所有无法签出的页面，并列出当前的签出人。<br />对于无法签出的页面，最好放弃继续编辑。如果选择“强制编辑”，以后签入时可能会导致其他人的修改被覆盖而丢失。

<a name="ad75a2db"></a>
#### 4.4.2　提交变更
签出原型页面后，可以在本地任意修改页面。提交变更之后，会将本地修改同步到Axure Share平台的团队项目中。<br />（1）修改之后，打开“团队”菜单，选择“提交所有变更到团队目录”命令。Axure RP会将所有修改更新到Axure Share平台上的项目文件中。<br />（2）提交变更时，需要填写“变更说明”，记录做了哪些修改，方便团队成员了解项目的进展。
<a name="95e76521"></a>
#### 4.4.3　签入
签入一个页面就是归还一个页面的使用权。归还一个原型页面的使用权后，将不能再修改这个原型页面。<br />（1）打开“团队”菜单，选择“签入全部”命令，即可签入页面。<br />（2）签入与提交变更不同。签入代表归还页面的使用权；提交变更代表将修改更新到团队项目。如不提交变更直接签入，Axure RP会在签入时自动提交变更。<br />·已经提交过变更之后再签入时，“签入”对话框中会提示不需要填写签入说明。<br />·修改原型之后直接签入，在“签入”对话框中可以填写签入说明。<br />（3）签入后，原型页面恢复到“未签出”状态，页面上的标志变回蓝色的菱形。

<a name="77ef0f27"></a>
#### 4.4.4　历史记录
提交变更、签入之后都会留下历史记录。历史记录中会按时间顺序标明谁对原型做了修改，修改了哪些页面等信息。<br />（1）在“团队”菜单中，选择“管理团队项目”命令，可以在弹出的对话框中随时查看团队项目中各页面的状态，如图所示。<br />![屏幕快照 2019-04-08 下午5.12.52.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714786043-a7600b93-4a07-4025-8b99-1eb95f28103d.png#align=left&display=inline&height=361&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.12.52.png&originHeight=1238&originWidth=2086&size=1160304&status=done&width=609)

```
·我的状态：我的签入、签出状态。

·团队目录状态：该页面是否可以签出。

·需要获取变更：如果其他人更新了该页面，我就需要获取变更。

·需要提交变更：如果修改了页面，则需要尽快提交变更。
```

**提示：**<br />如果没看到数据，可尝试单击“刷新”按钮，更新数据。

（2）在“团队”菜单中，选择“浏览团队项目历史记录”命令，可以在弹出的对话框中随时查看团队项目的签入、签出记录，如图所示。<br />![屏幕快照 2019-04-08 下午5.14.07.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554714859229-f5169afd-e20f-462b-96ef-59fb61960fa9.png#align=left&display=inline&height=412&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.14.07.png&originHeight=1562&originWidth=1660&size=947807&status=done&width=438)<br />可以自定义时间段获取历史记录。<br />历史记录的签入说明中包含手动输入的说明文字，以及系统自动添加的页面修改记录。

<a name="4a0c6363"></a>
### 4.5、使用[蓝湖](https://lanhuapp.com/prd/?Axure)
简单好用的团队工作台。<br />无缝连接产品、设计、研发流程，降低沟通成本，缩短开发周期，提高工作效率。

<a name="9002092c"></a>
## 五、响应式原型设计
响应式的网站是指网页的排版会根据户行为及使用的设备环境，如系统平台、屏幕尺寸、屏幕方向等进行相应的布局调整。
<a name="66925fc8"></a>
### 5.1 响应式设计
<a name="23cee321"></a>
#### 5.1.1 响应式设计思维
响应式设计不仅是一种技术更是一种思维方式。在设计产品时，需要从“交互、布局”两个方面考虑如何让产品适应不同的设备。<br />**1.交互**<br />同一页面在不同类型的设备（手机、平板、笔记本电脑等）上，应该支持不同的操作方式（如鼠标和触屏），让用户在每种设备上都能使用符合习惯的交互方式。
```
·移动端应该有足够大的按钮，供手指操作。

·PC端上应该平铺多个按钮，用户可以用鼠标精准操作。

·移动端应该支持手势操作，如侧边栏，左滑删除，下拉刷新等。

·PC端可以支持鼠标悬浮操作。
```

**2.布局**<br />页面上各模块在不同设备、不同分辨率上，应该有在不同的大小和比例。图片应该有不同的分辨率。
```
·模块应该能够自动调整大小和间距，以填满整个页面。

·当页面尺寸变动较大时，能够合并模块。

·当页面尺寸变动较大时，隐藏正文预览、简介说明等较长的文本。

·图片在比例发生变化时依然美观可用。

·导航菜单保持逻辑清晰，同时部分菜单可隐藏或收起。
```

<a name="86864624"></a>
### 5.2 自适应视图
Axure RP的“自适应视图”功能可以用来实现响应式设计。默认情况下，Auxre RP的画布是没有高度和宽度限制的。使用“自适应视图”会以默认画布为“基类视图”，创建出同一个页面的子视图。<br />·子视图会继承基类视图的元件。元件的图片、文本内容和交互动作必须与基类视图保持一致，但尺寸、位置、样式等可以不同。<br />·子视图可以限制画布的高度和宽度。预览原型页面时，会根据浏览器的高度、宽度选择按哪个视图来显示。例如大于1024×768时显示基类视图，小于1024×768时显示子视图。<br />做响应式的原型时，可以先做好基类视图的布局，适配一个终端。然后在子视图中修改布局，适配另一个终端。这样，就能快速做出适配多个终端的原型。
<a name="ad30f551"></a>
#### 5.2.1 添加子视图
| （1）在项目菜单中选择“自适应视图”命令，如图示。 | ![屏幕快照 2019-04-08 下午5.30.14.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554715930600-3c22ef92-d9bd-4699-a74a-0c59f9967f2f.png#align=left&display=inline&height=178&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.30.14.png&originHeight=584&originWidth=614&size=278673&status=done&width=187) |
| --- | --- |
| （2）在弹出的“自适应视图”对话框中，可以看到基类视图的信息，包括名称和宽度、高度设置，如图所示。 | ![屏幕快照 2019-04-08 下午5.32.46.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554715978509-7a433624-af4a-470a-bf24-c9c9e761bb6e.png#align=left&display=inline&height=185&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.32.46.png&originHeight=472&originWidth=864&size=157831&status=done&width=338)

**·名称：**默认为“基本”。一般用来标识基类视图适配哪个终端。<br />**·宽、高：**基类视图是不限制宽度、高度的。这里的宽、高只影响画布上显示的辅助线。 |
| （3）单击添加（+）按钮，可以添加子视图，如图8-4所示。 | ![屏幕快照 2019-04-08 下午5.33.15.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554716007485-70c4d762-848b-41c3-acf9-59b59a8f4acf.png#align=left&display=inline&height=236&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.33.15.png&originHeight=676&originWidth=872&size=179807&status=done&width=304)

**·名称：**默认名称为“新视图”。<br />**·条件：**限制视图大于等于或者小于等于某个分辨率。<br />**·宽、高：**子视图的宽度、高度设置影响子视图的画布大小。可以只设置其中一个值。<br />**·继承于：**“新视图”继承于“基本”。子视图也可以再有子视图。在下拉列表框中可以选择基类视图或子视图。 |
| （4）将“新视图”设为宽度小于等于1024，单击“确定”按钮。 |  |
| （5）在页面的“属性”标签中，勾选“启用”自适应复选框，如图8-5所示。 | ![屏幕快照 2019-04-08 下午5.33.48.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554716037908-30cc21c5-a423-4ca8-a1f1-c95cbdd9a974.png#align=left&display=inline&height=216&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.33.48.png&originHeight=754&originWidth=750&size=259265&status=done&width=215) |
| （6）启用自适应之后，在页面标签下方会看到切换视图的按钮，如图8-6所示。 | ![屏幕快照 2019-04-08 下午5.34.17.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554716066340-e5db91a0-c632-4e6b-8eea-2d7fbc546add.png#align=left&display=inline&height=95&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%885.34.17.png&originHeight=302&originWidth=746&size=122736&status=done&width=234) |


<a name="6ccddcd1"></a>
#### 5.2.2 继承
子视图会继承父视图中的元件。继承的元件有些情况下是同步修改的，有些情况下不是同步修改的。下面详细介绍两者的关系。
```
1.父视图被修改，子视图随之修改


2.子视图中修改过的元件不再随父视图的修改而改变


3.在子视图中修改样式，父视图不随之修改


4.在子视图中修改文字、交互，父视图随之修改


5.“影响所有视图”复选框
如果勾选了“影响所有视图”复选框，那么在子视图中的所有修改，父视图都会随之改变。
```


<a name="4149694b"></a>
### 5.3、案例
[《响应式网站》](https://pan.baidu.com/s/1__WDiQv0EoMU3zmLlGUTNw)提取码: 2ize

<a name="874dcd60"></a>
## 六、交互动画
做交互动画是Axure RP的强项。简单的几步设置就可以让原型动起来，从而实现有创意的交互效果。用Axure RP做原型常常会引来设计师的惊呼：“快看！他的原型会动！”。
<a name="47e2d1cd"></a>
### 6.1　基础概念
<a name="809d6081"></a>
#### 6.1.1、了解4个概念
用户操作会“触发”交互动画“用例”，交互动画可以设置发生“条件”和具体“动作”。触发事件、用例、条件、交互动作四者的关系如图所示。<br />![屏幕快照 2019-04-08 下午7.32.59.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554723187779-90cf446c-56f5-47df-9aba-2f32c63cd5c1.png#align=left&display=inline&height=112&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.32.59.png&originHeight=376&originWidth=866&size=265621&status=done&width=259)

**1.触发事件**<br />生成原型网页后，Axure RP会监控每个元件的状态。若用户的操作改变了元件状态，则元件会向Axure RP报告自己被怎样操作了，发生了什么样的变化。这个过程就是“触发事件”。常见的触发事件有：元件被单击、元件被拖曳、元件失去焦点，元件大小改变等。<br />**2.用例**<br />发生触发事件后，Axure RP会检查有没有应对这个“触发事件”的应对方案。如果有，则执行应对方案。这个应对方案称为“用例”。用例是条件和交互动作的集合。<br />**3.条件**<br />条件是指执行用例中的交互动作前必须满足的前提。Axure RP在执行用例中的交互动作前，会先判断用例的条件是否满足，条件满足才开始执行用例。<br />**4.交互动作**<br />交互动作是指原型针对用户操作做出的反应。常见的交互动作有：移动元件、打开链接、显示/隐藏元件等。

<a name="4d370a6b"></a>
#### 6.1.2、触发事件
用户操作会产生触发事件，例如单击、拖曳等。<br />事件体现，如图：<br />![屏幕快照 2019-04-08 下午7.39.53.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554723674469-3018f6a3-5b35-48d1-9793-df1a35b74e6d.png#align=left&display=inline&height=119&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.39.53.png&originHeight=284&originWidth=862&size=145288&status=done&width=362)<br />事件有个特点，就是事件的名字都以“时”结尾。“事件”的作用如其名一样，可以用来控制交互效果发生的“时机”。

**1.元件变化产生的事件**<br />Axure RP中有很多种事件，下面先了解矩形元件有哪些事件。选中矩形元件，单击“更多事件”按钮，可以看到如图所示的菜单。<br />![屏幕快照 2019-04-08 下午7.42.03.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554723741089-b919bf61-66e1-4c3f-a155-aa78e411773e.png#align=left&display=inline&height=410&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.42.03.png&originHeight=928&originWidth=862&size=299736&status=done&width=381)

这些事件都相当的好理解。这里不做过多的介绍，希望大家多动手练习。

**提示：**<br />在手机上看原型时，手指单击相当于鼠标单击，手指长按相当于鼠标长按。<br />“矩形元件”中包含了大多数元件通用的事件。除此之外，一些特殊类型的元件会产生独特的事件。

2.一些特殊类型的元件产生的事件<br />·单选按钮元件会产生事件“选中时”“取消选中时”，如图所示。<br />![屏幕快照 2019-04-08 下午7.48.36.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724172673-778fc32d-0be8-4901-a315-a88c63e6aec1.png#align=left&display=inline&height=127&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.48.36.png&originHeight=316&originWidth=862&size=153433&status=done&width=347)<br />·在文本框元件中输入或删除文本会产生事件“文本改变时”，如图所示。![屏幕快照 2019-04-08 下午7.48.43.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724152147-80229806-43a8-4e22-b905-38d692f7a46e.png#align=left&display=inline&height=102&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.48.43.png&originHeight=210&originWidth=862&size=106604&status=done&width=417)<br />·动态面板切换状态会产生事件“状态改变时”，如图所示。<br />![屏幕快照 2019-04-08 下午7.48.53.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724194409-75f81ef5-2bb7-4b8e-8ea4-ba3235b7c0c6.png#align=left&display=inline&height=182&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.48.53.png&originHeight=314&originWidth=862&size=144255&status=done&width=499)<br />·动态面板被拖曳会产生事件“拖动时”，如图上图所示。

3.整个页面发生变化产生的事件<br />另外，整个页面发生变化也会产生事件，如图所示（单击页面空白区域可以看到页面的事件）。<br />![屏幕快照 2019-04-08 下午7.48.21.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724220571-cc5cc65f-a861-42ab-b139-f045c9263b96.png#align=left&display=inline&height=98&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.48.21.png&originHeight=338&originWidth=564&size=151966&status=done&width=164)<br />·“页面载入时”是指页面在浏览器中打开。<br />·“窗口改变时”是指浏览器窗口改变尺寸。

<a name="d21def90"></a>
#### 6.1.3、用例
Axure RP可以针对“触发事件”设置“用例”。一个用例代表一套交互流程。<br />下面看看“输入密码”的案例是如何设置用例的。

| （1）选中原型中的“下一步”按钮，在“属性”面板中的“鼠标单击时”上右击，在弹出的快捷菜单中选择“添加用例”命令，如图所示。 | ![屏幕快照 2019-04-08 下午7.54.09.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724525960-cab0b2d9-270c-45cc-b3a3-d5ded29a6f08.png#align=left&display=inline&height=232&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.54.09.png&originHeight=796&originWidth=862&size=428195&status=done&width=252) |
| --- | --- |
| （2）在弹出的设置窗口中，将“用例名称”改为“输入正确”，如图所示。然后用同样的方法再添加一个用例，并将“用例名称”改为“输入错误”。 | ![屏幕快照 2019-04-08 下午7.54.35.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724547991-b8b543ac-298b-448d-be3d-3e3e9aa441b2.png#align=left&display=inline&height=225&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.54.35.png&originHeight=1422&originWidth=2134&size=714989&status=done&width=338) |
| （3）在“属性”选项卡中可以看到改名后的两个用例，如图所示。 | ![屏幕快照 2019-04-08 下午7.54.59.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724560607-88dfc282-7be6-47c9-8198-0e52a2935401.png#align=left&display=inline&height=184&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.54.59.png&originHeight=468&originWidth=862&size=183272&status=done&width=338) |
| （4）设置了用例之后，元件右上角会出现一个序号，如图所示。可以通过“是否有序号”来快速辨识一个元件是否设置过用例。 | ![屏幕快照 2019-04-08 下午7.55.12.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554724571464-adba5458-2dba-42e1-960c-f62ea0401754.png#align=left&display=inline&height=96&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%887.55.12.png&originHeight=438&originWidth=798&size=78904&status=done&width=174) |

用例包括两部分，即执行用例的条件和具体的交互动作。条件和交互动作的设置方法在4.1.5节和4.1.6节中将详细介绍。

<a name="2cf9a8c4"></a>
#### 6.1.4　交互动作
Axure RP支持的交互动作主要分为以下5类。
```
·链接：打开新的网页链接，常用于实现页面间的交互。

·元件：改变元件的属性，如可见性、大小和位置等，常用于实现一个页面上的交互。

·变量：通过设置变量值来记录数据，如记录输入的文字、记录选项的状态等。

·中继器：通过操作“中继器”元件来管理数据，如在表格中添加一行数据、删除一行数据等。

·其他：等待、自定义事件等不属于前几类的交互动作都归在此类，后文案例用到这些事件时，会分别介绍。
```

由于Axure RP中的交互动作太多，所以不在这里一一介绍，而是分散在各个章节中介绍。

<a name="4a05a292"></a>
#### 6.1.5、条件
若一个触发事件有多个用例，通常要给用例设置“条件”。这样就能在不同情况下，执行不同的用例。<br />**1.“条件设立”界面介绍<br />![屏幕快照 2019-04-08 下午8.21.43.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554726424246-d5a079f2-75a7-4436-ac4e-16cec1d1e628.png#align=left&display=inline&height=358&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.21.43.png&originHeight=1256&originWidth=2110&size=1012569&status=done&width=602)**<br />下面介绍“条件设立”界面中的几个概念。

```
·焦点元件文字：当前焦点所在的元件上的文字。

·元件文字长度：元件上文字的字数。例如，想判断用户输入的是不是手机号，可以判断元件上文字的长度是否等于11。

·被选项：当前选中的下拉列表元件上的文字。

·选中状态：某个元件是否被选中。选中为true，未选中为false。

·面板状态：动态面板的当前状态。
例如，想判断开关是否打开，可以先在动态面板的状态1中画一个打开的开关，在状态2中画一个关闭的开关。
判断动态面板是否处于状态1，就相当于判断开关是否打开。

·元件可见：某个元件是否可见。可见为true，隐藏为false。

·按下的键：可以作为判断条件。例如，判断按下的键是不是Enter键，是否进入下一个页面。

·指针：就是鼠标光标的位置。可以判断光标是否进入某个元件的范围内。

·元件范围：元件所占的整片位置。可以判断元件范围是否与另一元件重合。

·自适应视图
```

条件的关系符号有以下10种。
```
·“==”表示“等于”。

·“！=”表示“不等于。

·“＜”和“＞”表示小于和大于号。

·＜=表示小于等于号。

·＞=表示大于等于号。

·“包含”：如字面意思，表示关系符号前面的文字中是否包含了后面的文字。例如，判断“邮件”文本框中是否包含@。
“不包含”的意义与之相反，较好理解，不再赘述。

·“是”：用来判断值的类型（文字、数字等）。例如，判断“手机号”文本框中是否都是数字。
“不是”的意义与此类似较易理解，不再赘述。
```

组合条件：Axure RP允许设置多个条件。
```
·图中右上角红色标注框中的按钮可以添加或删除一个条件。

·图中左上角的选项可以设置多条件整体成立的模式——多个条件同时符合，才算整体成立；
或者多个条件中只要有任意一个符合，就算整体成立。
```

**2.“if……else if……”结构**<br />条件语句一般分为两部分，即逻辑关系和条件内容。
```
如果有多个用例，if只能有一个，else if可以有多个：

·用例1 if XXX

·用例2 else if XXX

·用例3 else if XXX

·用例4 else if XXX
```

按从上到下的顺序，依次检查用例的条件，若条件满足，则执行用例并停止检查，否则继续检查后续的其他用例条件。

如果所有的条件都不满足，则一个用例都不会执行。为了避免这种情况，通常会将最后一个用例的条件内容设为true。例如：
```
·用例1 if XXX

·用例2 else if XXX

·用例3 else if XXX

·用例4 else if true
```

true永远表示条件成立，它可以用来“兜底”。即使用例1、用例2、用例3的条件都未满足，用例4也会被执行。

**3.“if……if……”结构**<br />if……else if……结构的用例，在执行时会依次检查用例的条件，并只执行第1个满足条件的用例。如果想实现“执行所有满足条件的用例”的效果可以使用“if……if……”结构。

“if……if……”结构的用例会根据各自的条件是否成立来决定该用例是否执行。最终可能执行其中一个，也可能所有用例都执行或所有用例都不执行。

<a name="12d45c30"></a>
### 6.2　动态面板
动态面板是一个容器，包含多个“状态”。状态上可以放置元件。一个状态就像一个页面，多个“状态”间可以动态切换，就能实现页面切换的效果。动态面板是最常用、最便于实现交互动画的元件。

<a name="40ff6ddf"></a>
#### 6.2.1　创建动态面板
在Axure RP中，可以直接从元件库中把动态面板拖曳到画布上。动态面板是一个容器，即动态面板是个“空壳”。在画布上，它应该是透明的。但是为了方便找到它，Axure RP给动态面板加了一层浅蓝色遮罩，如图所示。<br />![屏幕快照 2019-04-08 下午8.38.50.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727179763-6c6c1672-84e1-4933-ba79-168985ce6020.png#align=left&display=inline&height=170&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.38.50.png&originHeight=336&originWidth=870&size=111798&status=done&width=439)<br />除了直接拖曳，还有一种创建动态面板的方法是把多个元件“转换为动态面板”。
```
·如果已经知道动态面板应该做成多大尺寸，可以直接创建动态面板。

·如果开始不了解动态面板该有多大尺寸，那么可以先摆好元件，再把摆好的元件转换为动态面板。
```

全选元件，然后在右键快捷菜单中选择“转换为动态面板”命令，如图所示。<br />![屏幕快照 2019-04-08 下午8.39.07.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727211041-f13aab94-13a8-49b5-bf67-56701f95a0db.png#align=left&display=inline&height=62&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.39.07.png&originHeight=216&originWidth=842&size=126329&status=done&width=241)

转换为动态面板”其实自动干了两件事：
```
·一是创建了一个新的动态面板。

·二是把元件放在了动态面板的第一个“状态”里。
```

例如图中，矩形元件转换为动态面板后，被放在了动态面板的状态State1中。<br />![屏幕快照 2019-04-08 下午8.41.59.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727338319-7aaba752-6201-4887-99f6-f70272f0b5e6.png#align=left&display=inline&height=127&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.41.59.png&originHeight=210&originWidth=872&size=52676&status=done&width=528)

“转换为动态面板”操作是可逆的。“从首个状态中脱离”命令（如图所示）与之相反，可以让第一个状态中所有元件从动态面板中脱离，并删除第一个状态。如果动态面板只有一个状态，那么这个功能会将动态面板删除，将状态中的所有元件直接放在画布上。<br />![屏幕快照 2019-04-08 下午8.42.08.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727363781-54ace556-d4cc-4c1c-8b28-084c02d53a5c.png#align=left&display=inline&height=157&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.42.08.png&originHeight=596&originWidth=872&size=224996&status=done&width=229)

<a name="c0137e34"></a>
#### 6.2.2　动态面板的状态
动态面板是一个容器，包含多个“状态”。每个状态就像卡片盒里的一张卡片。盒子里可以有多张卡片，但只有最顶层的卡片可以被看到。<br />**1.状态的基本操作**<br />（1）添加状态<br />在状态上右击，在弹出的快捷菜单中选择“添加状态”命令（如图所示），可以添加多个状态，这里添加了3个状态（State1、State2、State3）。<br />![屏幕快照 2019-04-08 下午8.44.59.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727516351-8f2dcf45-a55e-47be-af84-1c518dca1935.png#align=left&display=inline&height=201&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.44.59.png&originHeight=656&originWidth=844&size=287905&status=done&width=258)<br />（2）查看状态<br />双击状态名称，即可进入“状态页面”查看状态。开始的每个状态都是空的，像其他页面一样，“状态页面”中可以添加元件。例如，图中，就在State1页面中添加了一个矩形元件。<br />![屏幕快照 2019-04-08 下午8.46.05.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727573520-cc955a1d-a360-4b1c-8a34-594ad6379712.png#align=left&display=inline&height=167&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.46.05.png&originHeight=404&originWidth=866&size=124349&status=done&width=359)<br />（3）复制状态<br />“复制状态”命令会生成一个新的状态，并复制原状态中的所有元件。例如，图中，复制State1会生成一个新的状态State4。而且，State4中已经包含了一个跟State1中一模一样的矩形元件。<br />![屏幕快照 2019-04-08 下午8.47.43.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727673262-c5950808-8da0-43c8-8aa2-0252a25e0eb4.png#align=left&display=inline&height=166&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.47.43.png&originHeight=310&originWidth=866&size=141405&status=done&width=465)<br />**2.状态的显示特性**<br />动态面板同一时间只显示最上层的状态。下面我们来试一试。<br />（1）将State4中的矩形元件上的文字改为B。回到index页面，可以看到动态面板显示的是State1，如图所示。<br />![屏幕快照 2019-04-08 下午8.48.36.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727740873-431d211c-6de9-4893-9dd1-e3135b68a72a.png#align=left&display=inline&height=157&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.48.36.png&originHeight=338&originWidth=876&size=107983&status=done&width=407)<br />（2）如图所示，调整动态面板的状态顺序，现在是State4处于最上层。相应的，画布上动态面板显示的不再是State1，而是State4。<br />![屏幕快照 2019-04-08 下午8.48.45.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554727786487-3340c440-a76f-4e28-9d72-71aa1ce0d789.png#align=left&display=inline&height=149&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.48.45.png&originHeight=322&originWidth=876&size=105207&status=done&width=405)

**提示：**<br />切换动态面板的状态，就能改变动态面板显示的页面。利用这个特性可以实现很多交互效果。例如，轮播图、标签页等。后文的案例中将有更多的说明。

<a name="79349a3a"></a>
#### 6.2.3、调整动态面板的尺寸
动态面板像一个窗口，状态页面是窗外的风景。动态面板的尺寸大小控制着状态页面的可视范围。动态面板越大，状态页面的可视范围越广。<br />**1.默认尺寸**<br />默认情况下，动态面板自动调整为状态页面的大小，使状态页面完整显示。Axure RP中的元件大小根据内容自动调整时，元件四周的拖曳块是黄色的；元件大小由手动调整时，四周的拖曳块是白色的。默认情况下选中动态面板后如图所示。<br />**2.手动调整尺寸**<br />“手动拖曳动态面板可以直接改变其大小。无论如何拖曳，状态页面的左上角是固定的。动态面板尺寸缩小之后，状态页面左上角与动态页面左上角对齐，从右下侧开始隐藏。<br />**3.自动调整尺寸**<br />手动缩小尺寸后，再想调回“按内容自动调整大小”，有两个办法，一是鼠标双击元件四周的拖曳块；二是从右键快捷菜单中选择“自动调整为内容尺寸”命令，如图所示。<br />![屏幕快照 2019-04-08 下午8.54.53.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554728116655-3c8cf442-bb05-40a6-b9d4-f4c70ab70d7d.png#align=left&display=inline&height=121&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.54.53.png&originHeight=378&originWidth=860&size=198065&status=done&width=276)<br />**4.100%宽度**<br />动态面板还有个特殊功能，即“100%宽度”，如图上图所示，可以让动态面板的宽度与展示原型的浏览器宽度相同。动态面板设置为“100%宽度”之后，在画布上不会立即看到效果，当原型展示在浏览器中时才能看到效果。

<a name="7798b543"></a>
#### 6.2.4、拖曳
动态面板是唯一可以响应“拖曳”操作的元件。APP原型中拖曳操作比较多，例如上/下翻列表、左滑返回上一页等。这些交互效果只能由动态面板来实现。<br />**1.拖曳相关的触发事件**<br />下面先看一下动态面板中与拖曳操作相关的触发事件，如图所示。<br />![屏幕快照 2019-04-08 下午8.56.58.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554728245833-8b772e2e-788e-49d9-b790-724d9626254b.png#align=left&display=inline&height=121&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%888.56.58.png&originHeight=574&originWidth=604&size=364575&status=done&width=127)<br />Axure RP把“拖曳”操作的整个过程分解成了3个阶段，每个阶段对应一个触发事件。<br />（1）拖动开始时：鼠标按下的瞬间触发这个事件。如果拖曳交互效果比较复杂，可以在这个事件中处理一些准备工作。<br />（2）拖动时：鼠标按下并持续按住时，整个持续时间段内会不断触发这个事件。通常用来实现“鼠标拖曳，元件随之移动”的效果。例如上下拖曳列表，拉出侧边栏等。<br />（3）拖动结束时：持续按住鼠标一段时间后，在松开的一瞬间会触发这个事件。通常用来实现“松开鼠标，元件回弹”的效果。例如，下拉刷新、iOS列表的弹性效果等。<br />“拖动结束时”还有两个特殊的变体。Axure RP会在拖动结束时，自动识别拖曳的方向。根据拖曳是向左或向右，进一步分出两个事件。
```
·向左拖动结束时：按住鼠标，向左拖曳一定距离然后松开鼠标，在松开的瞬间触发这个事件。

·向右拖动结束时：按住鼠标，向右拖曳一定距离然后松开鼠标，在松开的瞬间触发这个事件。
```

无论拖曳路径多复杂，都会触发“拖动结束时”事件。但只有水平向左/右拖曳才会触发“向左/右拖动结束时”事件。这两个事件可以快速实现一些简单的滑动效果。例如，左右滑切换轮播图等。

**2.举例讲解拖曳效果的实现**<br />“鼠标一边拖曳，元件一边随之移动”是最常见的交互效果。下面介绍如何实现这个效果。<br />在动态面板的“拖动时”事件中添加用例Case1，然后添加动作“移动”。选择“当前元件”为要移动的元件，移动方式选择“拖动”，表示动态面板跟随鼠标拖曳而移动。这样就实现拖曳元件的效果了。

**3.拖曳的多种移动方式**<br />除了“拖动”之外，“移动”动作还可以配置其他移动方式。而且，在“拖动开始时、拖动时、拖动结束时”等事件中，可以选择的移动方式是不同的。

“拖动开始时”可以选择“到达”“经过”，如图所示。两种方式都带有x、y两个参数，不过两种方式下，参数的含义不同。<br />![屏幕快照 2019-04-08 下午9.04.09.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554728691637-192b5d03-d763-4ef4-9c91-f0fcb5e037bd.png#align=left&display=inline&height=97&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%889.04.09.png&originHeight=304&originWidth=852&size=168709&status=done&width=273)
```
·“到达”方式下，x、y表示“移动到”坐标值为x、y的位置。

·“经过”方式下，x、y表示向右移动x像素，向下移动y像素。x、y为负数时，向反方向移动。
```

“拖动时”可以选择的，除了“到达、经过”移动方式，还有“拖动、水平拖动、垂直拖动、回到拖动前位置”移动方式，如图所示。默认选择“拖动”移动方式。<br />![屏幕快照 2019-04-08 下午9.04.21.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554728674487-c60ee08d-7d8b-443b-a474-dd40bd4856ee.png#align=left&display=inline&height=147&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-08%20%E4%B8%8B%E5%8D%889.04.21.png&originHeight=498&originWidth=376&size=98955&status=done&width=111)
```
·拖动：要移动的元件随着鼠标光标而动，光标走过多少距离，元件就走多少距离。

·水平拖动：要移动的元件只在水平方向上随着光标移动。

·垂直拖动：要移动的元件只在垂直方向上随着光标移动。
```

“拖动结束时”与“拖动时”可以选择的移动方式一样。默认选择“回到拖动前位置”。
```
·回到拖动前位置：元件移回按下鼠标，拖曳开始的瞬间的那个位置。
```

<a name="0dc3e593"></a>
### 6.3、案例
《轮播图》<br />《切换标签页》<br />《侧边栏》<br />《通知》<br />《自动弹出键盘》<br />《优化的注册流程》<br />《锤子开机解锁》<br />《企业网站》

[案例下载](https://pan.baidu.com/s/1f52lvsbx-aauy2dbW8n-oQ) 提取码: n3ts
