# 设计文件的版本控制

使用git管理设计.sketch文件的关键版本。[Demo](https://github.com/jingwhale/sketch-file)。

git的好处：

| -强大的版本控制，分支系统 |
| --- |
| -Git中每个克隆(clone)的版本库都是平等的。你可以从任何一个版本库的克隆来创建属于你自己的版本库，同时你的版本库也可以作为源提供给他人，只要你愿意。 |
| -Git的提交不会被打断，直到你的工作完全满意了，PUSH给他人或者他人PULL你的版本库，合并会发生在PULL和PUSH过程中，不能自动解决的冲突会提示您手工完成。 |
| -可以为 Git 版本库进行授权：谁能创建版本库，谁能向版本库PUSH，谁能够读取（克隆）版本库 |
| -你完全可以在脱离Git服务器所在网络的情况下，如移动办公／出差时，照常使用代码库；你只需要在能够接入Git服务器所在网络时，PULL和PUSH即可完成和服务器同步以及提交 |
| -图形界面 |

<a name="c2bfb5c9"></a>
### 1、github配置公钥
本地与远程仓库连接。
<a name="f85e2397"></a>
#### 1.1、确认是否已经有一个公钥
即检查.ssh文件夹，以及文件夹中是否存在id_dsa 和 id_rsa.pub文件<br />有.pub后缀的文件就是公钥，另一个文件则是密钥<br />如果不存在，或者干脆连.ssh文件夹都没有，可以进行创建<br />如果存在，直接将公钥串添加到github中

```
cat ~/.ssh/id_rsa.pub
```

<a name="bf55c2ba"></a>
#### 1.2、生成公钥
可以用ssh-keygen来创建<br />它先要求你确认保存公钥的位置（.ssh/id_rsa）<br />然后它会让你重复一个密码两次，如果不想在使用公钥的时候输入密码，可以留空。<br />生成后，同样获取公钥：
```
cat ~/.ssh/id_rsa.pub
```

<a name="9e47394f"></a>
### 2、安装[SourceTree](https://www.sourcetreeapp.com/)
git操作工具。[使用参考](https://www.jianshu.com/p/1e286d33adab)。

<a name="28a8e9b3"></a>
### 3、将.sketch文件推至远程库
**github建立仓库，clone到本地，将.sketch文件存入到本地文件库中，在Sketch中git此文件即可追踪。**<br />**
<a name="d798a294"></a>
### 4、git 使用规范
<a name="56758cfd"></a>
#### 4.1 git提交规范
| _操作_ | _规范_ |
| --- | --- |
| 1）、添加 | @ add description |
| 2）、更新 | @ update description |
| 3）、优化 | @ opt description |
| 4）、删除 | @ delete description |

<a name="9659a0a4"></a>
#### 4.2 git分支规范
| 1）、设计开发分支 | feature/object_name_time

单一项目，开发完成后合并回master，删除分支；<br />项目分子，保留分支。 |
| --- | --- |
| 2)、合并分支 | 手动：merge branch1 to branch2<br /><br />SourceTree（自动）："Merge branch 'master' of github.com:jingwhale/sketch-file" |

<a name="c32e86bc"></a>
### 5、使用git进行项目的版本控制。
**建议：**

| 1.1、单个项目，分工合作，需要拉单独项目的分支，完成后合并 |
| --- |
| 1.2、单个项目，不同的方案，建议各自使用分支管理不同的版本 |
| 1.3、提交关键记录：可以批量修改、或单次修改，但属于较大的改动。 |

<a name="5d8cbed7"></a>
### 6、git 仓库
**6.1、免费的git仓库**<br />[1）、github](https://github.com/)<br />[2）、腾讯云开发者平台](https://dev.tencent.com/user)<br />[3）、码云](https://gitee.com/)


**6.2、自建git仓库**<br />[1)、《使用gitlab搭建自己的代码库》](https://www.cnblogs.com/pliybird/p/6026248.html)<br />[2)、《搭建Git服务器》](https://www.liaoxuefeng.com/wiki/0013739516305929606dd18361248578c67b8067c8c017b000/00137583770360579bc4b458f044ce7afed3df579123eca000)

<a name="4f94ec4e"></a>
### 7、项目工程搭建
[7.1、项目工程目录示例：](https://dev.tencent.com/u/whalexplorer/p/prototype/git/tree/master)<br />![屏幕快照 2019-04-13 上午10.40.48.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1555123268532-17fe5dca-5373-4809-854f-87aea7014388.png#align=left&display=inline&height=212&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-13%20%E4%B8%8A%E5%8D%8810.40.48.png&originHeight=530&originWidth=698&size=63952&status=done&width=279)

项目以文件夹形式存在，用英文命名。如：tmall、whaleCode等。<br />README.md为项目的展示链接。

7.2、项目目录示例：<br />![屏幕快照 2019-04-13 上午10.44.36.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1555123484741-66e24a8f-58c2-4215-871c-2620a1330737.png#align=left&display=inline&height=150&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-13%20%E4%B8%8A%E5%8D%8810.44.36.png&originHeight=314&originWidth=664&size=29092&status=done&width=317)
```
tmall.sketch为sketch文件；

tmall文件夹为sketch文件的html版本，看在线观看，有FusionCool工具自动生成；

README.md为项目的介绍
```

7.3、自动生成项目的导航<br />1）、在工程目录prototype下，使用：
```
npm init
```

依次按照需求填写信息，生成package.json：
```
{
  "name": "prototype-project",
  "version": "1.0.0",
  "description": "prototype",
  "main": "index.js",
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
  },
  "repository": {
    "type": "git",
    "url": "git@git.dev.tencent.com:whalexplorer/prototype.git"
  },
  "keywords": [
    "prototype"
  ],
  "author": "jingewhale@yeah.net",
  "license": "ISC"
}
```

2）、在工程目录prototype下，安装whale-makelink：
```
npm i whale-makelink
```

3)、添加npm运行的脚本，在package.json的scripts中添加link命令：
```
"link": "node ./node_modules/whale-makelink/index.js"
```

完整的package.json如下：
```
{
  "name": "prototype-project",
  "version": "1.0.0",
  "description": "prototype",
  "main": "index.js",
  "dependencies": {
    "whale-makelink": "^1.0.3"
  },
  "devDependencies": {},
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "link": "node ./node_modules/whale-makelink/index.js"
  },
  "repository": {
    "type": "git",
    "url": "git@git.dev.tencent.com:whalexplorer/prototype.git"
  },
  "keywords": [
    "prototype"
  ],
  "author": "jingewhale@yeah.net",
  "license": "ISC"
}
```

在工程目录下运行：
```
npm run link
```

会自动将各个共目录，添加到工程的README.md中，展示如下：<br />![屏幕快照 2019-04-13 上午10.59.14.png](https://cdn.nlark.com/yuque/0/2019/png/120638/1555124362834-7fa5ec9f-59f1-4c15-9ef2-3f278030e100.png#align=left&display=inline&height=189&name=%E5%B1%8F%E5%B9%95%E5%BF%AB%E7%85%A7%202019-04-13%20%E4%B8%8A%E5%8D%8810.59.14.png&originHeight=576&originWidth=2276&size=81873&status=done&width=746)
<a name="78a68284"></a>
### 8、.gitignore
可以忽略某些文件的变动，不提交到git 仓库。<br />在.gitingore 文件中，遵循相应的语法，在每一行指定一个忽略规则。[《Git忽略提交规则》](https://www.cnblogs.com/kevingrace/p/5690241.html)。
```
node_modules
.idea/
*.log
```

有时候一些文件已经添加到git中，我们需要从git cached中删除，不然.gitignore配置不生效。示例，node_modules已经存在git cached中，删除命令如下：
```
git rm -r -f --cached  /node_modules/
```

<a name="6c159de6"></a>
### 9、使用[git-sketch-plugin](https://github.com/mathieudutour/git-sketch-plugin)插件管理sketch版本。
[具体操作](https://www.jianshu.com/p/c401c0b1247e)。
