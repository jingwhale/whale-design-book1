# 建立一套设计规范组件库

<a name="afd185c7"></a>
## 1、什么是库
<a name="2d314055"></a>
### 1.1、Library 介绍
Library 其实只是一个普通的 Sketch 文件，其中包含 Symbol，你可以在其他 Sketch 文件中使用此 Symbol。如果您更新 Library 文件中的任何一个 Symbol，你都会收到更新通知，利用 Library，团队成员们可以在 Sketch 文件之间共享 Symbol，并使其更新以始终保持同步。

<a name="2b96f302"></a>
### 1.2、模版与库
模版（Template）与库（Library）本质上并无区别，都是一个普通的 Sketch 文件，除了低版本（低于 43）Sketch 建立的文件无法直接加入到库面板中外，任何带有组件（Symbols）的 Sketch 文件都可以直接加入库面板。<br />有时模版特指被加入到菜单 「New From Template」 下或显示在 Welcome 界面上的那些文件。可以使用 「Save as Template…」 菜单或者直接将文件复制到 「~/Library/Application Support/com.bohemiancoding.sketch3/Templates」 文件夹内。

库则是指被添加到 「Preferences – Libraries」 面板下的那些文件，它们没有统一保存的地方。

在没有引入库功能时，设计团队使用模板文件来协作，但 Sketch 并未提供一种文档内容更新机制，只能依赖一些插件将文档通过组件名称匹配来替换成另一个文件的组件，但这对组件图层命名要求严格，也没有可视化对比。库功能解决了这种公共内容更新或替换的需求，这一点在团队协作中非常重要。

库并没有取代模版的意思，从界面上只能访问到库文档内的组件，也就是库文档内的画板（Artboard）或不在画板内的图层，对于库实际上没有太多用处的，有些库是程序生成的，这种情况组件在画布上的位置也没有太多讲究。模板文档则会带有一些实例或说明，模板内的组件也可以都替换成库的外部组件，模板也可以为库提供直观的检索、示例演示或者作为一个快速搭建界面的框架。

<a name="5209561f"></a>
### 1.3、Library类型
<a name="f89282a4"></a>
#### 1.3.1、内置库（Internal Libraries）
是指随 Sketch 自带的库，如， iOS UI Design 这个库，文件保存在 「/Applications/Sketch.app/Contents/Resources/libraries/iOS UI Design.sketch」。

<a name="070c2972"></a>
#### 1.3.2、用户库（User Libraries）
就是用户从库面板上的 「Add Library…」 按钮上添加的库。

<a name="230aa241"></a>
#### 1.3.3、远程库（Remote Libraries）
内置的需要下载的 Apple iOS UI 也属于这个类型。目前这个功能仅开放了从 Sketch Cloud 添加库，用户需要注册 Sketch Cloud 上传文件，分享页面链接给使用者，使用者页面上的 「Download – Add Library to Sketch」 菜单添加到库面板。

<a name="827e4add"></a>
### 1.4、Library 协同
在设计团队中，多人协作是必然情况，那么如何使通用模块和控件始终保持一致呢？我们只需将 Librar 文件存放在一个固定的地方，例如云盘、公司内部网盘等位置，将通用的控件以及模块存放在其中，然后其他设计师就可以轻松调用了。当这个 Librariy 有任何修改，并更新到你的本地，你都可以接收到更新通知。

通常情况下，我们会将公司产品的设计规范、通用模块和控件做成 Library 文件，让团队内的其他设计师进行调用。一般里面包括颜色、图标、文字、还有其他模块控件等。团队的设计师可以充分利用 Library 来让自己文件里面的 Symbol 始终保持最新，以及和团队成员保持一致。但是由于任何设计师都可以对 Library 文件进行编辑，所以我们要将 Library 进行安全的分离，对 Library 的编辑只能在特定的位置、特定的文件，甚至特定的人进行，因此一般不会有不相关的编辑。如果一旦不小心无意进行了修改一定要及时修改回来，不然团队内的其他设计师的文件就会出问题。

下面就分享一下如何利用创建一个 Library协同。
<a name="70d5a8a3"></a>
#### 1.4.1、Sketch Cloud
利用Sketch Cloud实现，具体步骤如下：<br />1）上传Librariy 到Sketch Cloud<br />![Xnip2019-03-23_20-38-54.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1553344749442-1ee1ad66-9089-4651-b13a-74851407f34a.jpeg#align=left&display=inline&height=241&name=Xnip2019-03-23_20-38-54.jpg&originHeight=1800&originWidth=2880&size=323562&status=done&width=386)

2）设置勾选Use as Library<br />![Xnip2019-03-23_20-38-31.jpg](https://cdn.nlark.com/yuque/0/2019/jpeg/120638/1553344764907-7b17a2e9-4050-4230-bb23-0c80befda2d9.jpeg#align=left&display=inline&height=470&name=Xnip2019-03-23_20-38-31.jpg&originHeight=1288&originWidth=1014&size=126736&status=done&width=370)

3）下载，Add Library to Sketch<br />打开连接，点击Add Library to Sketch<br />![屏幕快照 2019-03-23 下午8.40.35.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553344857504-b9692a10-bd3c-42bf-824e-2c74a95e7ef6.png#align=left&display=inline&height=305&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-03-23%20%E4%B8%8B%E5%8D%888.40.35.png&originHeight=1288&originWidth=1982&size=506848&status=done&width=470)

<a name="aa822013"></a>
#### 1.4.2、坚果云协同
原理是利用坚果云的多人同步功能。坚果云会把你的文件夹同步到服务器中，同时也可以同步到你同事的电脑中。具体操作如下：<br />1）共享者新建需要同步共享的文件夹<br />![屏幕快照 2019-03-23 下午8.25.41.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553343957116-9e98f9d1-b4aa-4021-b3a7-30841fc2f484.png#align=left&display=inline&height=410&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-03-23%20%E4%B8%8B%E5%8D%888.25.41.png&originHeight=1194&originWidth=754&size=102155&status=done&width=259)<br />2）共享者设置需要的同步的账户<br />点击小人图标，邀请共享人<br />![屏幕快照 2019-03-23 下午8.15.53.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553343420105-c3933a07-4ac2-4da4-a74f-ddddb1e29ab0.png#align=left&display=inline&height=246&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-03-23%20%E4%B8%8B%E5%8D%888.15.53.png&originHeight=818&originWidth=992&size=80022&status=done&width=298)<br />3）被共享者接受同步文件夹<br />![屏幕快照 2019-03-23 下午8.10.26.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553343470001-64a14a60-9524-41ca-84a5-df6bbf4ff311.png#align=left&display=inline&height=127&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-03-23%20%E4%B8%8B%E5%8D%888.10.26.png&originHeight=190&originWidth=424&size=46401&status=done&width=284)

协同者Add Library 按钮选择存放在坚果云的 sketch 文件，这样 Library 文件已经添加成功，我们就可以轻松的访问我们 Library 里面的控件了。

如果有人对我们的 Library 文件进行了编辑，那我们会在自己使用 Library 文件中收到更新提示，我们可以根据自己的需求选择是否更新 Symbol。

<a name="afcf844d"></a>
### 1.5、库组件如何从关联的库更新
在介绍库更新机制前，需要简单了解下 Sketch 内部是如何识别对象的。在 Sketch 中创建的任何对象，新建一个文件、插入一个图层、创建一个样式等等，Sketch 都会给这些对象添加唯一标识 UUID。图层上的 UUID 这里称为图层 ID，组件上的 UUID 称为 组件 ID（SymbolID），组件母版和组件实例都即有图层 ID 也有 组件 ID。ID 信息在界面上没有体现，设计使也不会用到这些信息，它们是作为 Sketch 文档结构上使用的。

库组件并非真实的链接，你将包含外部组件的文档发给其他人，并不会出现坏链导致文档错误，实际上这些数据都保存在当前的文档中，所以使用外部组件不会使文档体积减小，它的优势在于更新机制。库组件也没有保存库的路径，它记录了库名、库 ID 和组件原始 ID（Remote SymbolID， 组件在它的库中的 SymbolID），库的名称显示在属性面板和外部组件管理面板上，库 ID 没有在界面上体现出来。

库组件自动更新，其实就是 「库列表」 – 「库 ID」 – 「外部组件原始 ID」 这三者的关联。通过库组件的库 ID，从库面板的列表中，按照添加的时间从新到旧依次检索所有未被禁用的、链接完好的库，直到匹配到库 ID ，然后查找该库文件内是否有与库组件 SymbolID 匹配的组件，如果包含并且内容有差异就提醒更新，更新的过程实际上就是内容替换。如果这个库文件没有与之匹配的组件，还会接着从另一个相同库 ID 的库文件内检索。如果某个环节没有结果，这个组件就不会有提示更新。比较棘手的问题是目前界面并没有地方可以处理这些关系，当这种隐藏的关系链出现问题，就需要借助特殊的插件，或通过在 「Plugins」 – 「Run Script…」 运行特定的脚本来查看信息或处理关联。

<a name="48476998"></a>
## 2、组件实例、组件母版与库组件
组件母版（Symbol Master）是一种特殊画板，能够引出另一个分身称为组件实例（Symbol Instance），分身只有单一的图层，但可能会有不同外观。组件实例在图层面板有两种图标，旋转箭头图标表示文档内的实例，而索链图标则表示来自库的实例，这种来自库的实例无法在当前文档修改母版，很多情况就称为库组件（Library Symbol）。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553347918501-fbbed11b-3d1f-4a05-8caf-ba6a5c8761ff.png#align=left&display=inline&height=52&name=image.png&originHeight=114&originWidth=600&size=10100&status=done&width=273)<br />
<br />为了区别文档上的组件母版和库组件，文档上所有的组件母版集合称为内部组件（Local Symbols），文档上所有库组件的集合通常叫外部组件（Foreign Symbols）或导入的组件（Imported Symbols）。

从插入组件的菜单上，只能显示出库文档内的所有内部组件，文档内的外部组件是不会出现在菜单上的，所以通常情况下作为库的文档都是组件母版。使用了嵌入另一库组件的库组件，如果没载入内嵌库组件所属的库，在 Overrides 中把组件更换成其他组件，就只能重新插入来恢复之前的状态。

<a name="70838fba"></a>
## 3、symbol
<a name="61132457"></a>
### 3.1、什么是symbol
在 Sketch 汉化插件中，Symbol 被翻译为「符号」，又翻译「元件」。

Symbol 是 Sketch 中一个强大且实用的功能，可以让你轻松的在画板和页面以及多个文件中复用重复元素。

Symbol 的存在类似智能对象在 PS 中的存在，但 Symbol 比智能对象更加灵活实用。symbols 就像邮戳，制作了一个之后便可以反复使用。在 Sketch 中，当你修改了主 symbol，所有来自于该 symbol 的实例对象都会被自动更新，这能使设计稿的迭代效率得到极大提升。通过属性覆写 (overrides) 也可以对symbol进行订制。

<a name="2220af5c"></a>
### 3.2、创建symbol
<a name="3b062f74"></a>
#### 3.2.1、创建、使用、编辑元件
创建一个新元件非常简单。通过 symbols 将复用率较高的设计模式进行打包。举例来说，我们现在有一个卡片组件，其中包含一个圆形图片、一段文字描述以及一个按钮。完成布局设计，将它们打包成组，选中要转化为元件的内容，点击顶部工具栏的 Create Symbol 按钮，就可以转化为元件。

转化为元件的内容，可以直接复制，或在顶部 Symbols 菜单中选择使用。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553347883799-8bd1cc6e-16da-4474-929d-f062e2265f62.png#align=left&display=inline&height=228&name=image.png&originHeight=1150&originWidth=2102&size=398148&status=done&width=417)

当你准备像过去那样通过双击Library Symbol对其进行编辑时，Sketch会提醒你该Symbol属于某Library，你可以在「Unlink from Library」或是「Open in Original Document」当中进行选择。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553347970584-507a2760-1189-4f11-a100-c9eeff4cb70c.png#align=left&display=inline&height=178&name=image.png&originHeight=460&originWidth=1392&size=111208&status=done&width=539)
<a name="d41d8cd9"></a>
#### 
<a name="59f6da76"></a>
#### 3.2.2、元件的复制、分类、替换
如果想以某个元件为样板，创建类似的元件，可以在 Symbols 页面中直接复制。在左侧列表中右键选择 Duplicate ，或按住 Alt 拖拽画板。

在给元件命名时，可以使用斜线「/」进行分类，将不同类型的元件组织起来。

在画板中选择一个元件，在右侧的面板中可以将它替换为其他元件。替换的菜单中默认展开了当前元件所在的分类，便于在一个分类下进行切换。当然，也可以选择其他分类下的元件进行替换。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553346269275-6f7e8a33-70a1-4dad-b057-54e18740d27e.png#align=left&display=inline&height=237&name=image.png&originHeight=520&originWidth=800&size=146617&status=done&width=364)

<a name="580da8af"></a>
### 3.3、命名规范
为了使可覆写的属性在检查器面板当中呈现出恰当的属性名，例如“姓名”、“职能”等等，而不是在创建symbol时所使用的特定范例内容，你可以在打包创建symbol之前对图层进行重命名，使其与最终希望呈现出的属性名称一一对应。
<a name="0fc9ae79"></a>
#### 3.3.1、组件命名
库文件会分发给团队内部设计师，甚至是外部设计师，所以库组件的分组结构需要尽量清晰。组件名称使用 「/」 符号分组，建议分组在 1 – 4 之间，「/」 前后加入一个空格，名称使用 Title Case 或 lower case 方式命名，如果你的组件跟某个界面框架相应，也可以根据这个界面框架的模版名称命名。

第一组名称可以根据 Atomic Design 的理论命名。例如 Atoms、Molecules、Organisms、Templates、Pages 或 Components、Patterns 之类。<br />第二组名称使用元素的标准名称，这个可以参考各 Web 前端框架、iOS 和 Android 等平台对控件的命名。例如 Navigation Bar、Status Bar、Toolbar。<br />第三组名称则表示元素的不同属性或者状态，例如尺寸、浅色主题和深色主题，聚焦状态和禁用状态，正确、错误和警告状态等等。例如 Button Default、Button Primary。<br />通常第二、三组可能会有多个子类，因为 Sketch 会以字母顺序排列，所以通常将主类的名前置，而将表示状态等词后置，这样菜单中就会显示更清晰，例如 Input / Text Disable 和 Input / Password Disable。

目前设计师可以使用 Sketch Runner 插件的 Insert 功能，搜索并插入所有库中的组件，但目前该插件中文搜索结果非常差，所以建议组件命名统一采用英文，并且与相应的框架或平台的规范名称一致。

如果可能会导出组件，组件命名就尽量不要包含可以用于文件名的特殊符号，和大小写敏感问题，例如 macOS 文件名不能包含 「:」，Windows 不能包含 「:*?<> 」 等字符。另外在 macOS 和 Linux 中文件名以点开头的文件会被隐藏，所以组件的类中不要以点开头。

Sketch Runner 在搜索组件时，可以设置忽略名称带有某个特定前缀和后缀的组件。通常把一些不会在设计中独立使用的组件，图层命名使用 「_」 开头。 在库中那些有异议或未确定的组件，建议在图层命名结尾加 「!」 符号。<br />现在有很多设计系统包含 Sketch 的 UIKit，可以从这些文件上学习他们是如果管理库组件的，最后还是要根据团队的业务、技术水平和文化等因素，结合自己的思考，制定一套适合团队的管理规范。

<a name="26a03bb4"></a>
#### 3.3.2、样式命名
图层样式和文本样式的命名，尽量根据 Web前端框架、iOS 和 Android 等平台的规范，如果自己有一套规则，也需要合理的命名。样式命名建议分组在 1 – 2 之间，可参考组件命名规则。样式的命名也可以使用 「_」 开头来表示一些不会在设计中独立使用的样式。

<a name="716c3852"></a>
#### 3.3.3、Overrides 标签命名
Overrides 标签命名即是组件内相应的图层名，为了能清晰表达 Overrides 中各项的含义，会出现 Overrides 面板上的图层，例如文本图层、位图图层、位图填充图层、组件实例图层和热区图层等，都尽量需要改成合理的名称，例如统一改成 Text、Image、Icon 等等之类的词汇，有些设计也使用 Emoji 加文字的方式来命名 Overrides 标签。<br />Automate 插件内 「Symbol – Rename Instances」 可以把选中的组件实例图层，改成原组件模板的最后一组名称。

<a name="af2a9eba"></a>
### 3.4、元件的可变内容
通过属性覆写 (overrides) 对symbol进行订制。<br />譬如我们将一个卡片模式打包成为symbol，在日常使用时通常需要在不修改主symbol的前提下更改每个实例当中的具体属性值，例如图片、文字等等。属性覆写功能 (overrides) 就是用来解决这个问题的。<br />将symbol插入到画板当中，保持选中态，右侧检查器面板当中会出现“Overrides”选项单。下图所示的范例共包含4项可覆写文本字段，你只需在这里进行修改，便能使该symbol衍生出的每一个实例对象都体现出不同的内容。

symbol当中并非每一个元素都需要支持覆写功能，譬如那些永远不会发生内容变动的属性。如果不想该属性出现在symbol的检查器面板当中，只需在创建symbol之前在图层列表当中将该图层锁定即可 (锁型图标)。
<a name="26eff2a3"></a>
#### 3.4.1、可变的文本
元件内的文本默认都是可变的。对于不需要可变的文本，可以将它锁定（如上图中的「下载文件」文本）。<br />元件内的图层名将被 Sketch 用做可变内容的标题，图层的内容则被作为默认内容。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553348439869-bcaca2f1-4984-4893-852e-802c257fa1ba.png#align=left&display=inline&height=164&name=image.png&originHeight=360&originWidth=800&size=78848&status=done&width=364)

<a name="3538c25b"></a>
#### 3.4.2、可变的图片
元件内的可变图片，可以通过将元件内图形图层的填充改为图像模式来实现。<br />当然，可变图片的透明度、填充方式（Fill/Fit/Stretch/Tile）等属性也与元件内的设置保持相同。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553348411385-b22f7c5a-f879-4b1d-a84b-a92c9cff8431.png#align=left&display=inline&height=218&name=image.png&originHeight=480&originWidth=800&size=136493&status=done&width=364)

<a name="2bf89538"></a>
#### 3.4.3、可变的子元件：元件内的元件
在元件内使用的元件被称作子元件，在元件的 Overrides 设置中，可以选择替换不同的子元件，也可以直接对子元件的可变内容进行设置。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553348490262-2b0bad7d-617f-43ce-a76d-5acf48b028da.png#align=left&display=inline&height=146&name=image.png&originHeight=320&originWidth=800&size=95646&status=done&width=364)

在替换时， Sketch 只允许用同原始尺寸的元件进行替换。在替换后，子元件内同名的可变内容将被保留。

当我们将文字、图片、子元件组合起来使用后，可以实现复杂的组件化。在做诸如信息流、聊天列表、会话界面这类包含复杂重复内容的设计时，就能事半功倍了。

<a name="7f7cca48"></a>
### 3.5、自适应
使用 Sketch 中的「缩放控制」（Resizing）、「文本的内容跟随」两个特性来解决。
<a name="320fc6b3"></a>
#### 3.5.1、缩放控制：位置与尺寸
![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553348744814-8c29ecaf-4f47-448f-918a-93b213e9fd88.png#align=left&display=inline&height=109&name=image.png&originHeight=240&originWidth=400&size=42651&status=done&width=182)<br />在 Sketch 中，缩放控制（Resizing）是实现动态排版的主要方法。我们可以给每个图层设置 Reszing 属性，来控制图层内容在缩放时的表现。在上图中，可以直观的看到 Resizing 在缩放时起到的作用。<br />具体的控制关系如下：<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553348767973-357f5b11-5edc-4817-8c7a-400cf6ae2cf6.png#align=left&display=inline&height=158&name=image.png&originHeight=533&originWidth=800&size=190625&status=done&width=237)

<a name="a18c8ebc"></a>
#### 3.5.2、文本的内容跟随
Sketch 的元件中有个很神奇的特性，我将其译作「内容跟随」。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553348948497-dd092fbe-b086-4dc9-a807-8e1de468ff3b.png#align=left&display=inline&height=218&name=image.png&originHeight=480&originWidth=600&size=85840&status=done&width=273)<br />如上图，当文本被尺寸设置为 Auto 时，根据对齐方式的不同，其尺寸可变的一侧（左对齐文字的右侧，右对齐文字的左侧，不包括居中对齐）的组或图层会与文本保持固定的距离，距离限制为20px，超出这个距离的内容将不会跟随。

内容跟随甚至支持多个图层的连续跟随。利用这种特性，就可以做出固定间距、固定分隔图形的文字导航栏。

<a name="e0f1260f"></a>
#### 3.5.3、固定尺寸的深入研究
结论是：在 Sketch 中，「固定宽度/高度」只会确保组/图层的尺寸不会被「外部」缩放所改变，并不会限制其「内部」产生的尺寸变化，也不会影响其内部文本在尺寸变化后的「内容跟随」。

<a name="8226bcb8"></a>
#### 3.5.4、用Kitchen 插件中的智能排版
[https://www.uisdc.com/sketch-typesetting-plugin-kitchen](https://www.uisdc.com/sketch-typesetting-plugin-kitchen)

<a name="c7344727"></a>
### 3.6、嵌套
[https://www.yuque.com/jingwhale/tool/skhlps](https://www.yuque.com/jingwhale/tool/skhlps)

<a name="f0eb0a9d"></a>
## 4、设计规范库
<a name="679c9155"></a>
### 4.1、设计
<a name="b6743992"></a>
#### 4.1.1、Sketch组件设计的基础知识
**1）. **[**Text style**](https://sketchapp.com/docs/text/text-styles)<br />**![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553396925796-1512be8d-8e2d-49a3-87c2-40749a43c16a.png#align=left&display=inline&height=86&name=image.png&originHeight=188&originWidth=736&size=58165&status=done&width=335)**<br />在设计包含大量文本的界面时，许多图层拥有相同的文本属性。将它们保存为 Text Style，即可复用这些文本属性，无需逐一设置。<br />Text Style 用于设置文字规范，涵盖字体、字号、字重、颜色、字间距、行高 、段间距等内容。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553396947413-ddd91fa6-de35-482f-a037-20c5ea3322b7.png#align=left&display=inline&height=218&name=image.png&originHeight=306&originWidth=236&size=46944&status=done&width=168)<br />行高：参考知乎专栏[《聊一聊 Sketch 与 iOS 文字的行高》](https://zhuanlan.zhihu.com/p/38322447)

**2）.**[** Layer style**](https://sketchapp.com/docs/styling/shared-styles)<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553396978034-5da319a3-272e-4009-8d43-78f73f1fb0f4.png#align=left&display=inline&height=79&name=image.png&originHeight=174&originWidth=736&size=35181&status=done&width=335)<br />将一组风格元素保存为 Layer Style，这些元素便可复用在文档中的任何图层。<br />Layer Style 用于制作颜色规范，涵盖填充颜色、描边颜色、内外阴影、模糊效果等内容。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553397006662-1c8dbf31-9571-4e86-9b00-9b5b3e4d29c8.png#align=left&display=inline&height=87&name=image.png&originHeight=190&originWidth=237&size=11956&status=done&width=108)

**3）. **[**Symbol**](https://sketchapp.com/docs/symbols)<br />作为 Sketch 的一项主打功能，Symbol 可以在画板、页面甚至其他 Sketch 文件中复用。Sketch 52 后，新功能令 Symbol 更加灵活化、轻量化。<br />可复用：支持画板、页面、多个文档间的复用<br />可嵌套：Symbol 内可以嵌套多个 Symbol<br />可替换：Symbol 可替换为同组的其他 Symbol

**4). 英文命名**<br />之所以使用英文命名组件，有以下几点原因：<br />方便设计师后期修改、整理文件<br />团队内部易达成共识，方便协作<br />节约开发成本，减少不必要的沟通与重新切图情况

<a name="b14cea18"></a>
#### 4.1.2、组件库的构建思路
**1)、组件库的构建思路**<br />建立组件库之前，先来谈谈构建思路：解构、拆分、重构。<br />**「 解构 」**<br />通用类设计规范包含：基础规范、图标规范、组件规范，第一步，将这三类规范一一解构。例：基础规范解构为文字规范、颜色规范、布局规范…<br />**「 拆分 」**<br />将解构后的规范拆分为最基本的元素 Symbol，基础规范与图标规范到这一步就完成了。例：文字规范中，拆分为标题、副标题、正文、辅助文字、标签文字…<br />**「 重构 」**<br />重构或称为 Symbol [嵌套](https://sketchapp.com/docs/symbols/nested-symbols)。用于制作组件规范，将拆分后的元素 Symbol 组合为模块 Symbol，再将模块 Symbol 组合为组件 Symbol。

**2)、利用Symbol组件库建立设计规范**<br />**其实，一套优秀的Symbol组件库 = 一套简洁易用的设计规范。组件库中不仅涵盖了常用组件，同时也包含 Text Style 与 Layer Style，三者共同组成了一套设计规范。**<br />先来看看优秀的 Symbol 组件库（常用组件规范）是什么样子的：<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553396900493-27e24441-cf13-4caf-8ffd-7e700487b165.png#align=left&display=inline&height=200&name=image.png&originHeight=440&originWidth=1080&size=150199&status=done&width=491)

图示内容为 Ant Design 团队出品的 Web 端组件库⁶ ，使用 Symbol Manager 插件预览。<br />根据上文的思路，我们将基础规范、图标规范、组件规范解构并将部分拆分为基础元素，得出以下内容：

<a name="14f8d44b"></a>
#### 4.1.3、基础规范
| 1）. 文字规范（创建为Text Style） | ↳ 标题（Titile）<br />↳ 副标题（Subtitile）<br />↳ 正文（Body）<br />↳ 次要文字（Secondary）<br />↳ 标签文字（Tags） |
| --- | --- |
| 2）. 颜色规范（创建为Layer Style） |  ↳ 主色调（Primary）包含主色调的类似色，用做不同状态<br />↳ 功能色（Fuction）成功、失败、警示、不可用等状态的颜色<br />↳ 渐变色（Gradients）<br />↳ 背景色（Background）<br />↳ 字体颜色（Text） |
| 3）. 布局规范 |  ↳ 分割线（Dividers） |
| 4）. 标签规范 | ↳ …… |
| 5）. 其他样式 | ↳ 圆角规范（Radius）<br />↳ 阴影规范（Shadows） |

基础规范中的主要内容为文字规范与颜色规范，将文字规范中的元素创建为 Text Style，颜色规范中的元素分类后创建为 Layer Style，其他元素根据不同情况进行调整即可。

<a name="1daff329"></a>
#### 4.1.4、图标规范
图标规范中，可根据图标尺寸、业务场景、图标功能等进行层级区分，笔者根据图标尺寸来区分层级（暂不考虑最小可交互区域）：

| _尺寸_ | _使用场景：_ |
| --- | --- |
| 48px | Tab栏图标、金刚区图标、吸底按钮图标等 |
| 40px | 标题图标、个人中心列表图标等 |
| 30px | 辅助图标 |

在制作图标规范时，需要根据设计师自身情况作出相应调整。但在设计图标时，以下几点是共通的：<br />**「 构成简单 」**<br />根据简洁法则我们知道，简洁图形的识别需要用户最少的认知和努力。对于通用规范中的图标来说，尽可能的简洁以保证用户的辨识度。当然，像 TabBar、金刚区等特殊区域的图标，需要我们在工作中单独设计。

**「 视觉尺寸统一 」**<br />使用图标盒子作为设计时的参照，保证整套图标在视觉大小上的统一。当然图标盒子并不是一个定死的数值，日常工作中需要根据图标形状进行微调。

**「 像素对齐 」<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553397529302-09986d17-dc12-414f-bd62-7106eeaa4a72.png#align=left&display=inline&height=52&name=image.png&originHeight=77&originWidth=232&size=11199&status=done&width=156)**<br />对齐像素网格，路径锚点的位置使用整数，避免虚边情况的发生。<br />在 Sketch 中，可以通过打开像素模式或使用自动对齐像素功能来进行像素对齐。

**「 使用偶数 」**<br />适配原因，尤其在@2x的情况下作图时需格外注意。

**「 矢量形状 」**<br />使用 Convert to Outlines 与布尔运算功能，将图标转化为矢量形状。

TIPS：在矢量形状上套用 Layer Style 中的任意颜色，在之后的 Symbol 嵌套中就可以更改图标的颜色了。
<a name="ac2bc2c3"></a>
#### 4.1.5、组件规范
![组件规范.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553398279083-c44695b7-feb1-4f27-a12a-afcd07c2c84c.png#align=left&display=inline&height=506&name=%E7%BB%84%E4%BB%B6%E8%A7%84%E8%8C%83.png&originHeight=1848&originWidth=1132&size=232211&status=done&width=310)

由于篇幅有限，本文只介绍通用类组件，解构并归类后，得出以下内容（设计师可以根据项目情况自行补充）

但仅仅解构分类是不够的，想要完成一整套 Symbol 组件库，还需要将解构后的组件拆分为单独的元素 Symbol，以方便嵌套并组成 Symbol 组件。

<a name="82a600b4"></a>
#### 4.1.6、 List 组件举例分析
![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553398764517-7884bfd6-a0b7-4acf-aa19-e4552349b8f6.png#align=left&display=inline&height=132&name=image.png&originHeight=290&originWidth=699&size=22160&status=done&width=318)<br />同上文制作 Symbol 组件库的思路一样，对于单一组件，同样运用解构 → 拆分 → 重构的思路。不同的是，单一组件需要考虑到组件的不同形式 / 状态。

**「 解构为模块 」**<br />将 List 模块化解构，得到 背景 Background、分割线 Divider、左侧内容 Left、右侧内容 Right

**「 拆分为元素 」**<br />左、右两侧内容还可以继续拆分，得到 图标 Icon、标题 Title、文字 Text、箭头 Arrow

**「 添加其他形式 / 状态 」**<br />仅涵盖一种形式 / 状态并不能称之为完整的规范，我们需要考虑到List常见的所有形式<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553398748206-54b40176-308d-4188-b0ba-7aae50bacbdc.png#align=left&display=inline&height=301&name=image.png&originHeight=662&originWidth=1080&size=183970&status=done&width=491)

如图，分割线的各种状态，左右侧内容的各种形式都需要考虑在内。对比前文拆分的结果，去除重复项，你会发现多出了一个开关 Switch 元素（Arrow、Check属于Icon类），把它加入列表，就得到了构成 List 组件的所有元素 Symbol。<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553398716573-0741d4a3-54df-4b95-8538-a2e6e07118d2.png#align=left&display=inline&height=217&name=image.png&originHeight=587&originWidth=1080&size=226512&status=done&width=399)<br />是不是有点眼熟？没错，这些元素 Symbol 正是基础规范与图标规范中的内容。

**「 Symbol嵌套（重构）」**<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553398702635-68dfbad7-b6f5-4d56-9fa5-3e1c83072095.png#align=left&display=inline&height=335&name=image.png&originHeight=737&originWidth=1080&size=273277&status=done&width=491)<br />反向进行上面三步的思路，进行 Symbol 嵌套：首先将最基础的元素 Symbol 组合成模块化 Symbol，然后将模块化 Symbol 组合成为 List 组件。

由于使用了 Symbol 嵌套，所以最后组合而成的 List 组件可以在右侧的 Overrides 中进行各个模块与元素的设置。<br />重复利用解构为模块、拆分为元素、添加状态/形式、重构（元素 Symbol → 模块 Symbol → 组件 Symbol）这 4 个步骤，完成组件规范列表中的所有组件，这套利用了 Symbol 功能制作的通用规范组件库就完成了。

<a name="5a9bfc14"></a>
### 4.2、 让Symbol组件更加灵活
[Resizing ](https://sketchapp.com/docs/layer-basics/constraints)智能缩放是 Sketch 39 中加入的新功能，下面在Symbol 组件库中的一个栗子：<br />![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553399612179-127308ca-ed98-4bb4-a550-3469981eab36.png#align=left&display=inline&height=545&name=image.png&originHeight=1199&originWidth=900&size=179898&status=done&width=409)

将 Tabbar 解构，我们得到 N 个相同的 Tab 模块；然后将 Tab 模块拆分，得到 图标 Icon、文字 Text、分割线 Divider、背景 Background 4 个元素。

分别设置这 4 个元素的 Resizing 属性，Tab 模块即可做到横向自由拉伸且不打乱布局。通过横向拉伸尺寸，就可以得到 3-5 个 Tab 的 Tabbar 了。

可运用 Resizing 的类似组件还有很多，在制作 Symbol 组件库中稍加留意，就能让你的 Symbol 更加的灵活易用。

<a name="4249c8d8"></a>
### 4.3、规范化管理Symbol组件库
当 Symbol 名称中存在 「 / 」 符号时，Sketch 会将他们作为组独立对待。举个栗子：两个 Symbol，一个名为 「 Button / normal 」，另一个名为 「 Button / pressed 」，这两个 Symbol 将被归类在 Buttom 分组中。为了更好的管理Symbol组件库，我们需要用到更专业的插件工具。
<a name="5beab42e"></a>
#### 4.3.1、Symbol Organizer
能够按设定的规则来自动整理 Symbol 在 Symbol Page 的排列情况，整理后 Symbol 结构会更加清晰干净，便于后续维护和复用。

<a name="e91a4160"></a>
#### 4.3.2、 Sketch Manager
![image.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553399100112-b4cb206a-3fce-4327-a2ca-85fda1591905.png#align=left&display=inline&height=200&name=image.png&originHeight=440&originWidth=1080&size=150199&status=done&width=491)

<a name="f7edcc0c"></a>
#### 4.3.3、Symbol Instance Renamer
能够将 Symbol 的 Instance 们按照最新的 Master Symbol 的命名进行统一，摆脱了繁琐的手动重命名。查看官网

<a name="0e1ebaaa"></a>
## 5、高效率使用规范组件库symbols
使用插件Runner，通过搜索关键字插入 Symbol。

插件下载：[https://sketchrunner.com/](https://sketchrunner.com/)。

打开 Runner 的偏好设置，将第一项 Always start with 改为 insert，能够更方便地通过搜索关键字插入 Symbol。<br />![屏幕快照 2019-03-24 上午11.52.07.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1553399554884-bab1d20d-a027-498c-9d7d-5073f98b91d8.png#align=left&display=inline&height=338&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-03-24%20%E4%B8%8A%E5%8D%8811.52.07.png&originHeight=1070&originWidth=1768&size=408417&status=done&width=559)


