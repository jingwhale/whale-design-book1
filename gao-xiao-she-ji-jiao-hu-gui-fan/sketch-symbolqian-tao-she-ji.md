# Sketch Symbol嵌套设计

根据不同使用场景的需求，将symbol分别分为是control symbol、nested symbol 和 variables symbol三类，管理层级大概可以简化为：Control symbol— nested symbol—variables symbol。

不同类别之间互相嵌套使用，可以：  
1）保持设计的一致性，利于规范UI guide（有时候大体量设计稿出来不同symbol之间的本该一样的细节也有细微差别）  
2）简化symbol的使用方式、快速选用  
3）更改按钮或组件不同状态的样式时避免过多的重复工作

![Xnip2019-03-27\_15-50-04.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1553673034874-1622387f-6da8-4df1-890a-3b6e99e801af.jpeg#align=left&display=inline&height=847&name=Xnip2019-03-27_15-50-04.jpg&originHeight=1420&originWidth=1250&size=202114&status=done&width=746)

上图在用可视化的方式在symbol的page里给不同的symbol做了归类，乍看是三个不同的类别，但其实是互相嵌套的。

## 一、symbol三种类型

### Control symbol

control部分是产品中中所涉及的功能组件，比如文本输入框（input）、复选框单/选按钮。这是一个总的大类。

### Nested symbol

这里面是上述control中每一个symbol的feature在UI中会出现的不同状态，有默认的样式，选中状态，报错状态，输入后的状态等（同理在按钮设计时就会有悬浮／选中／不可用之类的）。

### Variables symbol

针对按钮中的可复用的变量所设的类别，拿图中举例，Variables第一个灰色矩形框的symbol（input），这个样式分别可以被Nested 里面第一列前两个（默认和value状态）和第二列第前两个（默认和selected状态）中的灰色边框所复用。

## 二、工作原理

control用来划分大类，比如有一个文本输入框，在control中只看到的是它的默认样式，它有不同的状态1234（选中／不可用／报错等），每一个control symbol下面其实隐藏了不同状态下的这个文本输入框，1234都在，只是不可见，只显示默认的状态，这一层称为type。下图是一个control symbol 里所包含的图层  
![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553672837689-eb2a54ec-2952-4a63-91bd-08116d46055c.png#align=left&display=inline&height=315&name=image.png&originHeight=692&originWidth=396&size=68837&status=done&width=180)

### 【第一层嵌套】

图中只有type图层可见，下面都是各种状态下的文本输入框，也即是说，这个nested 部分平铺展示出来每个symbol的状态其实也隐藏在所对应的control symbol 里的，这样每次需要使用某一个功能时，只用在control symbol里找到它默认type的那个symbol直接置入，然后在设计稿里把需要的那个symbol状态图层调成可见，而不是在成堆的symbol样式里来回肉眼搜索。

### 【第二层嵌套】

在刚刚上面的的variables 里面有解释，symbol之间有些变量（例如背景颜色，边框颜色粗细）是在整个设计系统里不断复用的。  
为了避免每次新建一个symbol之前都要手动去设置这些通用的参数，把这些变量预存为symbol，直接使用，然后放在nested symbol里锁住这个图层，这样在overrides里就不会出现这个变量以防不小心更改。即节省了多次重复设置的时间，也避免了因为一些记忆偏差或手残导致的误差而出现的不一致。

## 三、示例

![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553673626354-a354845b-5a65-47df-821b-2e5fb10ceb2b.png#align=left&display=inline&height=295&name=image.png&originHeight=600&originWidth=800&size=55332&status=done&width=393)

示例下载：[https://sketch.cloud/s/RdpOl](https://sketch.cloud/s/RdpOl)

## 四、symbol的自动化创建

由于单一control symbol建立，嵌套牵涉到大量的重复元素，并且创建具有一定的规律性，可考虑使用代码实现Nested symbol创建。具体做法如下：手动建立variables symbol（variables symbol本省也可由程序建立）和基础的type control，其他状态的Nested将定义好的variables symbol和type control参数参入自动化symbol程序，由自动化symbol程序生成其他状态的Nested。

### 自动化symbol工作流程：

1、自动化建立variables symbol。由variables symbol程序生成颜色等variables symbol。  
2、手动建立control symbol。  
3、依据variables symbol和control symbol自动化建立Nested symbol。由Nested symbol程序生成Nested symbol。

