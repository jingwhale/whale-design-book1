# Whale Kit

Whale Kit是Whale Design的重要组成部分，它是一个基于高效设计理念的快速原型工具，基于Sketch开发。它包含三部分：一是 Base Components，包含原型最基础的组件；二是交互业务，如自动添加修订记等；三是根据需求生成交互说明。特点是，能够快速的构建基础交互原型。  
![poster.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1555131317704-28867ce1-387a-44aa-8de6-47963f04fa4d.jpeg#align=left&display=inline&height=303&name=poster.jpg&originHeight=1116&originWidth=1814&size=186954&status=done&width=492)

**主要功能如下：**  
1、快速插入原型交互组件  
可快速构建页面与模块布局。上下布局、左右布局等。有时候，我们需要确定基础的布局，才进行进一步的页面的设计。布局通过线框实现页面与模块的布局。  
可快速插入图片、轮播图、按钮、头像、表格、标签、状态切换等交互组件。

2、快速实现交互说明

3、将现有的视觉库转化为原型库  
Convert to Grayscale用于将矢量形状转换为灰度颜色。 非常适合摆脱那些彩色线框或徽标墙。 适用于多个填充，边框和渐变。  
目前支持Shape、ShapePath、Text、Group以及symbol类型图层，对image图层暂时不支持。

4、插入网页到Artborad中  
将网页通过地址的方式直接插入到Artborad中，可通过配置插入页面的局部到Artborad中。

5、可以快速生成二维码  
填入二维码的内容，可以快速生成矢量二维码，并插入选中的区域中。

6、快速制作页面流程  
可以快速的生成页面流程图的页面。完整的页面流程图实现需要和Use Flows结合使用。

7、自动生成交互的封面

## 一、布局（Make Layout）

布局需要一个矩形容器，首先使用快捷键r建立一个矩形，然后使用快捷键“shift control a”打开设置面板，有等比和比例2种设置方式：

有等比设置界面：  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-04-01 &#x4E0A;&#x5348;2.07.45.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554055730228-298c5f5d-cae2-483b-b9fc-c0c3b2d72bf4.png#align=left&display=inline&height=252&name=屏幕快照%202019-04-01%20上午2.07.45.png&originHeight=582&originWidth=930&size=71874&status=done&width=403) 

不等比设置界面  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-04-01 &#x4E0A;&#x5348;2.09.55.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554055804446-243180e6-a16f-4de2-ad9b-1117915ffe62.png#align=left&display=inline&height=252&name=屏幕快照%202019-04-01%20上午2.09.55.png&originHeight=582&originWidth=930&size=75956&status=done&width=402)

### 1.1、上下布局

![upDownLayout.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1554451877517-12b0fa38-b49b-4a12-9cc5-a16d321d5eaf.jpeg#align=left&display=inline&height=125&name=upDownLayout.jpg&originHeight=346&originWidth=1172&size=21719&status=done&width=424)

### 1.2、左右布局

![leftRightLayout.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1554451890062-1b40bb01-4d34-421a-b473-1dcf8f6df569.jpeg#align=left&display=inline&height=114&name=leftRightLayout.jpg&originHeight=304&originWidth=1172&size=20609&status=done&width=441)

### 1.3、制作三栏ArtBoard交互布局

选中一个ArtBoard，使用快捷键“shift control a”，以选中ArtBoard的尺寸生成三栏，分别为页面、交互说明、状态界面，如下（iphone 8为例）：  
![iPhone 8.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554086713377-f1bdea09-388f-4ab5-aa93-a1f770e5e221.png#align=left&display=inline&height=339&name=iPhone%208.png&originHeight=667&originWidth=1050&size=18232&status=done&width=534)

这种三栏布局适合移动端交互或者功能设计交互使用，交互示例：  
![Screen Shot WebView &#x8BBE;&#x8BA1;.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554086944742-0cff7530-7ea0-41f1-9603-9e7a50d86a50.png#align=left&display=inline&height=632&name=Screen%20Shot%20WebView%20设计.png&originHeight=2038&originWidth=2404&size=494884&status=done&width=746)

### 1.4、Tab标签

![tab.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1554451984941-8a0779f7-26de-4ec9-95e6-cc5ec71d7694.jpeg#align=left&display=inline&height=42&name=tab.jpg&originHeight=98&originWidth=770&size=6563&status=done&width=330)

### 1.5、表格

### ![table.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1554452057639-9f801fb9-b2d7-4ec4-8a8e-ea4748635454.jpeg#align=left&display=inline&height=141&name=table.jpg&originHeight=362&originWidth=912&size=25589&status=done&width=354)

## 二、页面流程图（Flow Page）

页面流程图可以帮助理清页面之间的逻辑关系。[DEMO](https://www.yuque.com/jingwhale/component/artboards/59670)。  
在page内，直接使用快捷键“shift control option p”，可生成Page Flow的页面。详细请查看[《页面流程画图工具的设计与实现》](https://www.yuque.com/jingwhale/blog/eshtvp)  
![Page Flow Demo.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1555243354636-3a6bd089-e3ae-4f35-8220-06e7ea5f9903.png#align=left&display=inline&height=284&name=Page%20Flow%20Demo.png&originHeight=852&originWidth=1640&size=64199&status=done&width=547)

组件会自动为当前布局或场景分组，各个布局可以嵌套使用。  
Whale Kit提供的是基础组件，需要结合Sketch的快捷键使用，共同实现高效交互原型。

## 三、Web Page Screen Shot

在Sketch的Artboard中插入网页截图：  
1）、输入网址，自动截图到Artboard中，并居中显示；  
2）、可截取网页局部图片  
具体详情请查看[《](https://www.yuque.com/jingwhale/blog/ps6xzi)[Sketch网页截屏插件设计开发](https://www.yuque.com/jingwhale/blog/ps6xzi)[》](https://www.yuque.com/jingwhale/blog/ps6xzi)。

### 3.1、使用

1）在ArtBoard上，使用快捷键：“shift control option j”，调出插件的webview；  
2）填写ArtBoard的名字，默认为“修订记录”  
![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554012951583-360418f4-4e17-4a66-84e7-d97b1ede18e4.png#align=left&display=inline&height=260&name=image.png&originHeight=702&originWidth=806&size=67656&status=done&width=299) 

### 3.2、截图类别

| 截取某个Url的整个页面 | 填写Page Url，点击Insert Page，等待截图插入ArtBoard的即可。 |
| :--- | :--- |
| 截取截取某个Url的页面的一部分 | 在Page Url填入页面的地址，点击Page part，再点击Custom自定义输入要截图部分的类名字，点击点击Insert Page，等待截图插入ArtBoard的即可。 |
| 使用github的git commits作为修订记录 | 在Page Url填入github的仓库地址，点击Page part，默认就是截取git commits页面git commits列表的区块，无需要其他操作，点击点击Insert Page，等待截图插入ArtBoard的即可。 |

### 3.3、截取Goole 翻译的翻译框示例

截取截取某个Url的页面的一部分，截取Goole 翻译的翻译框示例：  
1\)、在ArtBoard上，使用快捷键：“command option shift j”，调出插件的webview；  
2）、填写ArtBoard的名字，默认为“Goole 翻译框”  
3）、在Page Url填入页面的地址  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-03-31 &#x4E0B;&#x5348;2.20.33.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554013345759-f9e0cab1-47f1-4af5-9f85-2f516423971a.png#align=left&display=inline&height=241&name=屏幕快照%202019-03-31%20下午2.20.33.png&originHeight=702&originWidth=806&size=77757&status=done&width=277)

4）、点击Page part，再点击Custom自定义输入要截图部分的类名字  
首先，找到要截图部分的类名字  
第一步，chrome中使用快捷键“fn+f12”打开开发者工具，或者右击点击“查看打开”；  
第二步，通选选择箭头找到区域的class name，复制下来  
![Xnip2019-03-31\_14-27-17.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1554013768220-b8549fee-50b6-447d-879d-07bca52d030c.jpeg#align=left&display=inline&height=290&name=Xnip2019-03-31_14-27-17.jpg&originHeight=1846&originWidth=3104&size=776711&status=done&width=487)  
其次，将class name复制到Custom里  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-03-31 &#x4E0B;&#x5348;2.20.44.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554013783154-4dcb89d3-b445-4f23-aa91-0bc156b7d34c.png#align=left&display=inline&height=268&name=屏幕快照%202019-03-31%20下午2.20.44.png&originHeight=702&originWidth=806&size=84983&status=done&width=308)

5）、点击点击Insert Page，等待截图插入ArtBoard的即可。  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-04-11 &#x4E0B;&#x5348;7.37.10.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554982644196-5fe58fb2-dc7a-4f67-8cfd-625773ba8b72.png#align=left&display=inline&height=251&name=屏幕快照%202019-04-11%20下午7.37.10.png&originHeight=1442&originWidth=2708&size=265159&status=done&width=472) 

## 四、Convert to Grayscale

一个简单的Sketch插件，用于将矢量形状转换为灰度颜色。 非常适合摆脱那些彩色线框或徽标墙。 适用于多个填充，边框和渐变。

目前支持Shape、ShapePath、Text、Group以及symbol类型图层，对image图层暂时不支持。

### 4.1、使用

**1）、选中区域**  
选中区域类型包括Shape、ShapePath、Text、Group、Artboard以及symbol;  
选中要变灰色的图层，使用快捷键“control option shift g”，等待完成即可。

**2）、page**  
选中文档中的page页面，使用快捷键“control option shift g”，等待完成即可。

Symbols page是page的一种特殊情况，用法与page相同。需要选中库的Symbols page页面。

**3）、全部document**  
不选中任何page、图层，直接使用快捷键“control option shift g”，等待完成即可。

### 4.2、技巧：

由于Convert to Grayscale算法使用了较多的循环遍历操作和样式赋值操作，当图层较多时，用时会较长  
1）请尽量选择需要改变颜色的图层，避免多余的图层  
2）适当选择合适的Convert to Grayscale 类型：

| part | 选中图层 选中区域类型包括Shape、ShapePath、Text、Group、Artboard以及symbol |
| :--- | :--- |
| page | 选中单个页面，不选中任何图层 |
| symbols page | Symbols page（page的一种） 一般将视觉的Symbols库的symbol转变为灰色的交互Symbols库。 |
| Artboart | 选中画板 |
| Group | 选中分组 |
| all | 全部document 请谨慎使用，当图层较多时，可能会等待很长时间，甚至导致Sketch以外退出。 |

## 五、常用交互组件

### 5.1、图片相关工具（Operate Image）

布局需要一个矩形或圆形容器，使用快捷键“shift control q”。Whale Kit会自动判别图形类别以生成不同的原型组件：矩形（快捷键r）会生成图片原型组件，椭圆矩形（快捷键u）会生成轮播原型组件，圆形（快捷键o）会生头像原型组件。

**1）、图片**  
![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554452264576-14529714-873a-4a4b-9a0d-91b4c1fb01ea.png#align=left&display=inline&height=109&name=image.png&originHeight=302&originWidth=786&size=14574&status=done&width=284)

**2）、轮播图**  
![lunbo.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554982326031-2edfffbc-0956-4a72-90a6-2f4e7641416f.png#align=left&display=inline&height=112&name=lunbo.png&originHeight=310&originWidth=786&size=19454&status=done&width=284)

**3）、头像**  
![icon.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554452298500-9af6edf3-0b08-42b8-9c98-ab2bd17d84b3.png#align=left&display=inline&height=82&name=icon.png&originHeight=248&originWidth=258&size=23693&status=done&width=85) 

### 5.2、按钮（Generate Button）

布局需要一个矩形容器，首先使用快捷键r建立一个矩形轮廓，然后使用快捷键“shift control z”。  
![button group.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554452320973-ca2a76f5-5230-45ca-896d-0dfe6f6cd39e.png#align=left&display=inline&height=40&name=button%20group.png&originHeight=96&originWidth=402&size=3438&status=done&width=167) 

### 5.3、状态变换

![toggle state.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1554452977354-7b1c5fe5-d5f1-4b86-9ab8-0c63e2fec271.jpeg#align=left&display=inline&height=68&name=toggle%20state.jpg&originHeight=152&originWidth=742&size=14074&status=done&width=334)

**1）、active状态**  
支持的类型有Group、Shape、ShapePath、Text等。  
直接选中图层，使用快捷键“control option shift k”，选择active。图层激活后整体颜色加深。  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-04-11 &#x4E0B;&#x5348;7.30.31.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1554982241080-ca7cef45-ba29-416a-a713-c67120e950ae.png#align=left&display=inline&height=146&name=屏幕快照%202019-04-11%20下午7.30.31.png&originHeight=318&originWidth=822&size=104743&status=done&width=377)

**2）、disabled状态**  
直接选中图层，使用快捷键“control option shift k”，选择disabled，即可。图层disabled后整体颜色减轻。

### 5.4、Generate QR Code

选中一个矩形，使用快捷键“ctrl shift option q”，填入二维码的内容，点击“OK”即可。二维码形状为方形，边长是选中矩形的宽度和矩形的长度二者中的最大值。  
![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-04-13 &#x4E0B;&#x5348;11.06.31.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1555168399041-69e55d01-584f-4708-872d-eff0191d5405.png#align=left&display=inline&height=132&name=屏幕快照%202019-04-13%20下午11.06.31.png&originHeight=294&originWidth=824&size=37971&status=done&width=369)  


二维码展示如下：  
![www.jingwhale.cc.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1555224392922-b6266713-5c76-4d30-832d-ebdbf923e79d.jpeg#align=left&display=inline&height=121&name=www.jingwhale.cc.jpg&originHeight=394&originWidth=394&size=57237&status=done&width=121)  


### 5.5、Generate Cover

选中一个ArtBoard，使用快捷键“ctrl shift option c”，输入封面信息，如下图：

![&#x5C4F;&#x5E55;&#x5FEB;&#x7167; 2019-04-20 &#x4E0B;&#x5348;10.59.10.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1555772365302-96df265a-63a0-4fc0-b5be-8b702ab9cc1a.png#align=left&display=inline&height=224&name=屏幕快照%202019-04-20%20下午10.59.10.png&originHeight=572&originWidth=808&size=64366&status=done&width=317)

填写完封面数据后，点击“Generate Cover”按钮，即可生成封面：  
![&#x5C01;&#x9762;.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1555772447881-41497fff-47b0-4e1f-a5be-c7cd7edb733a.png#align=left&display=inline&height=406&name=封面.png&originHeight=1024&originWidth=1440&size=44160&status=done&width=571)

## whale-kit

[https://github.com/jingwhale/whale-kit](https://github.com/jingwhale/whale-kit)

