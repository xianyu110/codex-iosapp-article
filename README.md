# 从 0 到 1 带你速通 Codex，做出第一个 iOS App

我在二月份写过一篇 [Codex 的教程](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647679828&idx=1&sn=6e1c0a935c70c566ee765c02a36327a6&scene=21#wechat_redirect)，但说实话，那时候的 Codex 和现在已经不是一个状态了。

现在的 Codex，明显进入了爆更模式。

所以这篇，我准备重新从 0 开始，把 Codex 的安装、界面、设置、插件、Skills、网页开发、iOS App 开发，以及手机远程继续开发，完整串起来。

这不是一篇只讲概念的文章。

我会用两个非常容易上手的例子：

- **做一个 Codex 功能介绍网页**
- **做一个用药提醒 iOS App**

带你跑完整个流程。

![图片](https://upload.maynor1024.live/file/1780037540426_article-02.jpg)

先给一个路线图。

| 阶段 | 你要做什么 | 目标 |
| --- | --- | --- |
| 1 | 安装并登录 Codex | 把工具跑起来 |
| 2 | 认识界面 | 知道对话、项目、权限在哪里 |
| 3 | 调整设置 | 让 Codex 更适合长期使用 |
| 4 | 理解 Skills 和插件 | 会给 Codex 加能力 |
| 5 | 做一个网页 | 跑通第一个完整项目 |
| 6 | 做一个 iOS App | 从需求到安装到手机 |
| 7 | 远程继续开发 | 手机上继续操作 Codex |

好，废话不多说，直接开始。

## 一、先安装 Codex

一切的前提，当然是你要有能正常使用 ChatGPT / Codex 的账号环境。

然后直接去 Codex 官网下载安装：

https://chatgpt.com/zh-Hans-CN/codex/

Mac 和 Windows 都有。

这里我用 Mac 做演示。

![图片](https://upload.maynor1024.live/file/1780037538756_article-03.png)

下载安装到本地后，正常打开，登录账号。

Codex 的额度跟你的 ChatGPT 会员有关。轻度使用，普通会员也能体验；如果你准备高频开发，建议先关注自己的额度消耗。

![图片](https://upload.maynor1024.live/file/1780037544310_article-04.jpg)

如果你有 API Key，也可以通过其他方式使用 Codex，这个看你自己的使用习惯。

![图片](https://upload.maynor1024.live/file/1780037552433_article-05.jpg)

登录之后，初始化选项根据自己的情况选择即可，不确定也可以先跳过。

![图片](https://upload.maynor1024.live/file/1780037550197_article-06.png)

接下来有一个很香的地方：**Codex 可以从 Claude Code 和 Cowork 导入内容。**

![图片](https://upload.maynor1024.live/file/1780037553748_article-07.png)

也就是说，如果你之前已经在 Claude Code 里沉淀过配置、记忆、习惯，现在可以直接迁移过来。

对我来说，这相当于 Codex 帮你搬家，一键继承之前的工作环境。

这一步做完，你就能进入 Codex 主界面。

## 二、先认识界面：对话和项目别搞混

进来之后，界面大概是这样。

![图片](https://upload.maynor1024.live/file/1780037561101_article-08.png)

中间是对话区，跟普通 AI 聊天界面类似。

左边栏主要管理两类内容：

- **对话**
- **项目**

![图片](https://upload.maynor1024.live/file/1780037568064_article-09.png)

**对话**适合处理不绑定具体文件夹的任务，比如调研、规划、写文案、整理想法。

![图片](https://upload.maynor1024.live/file/1780037573631_article-10.png)

真正做开发时，更建议用 **项目**。

项目会绑定一个本地文件夹，Codex 会把这个文件夹当作工作区。生成的文件、修改的代码、运行的命令，都会围绕这个目录展开。

![图片](https://upload.maynor1024.live/file/1780037576577_article-11.png)

一个项目里可以开多条对话。

我的建议是：**同一个方向放同一个项目，具体每件事开一条新对话。**

不要把所有任务都堆在一条长对话里。时间一长，上下文会变得很乱，Codex 也更容易被旧任务干扰。

新建项目很简单，在左侧项目区域点加号，选择一个文件夹即可。

![图片](https://upload.maynor1024.live/file/1780037576461_article-12.png)

进入项目后，你会看到对话框左下角出现权限选择。

![图片](https://upload.maynor1024.live/file/1780037576591_article-13.png)

一般来说有三种思路：

| 权限模式 | 适合谁 | 特点 |
| --- | --- | --- |
| 默认审批 | 新手、谨慎用户 | 每次关键操作都要确认 |
| 自动审查 | 日常开发 | 普通操作自动跑，高风险操作拦一下 |
| 完全访问 | 熟练用户、信任当前项目时 | Codex 可以更顺畅地连续执行 |

如果你刚开始用，我建议先保守一点。等你熟悉它的工作方式，再逐渐放开权限。

右下角可以切换模型和推理等级。

![图片](https://upload.maynor1024.live/file/1780037584291_article-14.png)

推理等级日常用高就够了。遇到大型重构、复杂排错、跨文件迁移，再开更高强度。

速度也可以选标准或快速。快速会更消耗额度，如果不是特别着急，标准速度已经够用了。

![图片](https://upload.maynor1024.live/file/1780037582675_article-15.png)

右下角还有语音输入。

![图片](https://upload.maynor1024.live/file/1780037590796_article-16.png)

不过如果你对转写速度和中文体验要求比较高，也可以继续用自己习惯的语音输入法。

用着用着，你肯定会想知道额度还剩多少。

![图片](https://upload.maynor1024.live/file/1780037597121_article-17.png)

点左下角设置，找到额度信息，就能看到短周期和周额度剩余情况。

![图片](https://upload.maynor1024.live/file/1780037603283_article-18.png)

**额度不是用来看的，是用来干活的。**

## 三、这些设置建议先改好

很多人一装好 Codex，就想马上让它做东西。

但我建议先花几分钟把基础设置调好。后面你会省很多事。

打开左下角设置。

![图片](https://upload.maynor1024.live/file/1780037603229_article-19.png)

常规设置里，建议把几个核心开关打开。

![图片](https://upload.maynor1024.live/file/1780037604791_article-20.png)

往下滑，把跟进行为改成 **引导**。

![图片](https://upload.maynor1024.live/file/1780037611533_article-21.png)

这个很重要。

开启之后，如果你发现 Codex 中途方向不对，或者你临时想插一句修改意见，可以更自然地介入，而不是一直等它把任务跑完。

如果开头忘了导入 Claude Code 的内容，也可以在这里补导入。

![图片](https://upload.maynor1024.live/file/1780037616215_article-22.png)

接下来是 **AGENTS.md**。

你可以把它理解成 Codex 的“家法”。

它是一套从上往下分层生效的约束体系：全局有全局规则，项目里也可以有项目规则。

![图片](https://upload.maynor1024.live/file/1780037616070_article-23.png)

如果你不知道一开始写什么，可以先用一套偏稳健的工程规则。核心思想其实就几条：

- **动手前先说明假设**
- **尽量小改，不做无关重构**
- **不要乱造 API、路径和配置**
- **能验证就验证**
- **遇到不确定就停下来问**

这类规则对新手尤其重要，因为它能让 Codex 更像一个可靠的工程助手，而不是一个一兴奋就乱改文件的自动化脚本。

推荐的行为约束示例：

```text
Behavioral guidelines to reduce common LLM coding mistakes.

1. Think Before Coding
- State assumptions explicitly.
- If uncertain, ask.
- If multiple interpretations exist, present them.

2. Simplicity First
- No features beyond what was asked.
- No abstractions for single-use code.
- If it can be simpler, simplify.

3. Surgical Changes
- Touch only what is necessary.
- Match existing style.
- Do not refactor unrelated code.

4. Goal-Driven Execution
- Define success criteria.
- Verify changes with the fastest relevant check.
- Loop until the requested outcome is handled.
```

记忆功能也建议打开。

![图片](https://upload.maynor1024.live/file/1780037622131_article-24.png)

打开以后，Codex 会在合适的时候总结之前的工作片段，后续遇到类似任务时能自动调出来。

外观里还有宠物区域。

![图片](https://upload.maynor1024.live/file/1780037628260_article-25.png)

这个不影响生产力，但确实有点可爱。

## 四、Skills 和插件：给 Codex 加能力

Codex 里有两个很重要的概念：

- **Skills**
- **Plugins**

入口在插件这个 Tab。

![图片](https://upload.maynor1024.live/file/1780037625047_article-26.png)

顶部可以在插件和技能之间切换。

![图片](https://upload.maynor1024.live/file/1780037629568_article-27.png)

**Skill** 就是给 Agent 使用的技能说明。它告诉 Codex：遇到某类任务时，应该按什么流程做。

如果你还不了解 Skills，可以看我之前写过的这篇：

[《一文带你看懂，火爆全网的 Skills 到底是个啥。》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647678672&idx=1&sn=c3510896d2de19b5c5ab6805c27182e5&scene=21#wechat_redirect)

**Plugin** 则更像一个打包好的能力包，里面可能包含 Skills、工具、配置、MCP、浏览器能力等。

简单说：

| 类型 | 可以理解为 |
| --- | --- |
| Skill | 一套任务处理方法 |
| Plugin | 一组更完整的能力包 |

Codex 的好处是，它把这些东西都做成了可视化 UI。

![图片](https://upload.maynor1024.live/file/1780037636677_article-28.png)

点击右上角管理，就能批量管理自己的插件和 Skills。

![图片](https://upload.maynor1024.live/file/1780037633916_article-29.png)

Codex 还内置了 Skill 创建器和插件创建器。

![图片](https://upload.maynor1024.live/file/1780037641159_article-30.png)

你想做一个什么技能，直接用大白话描述，它就能帮你生成初版。

![图片](https://upload.maynor1024.live/file/1780037644340_article-31.jpg)

如果你想安装非官方的 Skill 或插件，也可以直接把链接丢给它。

![图片](https://upload.maynor1024.live/file/1780037643378_article-32.png)

到这里，基础准备就差不多了。

下面开始动手。

## 五、第一个实战：让 Codex 做一个网页

先从简单但完整的任务开始：**做一个 Codex 功能介绍网页。**

建好项目文件夹后，先打开计划模式。

![图片](https://upload.maynor1024.live/file/1780037648983_article-33.png)

点击左边加号，开启计划模式。

![图片](https://upload.maynor1024.live/file/1780037656222_article-34.png)

计划模式的作用是：**只规划，不动手。**

对于稍微复杂一点的任务，我都建议先用计划模式过一遍。

![图片](https://upload.maynor1024.live/file/1780037656579_article-35.png)

你可以这样给 Codex 下需求：

> 帮我做一个 Codex 功能介绍网页，要好看，要有设计感，把所有功能按层级分类展示出来。

![图片](https://upload.maynor1024.live/file/1780037660373_article-36.png)

Codex 可能会先问你几个问题。

![图片](https://upload.maynor1024.live/file/1780037666881_article-37.jpg)

直接点选回答就行。

回答完，它会给你一份比较完整的实施方案。

![图片](https://upload.maynor1024.live/file/1780037672263_article-38.png)

确认方案没问题，再让它开始执行。

中间开发过程不用你盯着看，这种小网页基本一遍就能跑起来。

做完后，Codex 会提示你可以用内置浏览器打开预览。

![图片](https://upload.maynor1024.live/file/1780037672026_article-39.png)

打开之后会看到预览页面。

![图片](https://upload.maynor1024.live/file/1780037673155_article-40.png)

右上角有几个很实用的按钮。

![图片](https://upload.maynor1024.live/file/1780037683088_article-41.png)

第一个是截图。

![图片](https://upload.maynor1024.live/file/1780037680905_article-42.png)

第二个是批注，这个我用得非常多。

你可以直接在页面上圈选一个元素，写上修改意见，不用截图、不用描述半天。

比如你想把某个 logo 换成官方 logo，直接圈选它并输入说明即可。

![图片](https://upload.maynor1024.live/file/1780037691257_article-43.png)

现在还支持直接调字体、字号、颜色等参数，改完可以实时看到效果。

![图片](https://upload.maynor1024.live/file/1780037691053_article-44.jpg)

批注完，点右上角发送。

![图片](https://upload.maynor1024.live/file/1780037696855_article-45.png)

修改后的效果如下。

![图片](https://upload.maynor1024.live/file/1780037701594_article-46.png)

现在网页还只是跑在本地，只有你自己能看到。

如果想发给别人，就需要部署到服务器或者 Vercel、GitHub Pages 之类的平台。

如果你已经有自己的部署 Skill，可以直接让 Codex 调用。

![图片](https://upload.maynor1024.live/file/1780037708767_article-47.png)

输入 `/` 就能调用 Skill。

![图片](https://upload.maynor1024.live/file/1780037704897_article-48.png)

到这里，第一个网页项目就跑通了。

## 六、第二个实战：做一个 iOS 用药提醒 App

接下来做一个更进阶、也更有意思的东西：**iOS App。**

我用一个真实需求来演示。

最近体检后，医生开了几种药，有的一天吃两三次，有的饭前吃，有的饭后吃，时间一多就很容易搞混。

所以我想做一个手机上的 **用药提醒 App**。

需求很简单：

- 记录药品
- 设置服药时间
- 到点提醒
- 标记今天是否吃过

这类小需求特别适合用 Codex 练手。

同样，先开计划模式，把需求说清楚。

![图片](https://upload.maynor1024.live/file/1780037710723_article-49.png)

Codex 会先问一些产品细节，你按自己的需求回答。

最后它会给一份实施计划。

![图片](https://upload.maynor1024.live/file/1780037717397_article-50.png)

确认之后，就可以让它开始做。

过程同样不用你一直盯着。

大概二十分钟后，项目雏形就出来了。

![图片](https://upload.maynor1024.live/file/1780037723037_article-51.png)

它会生成一堆文件。

如果你不是开发出身，看不懂也没关系。

你只需要继续说：

> 我现在想把它传到我的手机上。

![图片](https://upload.maynor1024.live/file/1780037719590_article-52.png)

Codex 会告诉你：做 iOS App 和做网页不一样，需要 Xcode。

网页用浏览器就能跑，但 iOS App 需要本地编译工具。苹果这边就是 Xcode。

![图片](https://upload.maynor1024.live/file/1780037726696_article-53.png)

如果你电脑上没有 Xcode，也可以让 Codex 结合 Computer Use 帮你搜索、下载、安装。

这里的 `@` 是用来点名插件的。

![图片](https://upload.maynor1024.live/file/1780037725639_article-54.png)

Computer Use 是我很常用的能力。

它可以视觉化操控你的电脑，适合处理一些需要点按钮、填表、打开软件的流程。

使用前需要在设置里打开开关。

![图片](https://upload.maynor1024.live/file/1780037734572_article-55.png)

另一个常用插件是 Codex for Chrome。

![图片](https://upload.maynor1024.live/file/1780037734180_article-56.png)

它可以沿用你 Chrome 里已经登录的账号状态来操作网页。

并且会用 Tab Group 隔离工作区，不会把你的浏览器标签页搞乱。

![图片](https://upload.maynor1024.live/file/1780037740332_article-57.png)

软件下载完之后，你不一定要自己打开 Xcode 慢慢点。

可以继续让 Computer Use 帮你做后续编译和安装步骤。

![图片](https://upload.maynor1024.live/file/1780037744496_article-58.jpg)

操作过程中，电脑上方会显示 Codex 正在操控的状态提示。

![图片](https://upload.maynor1024.live/file/1780037748788_article-59.png)

不过遇到登录、密码、系统安全确认这类敏感步骤，它会停下来，让你自己操作。

![图片](https://upload.maynor1024.live/file/1780037751877_article-60.png)

剩下的步骤，继续让 Codex 一步步处理。

![图片](https://upload.maynor1024.live/file/1780037759668_article-61.png)

到了手机端，你需要自己完成一些物理操作：

- 用数据线连接 Mac 和 iPhone
- 打开开发者模式
- 重启手机
- 信任电脑
- 确认安装

这些 Codex 会给你提示，你照着做就行。

![图片](https://upload.maynor1024.live/file/1780037756414_article-62.png)

不一会，App 就能装到手机上。

![图片](https://upload.maynor1024.live/file/1780037759586_article-63.png)

雏形也跑起来了。

![图片](https://upload.maynor1024.live/file/1780037770432_article-64.png)

做到这里，你已经完成了从 0 到 1 的闭环：

| 步骤 | 结果 |
| --- | --- |
| 说出需求 | Codex 帮你整理方案 |
| 确认计划 | Codex 开始实现 |
| 生成项目 | 本地代码和文件落地 |
| 编译安装 | App 跑到手机上 |
| 继续修改 | 后续可以持续迭代 |

如果你还想继续远程开发，可以直接掏出手机操作 Codex。

目前需要 Mac 连接，iOS 和 Android 手机都可以。

我之前也写过一篇：

[《Codex 更新远程控制，你也终于可以在手机上随时随地 Vibe Coding 了。》](https://mp.weixin.qq.com/s?__biz=MzIyMzA5NjEyMA==&mid=2647682286&idx=1&sn=596aee2a6de3542e1e322d76913d738f&scene=21#wechat_redirect)

![图片](https://upload.maynor1024.live/file/1780037768165_article-65.png)

最后做出来的效果也没什么问题。

![图片](https://upload.maynor1024.live/file/1780037770443_article-66.png)

到时间后，会弹出提醒。

![图片](https://upload.maynor1024.live/file/1780037774395_article-67.jpg)

就很简单，也很有意思。

当然，如果你想上架 App Store，那就是另一套流程了，包括证书、签名、隐私说明、审核规则等，这里就不展开了。

## 写在最后：Mac 用户目前确实更爽

最后还得单独说一下：**现在 Codex 在 Mac 上的体验明显更完整。**

我整理了一张表，列了部分 Mac 支持但 Windows 暂时不支持的功能。

![图片](https://upload.maynor1024.live/file/1780037781277_article-68.png)

比如：

- **Computer Use**
- **远程手机连接**
- **Appshots**
- **Locked Computer Use**
- **Chronicle**

Appshots 可以双击 Command 键，把当前前台窗口截图和文字一起发给 Codex，不用再手动截图粘贴。

Locked Computer Use 可以让 Codex 在锁屏后继续操控 Mac。

Chronicle 则能记录屏幕上下文，让 Codex 更理解你最近在做什么。

这些能力对高频使用者来说非常香。

Windows 用户目前只能再等等。

## 最后的建议

如果你是第一次用 Codex，我建议不要一上来就做大项目。

更好的顺序是：

1. 先用对话做调研和规划；
2. 再新建项目做一个小网页；
3. 跑通浏览器预览和批注修改；
4. 再尝试做一个简单 App；
5. 最后再让 Codex 接管更复杂的自动化流程。

Codex 最强的地方，不是它能回答一个问题，而是它能进入你的工作目录，理解文件、修改文件、运行命令、打开浏览器、操作电脑，最后把一个真实任务推进到可验证的结果。

**从 0 到 1 做出第一个 iOS App，本质上不是为了做一个多厉害的 App。**

真正重要的是：你会理解 Codex 的工作方式。

你会知道什么时候该用计划模式，什么时候该给权限，什么时候该让它自动跑，什么时候该停下来自己确认。

这才是入门 Codex 最关键的一步。

希望大家 Coding 愉快。

***以上，既然看到这里了，如果觉得不错，随手点个赞、在看、转发三连吧。如果想第一时间收到推送，也可以给我个星标。谢谢你看我的文章，我们下次再见。***
