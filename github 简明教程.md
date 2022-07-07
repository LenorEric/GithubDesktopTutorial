# Github 简明教程

Lenor

## 符号定义

:fast_forward:： 代表这是一个快捷键

:question: ：代表这个操作未经验证

:balloon:：代表这是个可选操作

*italic*：斜体字代表这是一个 git/github 术语，或者代表这是图片/程序中的某一个内容。

\$内容\$：代表这里要替换成你自己对应的内容

[link](#Github 简明教程)：代表这是一个可以点击的链接，将会链接到某个特定的网址。

## Git/Github 是什么

Github 是一个基于 git 技术的代码管理平台，git 是一个免费开源的版本管理系统。

版本管理，意味它可以保存和管理一个项目的不同版本的文件，并提供各种管理与协作的功能。

例如多个人可以同时编辑一个项目，版本管理系统会负责合并不同人的修改。

或者如果你可以随时把代码完全或者部分回滚到之前的某一个版本，或者浏览之前某个版本和现在的差异。

甚至构建一个新的分支代码，在其中进行实验性的编辑，如果成功，就将这个分支合并到主分支中，否则丢弃这部分内容。这允许你进行多样的尝试而不用担心丢失任何已经做的进度。

## Why Github

国内的确也有类似 gitee 的平台提供了 git 服务，但是在各种方面都多多少少有点恶心人。以及考虑到 github 有着集成的 github desktop 以及各种其他的支持，使得新人也可以很快上手。

但是 github 在国内的可访问性多多少少有一点不好，在某些时候可能需要使用 “增强网络访问能力” 的部分工具。如果需要可以联系 Lenor 购买。当然，你也可以使用 gitee 配合其他开源的 git 管理工具。（甚至直接使用命令行

## 前期准备

首先，你需要确定你的网络可以访问 [github](https://www.github.com) 网址（如果不行，你可以联系柠檬来购买一个 “增强网络访问能力的工具”，一个月七块钱，可以两三个人合购），并[注册](https://github.com/signup)一个 github 账号。

:question: 此外，你也可以全程在本地使用 github，在这种情况下，你不需要一个 ”增强网络访问能力的工具”，但是也无法享受某些在线功能（例如在线 merge、多设备协作或在线编辑）。

## Github Desktop

原本 git 工具只提供了一个比较复杂的命令行交互界面（CLI），以及一个不是很好用的图形交互界面（GUI）。但是 github desktop 的存在，使得人们可以比较简单地使用 git 和 github 服务。

在[这里](https://desktop.github.com/)可以下载到 github desktop。

安装后按照提示登录 github 账号（:question:如果你确定不需要使用在线服务，你也可以不登录 github 账号）。

## 新建一个仓库(Repo)

Git 中，项目叫做 *repository*，简称 *repo*。在开始任何工作前，你都需要新建一个 *repo*。在 github desktop 中，选择顶部的 File -> New repository（:fast_forward: Ctrl + N)

<img src="https://s2.loli.net/2022/07/07/CGd1nEO9cihywrA.png" alt="新建 Repo" style="zoom: 67%;"/>

配置项目名称(Name) 和 :balloon:Description，以及本地的仓库目录。

注意，实际的目录格式为 \$Local path\$\\\$Name\$，例如目录为 C:\Lenor\Projects，项目名称为 HelloWorld，那么实际存储的目录是 C:\Lenor\Projects\HelloWorld。

你可以选择（或不选择） 生成 readme 文件，如果选择生成，那么会在项目中生成一个空的 README.md

:balloon:选择 git ignore，在其中选择一个你使用的语言（例如 C）。它可以避免不必要的文件被添加进版本管理系统中。

:balloon: 选择一个 License，通常你可以选择 GNU GPLv3，这会要求使用你的项目的人必须也对代码进行开源（特殊授权除外）。

之后点击 Create repository 新建这个 *repo*。

## 进行工作

之后，你可以在你新建的 *repo* 对应的本地目录中进行工作。所有在这个文件夹内进行的改动都会被追踪。

在进行了第一步操作后，你可以进行一次初始的 *Commit*。

*Commit* 是版本管理的基本单位，你可以随时回退到任何一个 *Commit* 的状态。因此建议在完成了任何小目标后或者要进行危险的改动前都进行一次 *Commit*。

<img src="https://s2.loli.net/2022/07/07/KT4q1yEz6gxLj3G.png" alt="image-20220707161758917" style="zoom:67%;" />

你可以在 *Changes* 列表中查看自从上次 *Commit* 以来进行了哪些改动。注意，仅文本文件支持这样的功能。二进制文件（例如图片或编译好的程序）不支持这样的操作。

首先在 1 处设置这次 *Commit* 的标题，通常是描述你这次的 *Commit* 干了什么，方便日后追踪。之后可以 :balloon: 添加一些 Description 进行更详细的描述。之后点击 *Commit to main* 来进行这次 *Commit*。

## 上传到云端

:balloon: 在第一次 *Commit* 后，你可以选择把它上传到云端，这样你可以在其他设备访问你的代码，但是这个步骤不是必须的。

点击 *Publish repository* ，配置项目名称和描述（通常不用修改，它会自动继承你在创建 *repo* 时填入的内容。

如果你选择 *Keep this code private*，那么仅你自己和被授权的用户可以访问你的代码。如果这是竞赛代码，推荐打开这个选项以防其他人盗用。

如果你选择了 *Keep this code private*，这个项目将作为一个私有项目保存。如果你希望其他人可以访问和改动你的代码，你可以将他们添加到 *Collaborators*。打开 

```
https://github.com/$你的用户名$/$你的项目名称$/settings
```

在页面左侧找到 Access -> Collaborators，点击 Add people。输入对应的人的用户名，点击 add 即可。再让对方打开

```
https://github.com/$你的用户名$/$你的项目名称$/invitations 
```

即可接受请求。

## *Push* 与 *Pull*

Push 和 Pull 是两种云端的基本操作。如果你没有使用云端操作，那么这两个步骤不是必须的。

在你进行了一个 *Commit* 之后，你需要使用 *Push* 将它上传到云端。或者在你的协作者进行了一个 *Commit* 后，你需要使用 *Pull* 将其拉去到本地。注意，对于任何操作，一定要先 *Pull*（如果有的话） 之后再 *Push*。如果当前存在需要 *Pull* 的内容，*Push origin* 按钮会变成 *Fetch*。

点击 *Push origin*（:fast_forward: Ctrl + P)，或者 *Pull origin*（:fast_forward: Ctrl + Shift + P) 即可进行 Push 或者 Pull 操作。

<img src="https://s2.loli.net/2022/07/07/PgAi2E35kKjNLC4.png" alt="image-20220707162938812" style="zoom: 67%;" />

## *Branch*

*Branch* 是 git 的另一个特性，它允许你构建代码的不同分支，以此来进行任何调试而不影响之前的代码。这个功能在非协作时可以被回滚 *Commit* 代替，因此这里暂不详细介绍。在协作的时候，它允许两个人同时编辑同一个内容，并进行 *Merge*。

<img src="https://s2.loli.net/2022/07/07/wHrGJTUaphN8YFB.png" alt="image-20220707165822954" style="zoom:67%;" />

点击 *Current branch* 即可切换当前的工作 Branch，在切换后，你文件夹内的所有文件都会变成这个 Branch 的状态。

注意，**切换 Branch 的时候需要关闭所有已经打开的编辑窗口**(:question:keil 可能会提示文件有外部改动，如果是这样的话不用关，导入外部改动即可。CLion 等软件会自动导入外部改动，也不需要关。Arduino、Markdown 一定要关)（切换后文件会有改动，不关闭可能会导致意料之外的错误）。

注意，切换 *Branch* 的时候需要 *Commit* 现在的代码，否则不熟悉操作的时候容易导致进度丢失。

:bulb:Note: branch 和 commit 的区别是什么？答案：branch 是 commit 的文件夹，它可以包括若干个 commit，其中 main 这个 branch 是主文件夹。

## 回滚

回滚代表你可以将你现在的所有内容变成之前的某一个状态。尽管还提供了更高级的回滚方式，但是最方便的还是这种。

首先，你需要提交一个 *Commit* 来保存你当前的所有改动，并关闭所有已经打开的编辑窗口(:question:keil 可能会提示文件有外部改动，如果是这样的话不用关，导入外部改动即可。CLion 等软件会自动导入外部改动，也不需要关。Arduino 一定要关)（回滚后文件会有改动，不关闭可能会导致意料之外的错误）。

之后，点击 *Changes* 旁边的 *History*，在其中寻找你想要回滚到的版本。右键点击后选择 *Create branch from commit*，选择一个合适的文件名。这样就会创建一个新的 *Branch*，内容是当前这个 *Commit* 版本的内容。注意，所有在这个 *Commit* 后进行的编辑都不会存在于这个 *Branch* 中，但是你可以稍后将其合并这个 *Branch* 到 主分支中，以此来不丢失任何进度地恢复代码。

之后你可以按照上面的说明，通过切换到这个新建的 Branch 来恢复到之前的内容。

## 合并

*Merge* 是 git 的另一个重要操作，用以合并两个不同的 *Branch*。但本质上它是在对 *Commit* 进行操作。

它通常用以处理这样的一个情况：

存在两个版本 A 和 B，其中包含某些内容在 A 中更新需要保留，而某些内容 B 中更新而需要保留。在这种情况下，需要合并这两个版本，形成一个最新的版本。例如在回滚后，Branch A 中包含部分不想要的代码，但是也有部分希望保留的代码。Branch B 中包含部分以前写的希望保留的代码，但是也有部分老旧的代码需要扔掉。

如果 Branch A 和 Branch B 中，不存在两个相同的文件都被修改的情况，那么这时候 Merge 非常简单，否则可能需要进行手动的调整。推荐使用软件 [VSCode](https://code.visualstudio.com/) 进行手动 Merge。
