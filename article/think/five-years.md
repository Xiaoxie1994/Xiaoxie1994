# 工作五年小结 | 面对不确定性快速上升的外部环境，我们该如何寻求突破？
## 1. 前言
工作五年了，来京东马上满一年，前四年在开水团，不禁感叹时间过的真快啊！回想19年从西安交大硕士毕业孤身前往北京开始职业生涯，经历了孤独迷茫到自立坚定，再到23年下定决心携妻还蜀安家，并来到京东开始新的征程，这5年过的很快也很充实。

今年也是我的而立之年，感觉一迈过这个坎，眼前的世界就不一样了，事业上还未成气候，更多的生活琐事就开始扑面而来。网上有段子笑称现代的“五子登科”中的五子分别指的是“车子、票子、房子、妻子和孩子”，这个词本来表达的是人们对美好生活的向往，但旧词新义体现更多的是中年人的无奈。

<img src="image-1.png" alt="复杂性的世纪" width="500">

英国物理学家霍金曾说“**21世纪将是复杂性的世纪**”，科学的事我不懂，但我的直观感受是各行各业的复杂性都在持续的上涨且很快。就程序员这个职业来说，面试的难度是越来越大，当然面试可能存在一定的造火箭行为，但工作整体的难度确实是在逐年上涨。举个例子，之前业务开发主要工作是完成需求编码，而且由于很多都是新开业务也不存在太多历史债务，工作的条线和职责比较清晰。但随着业务进入成熟期，增长变缓导致更多的运维负担和质量问题开始凸显，开发不仅要完成基本的编码，也需要参与到更多**运维监控和质量保障**工作中，这使得工作的内容变得复杂多样，认知负载极速增加。而且就算是基本的编码工作，为了保证能适应未来发展趋势也会在前期投入更多精力进行方案设计，越来越考验开发的知识储备和架构思维。

同时新的技术在不断地出现并对我们的工作造成实际的影响，从2022年12月OpenAi发布**ChatGPT**至今不到两年时间里，大模型已经侵入到了生活中的方方面面。哪个程序员敢说自己完全没有用过大模型，基于大模型衍生的编码辅助、智能问答、内容&图片生成等工具真真切切的影响到了我们工作的方式。开发已然变成了一个**复合型职业**，对个人能力提出了更高要求。

<img src="image-2.png" alt="复合型职业" width="500">

外部环境的走向不是个人能够左右的，因此我不聊公司或城市的差异，也不聊如何和生活琐事对线，仅仅聊一下“**个人成长**”，因为这个话题的主动权掌握在我们自己手上，最好的投资就是投资自己（想到A股😭）。那么在这个复杂性快速上升的21世纪，面对不确定性上升的外部环境，我们该如何寻求突破呢？我当前的答案是：**持续学习，制造正反馈，相信复利效应。**

## 2. 收获
### 2.1 业务理解
目前参与的业务方向具有保密性质并逐渐进入成熟期，系统架构也逐渐趋于稳定，日常的工作内容更多投入在技术支持、运维监控和质量保障上，系统功能迭代频率下降，部分开发精力投入在提效工具建设上。由于项目保密性质，这里就不展开说明业务上的具体工作内容，仅对如何快速了解业务知识和熟悉系统代码进行总结。

#### 2.1.1 了解业务
我学习业务知识的基本思路是“**读->想->写->讲**”四步循环，下面是具体的执行步骤，其中步骤2→6我会多跑几轮，逐渐建立起深入的业务认识。

- **① 信息收集**：尽可能检索业务和系统相关的文档、分享视频、代码和配置数据等；
- **② 信息整合**：从用户视角出发串联业务流程，并将流程拆分成独立的功能模块。整合不仅仅聚焦于负责的业务，也要考虑到上下游；
- **③ 功能细化**：针对业务各个模块进行细化，包含模块主要功能、输入输出定义和交互中间件等，思路可以参考[C4模型](https://www.infoq.cn/article/c4-architecture-model)；
- **④ 文档沉淀**：将理解的内容整理成文档，从背景、名词、现状、未来发展等方面进行叙述，串联业务和系统整个生命周期；
- **⑤ 业务串讲**：将总结的内容分享出来，并收集熟悉业务听众的反馈（收集反馈很重要，老同事能够指出难以发现的细枝末节并分享一些历史原因导致的设计缺陷）；
- **⑥ 认知迭代**：基于新的输入重新迭代自己的业务认知。

<img src="image-3.png" alt="了解业务步骤" width="800">

#### 2.1.2 熟悉代码

可以找之前负责的同事领读，不过这种方式只能对项目有一个大致的认识，具体的细节很难面面俱到。熟悉代码没有捷径，只能通过阅读代码，但阅读代码是有方法的。关于如何高效阅读代码我还没有总结出一套完整的方案，不过大体的思路是**方法+工具**结合方式：从系统入口开始，结合业务完整跑通核心链路，若有不懂的逻辑可以使用debug或代码分析工具，边读边做好笔记，并最好进行一次代码串讲收集反馈。下面推荐一些经验总结：

- **① 阅读代码方法**：[如何阅读代码](https://www.thoughtworks.com/zh-cn/insights/blog/careers-at-thoughtworks/how-to-read-code)、[how-to-interrogate-unfamiliar-code](https://stackoverflow.blog/2022/08/15/how-to-interrogate-unfamiliar-code/)、[如何高效阅读源代码](https://catcoding.me/p/learn-from-source-code/)

- **② 阅读代码工具**：[想提高阅读代码的效率？试试这些工具吧！](https://www.shawnxie.top/archives/1716733748336)

<img src="image-4.png" alt="阅读代码工具" width="500">

不过工具和方法永远不是最重要的，**去读**，并在遇到困难的时候，看不明白的时候，咬牙坚持下去，抽丝剥茧，逐个击破。

### 2.2 技术提升

技术能力是开发的立足之本，因此前言中提到的寻求突破更多指的是技术能力上的突破，提升的方法我采取三步走：**持续学习，制造正反馈，相信复利效应。**

<img src="image-5.png" alt="技术提升" width="500">


#### 2.2.1 持续学习

<img src="image-6.png" alt="持续学习" width="500">

为什么需要持续学习，说白了是为了适应社会发展和保持个人竞争力，只出不进，我们将很快达到能力瓶颈。

- **应对快速变化的世界**：世界经济论坛2020年的[一份报告](https://www.weforum.org/publications/the-future-of-jobs-report-2020/)说到 2025 年，员工执行工作所需的 44% 的技能将因快速的技术进步而改变。持续学习可以帮助我们跟上这些变化，不被时代淘汰。
- **个人成长与发展**：通过持续学习，我们可以扩展自己的知识面，有朝一日也会运用到工作中去解决问题。
- **保持心理健康**：持续学习有助于保持大脑活跃，预防认知衰退，并且可以带来心理上的满足感和幸福感，扩展阅读“[锻炼大脑，这里有一套全指南](https://36kr.com/p/2857916221541250)”。

#### 2.2.2 制造正反馈

正反馈能提供持续学习的动力，适当的正反馈也有利于习惯的培养。我目前通过分享来获得正反馈，分享带来的阅读量、评论、点赞和收藏都会促使我继续学习并分享，而且反馈中的建议也很宝贵，能够指出我的知识盲区。目前保持了两个分享习惯：

- **每月在内部社区发表一篇文章（部分已同步外网）**

要特别感谢公司神灯社区，从去年10月发布第一篇文章开始，我基本保持一月一篇的频率，神灯社区的互动和积分给我带来了大量的正反馈，提供了我持续学习的动力ღ( ´･ᴗ･` )。

|   |   |
|---|---|
|**时间**|**文章**|
|2023.10|[浅析“代码可视化”](https://juejin.cn/post/7291321879321641019)|
|2023.11|[【代码可视化实践】代码变更影响分析](https://juejin.cn/post/7304561386889543706)|
|2024.1|[想提高阅读代码的效率？试试这些工具吧！](https://www.shawnxie.top/archives/1716733748336)|
|2024.2|“代码可视化”导图|
|2024.3|[实现“代码可视化”需要了解的前置知识-编译器前端](https://juejin.cn/post/7356625386665033728)|
|2024.4|[离开工位老是忘记锁屏？试着让电脑自动完成这事吧！](https://www.shawnxie.top/archives/1716735829719)|
|2024.5|[实现“代码可视化”需要了解的前置知识-编译器中端](https://juejin.cn/post/7371000326131302450)|
|2024.5|[看不懂正则表达式？试试可视化工具吧！](https://www.shawnxie.top/archives/1716736791836)|
|2024.6|[没时间了解技术热点？让大模型帮你整理重点吧！](https://www.shawnxie.top/archives/1722760319667)|
|2024.7|[用 AI 解锁技术调研的新姿势](https://www.shawnxie.top/archives/1725364383512)|
|2024.8|2024黑马海选 \| 不做牛马队-孤岛函数治理|
|2024.8|2024黑马初赛 \| 不做牛马队-孤岛函数治理（完结）|

- **每周将感兴趣的内容整理为技术周刊**

写周刊的目的是提高知识的留存率，当然也能带来各种正反馈😁。目前已经坚持了两个月，虽然会牺牲周末半天时间且发布后也没啥阅读量😭，但基本的目的达成了，希望能保持下去。感兴趣的同学可搜索公众号“肖恩杂谈”订阅一下🥺，历史文章查看：[技术周刊合集](https://mp.weixin.qq.com/mp/appmsgalbum?__biz=MzkwODY0ODQzOQ==&action=getalbum&album_id=3492416248238096386#wechat_redirect)。

<img src="image-7.png" alt="技术周刊合集" width="500">

#### 2.2.3 相信复利效应

<img src="image-8.png" alt="技术周刊合集" width="500">

“**复利是世界第八大奇迹**”，谣传是爱因斯坦所说，但无据可查。不过不管是谁说的，复利本身带来的效果是可观的，下面是一个简单的复利公式（F为收益，P为本金，i为利率，n为时间）。

<img src="image.png" alt="复利计算公式" width="200">

根据公式我们只需要每天比昨天的自己进步**0.1%**，那么一年后的个人能力将比一年前的自己提升**44.03%**（1*(1+0.001)^365-1），虽然这是理想数据，但足以说明持续学习的效果是可观的。

我也在用实际的行动验证，24年初立了个Flag🚩：写一本关于“代码可视化”的GitBook，目前[《Code Visualization》](https://xiexiao064.gitbook.io/code-visualization)在持续施工中，希望有生之年能写完吧😁，感兴趣的朋友可以先睹为快，提提建议。

<img src="image-9.png" alt="Code Visualization" width="800">


## 3. 未来展望

按照前文的思路进行积累，可能会出现知识储备了很多但工作中实际用到很少，导致一些割裂感。出现这种情况不能武断的认为学的东西没有用，很可能只是在当前的场景下暂时还用不上。知识的储备和应用就像树木地下和地上部分，根系越深越广，躯干部分才能茁壮成长。对于未来，我将继续践行自己的成长理论，并逐渐在工作中运用新学到的知识，产生价值。

<img src="image-10.png" alt="持续积累" width="400">


## 4. 学习资料
由于每个人需要学习的内容不同，文中只给出了一些学习理论并没有提供实际的学习案例分享。在最后这里分享一下收集的部分学习资料（均来自网络），GitHub Stars合集“[学习资料](https://github.com/stars/Xiaoxie1994/lists/%E5%AD%A6%E4%B9%A0%E8%B5%84%E6%96%99)”会持续更新，大家如果有其他推荐也可以发在评论区。
- [千古前端图文教程](https://web.qianguyihao.com/)
- [前端技能汇总 Frontend Knowledge Structure](https://github.com/JacksonTian/fks)
- [《系统重构与迁移指南》](https://github.com/phodal/migration)
- [Hello 算法](https://www.hello-algo.com/)
- [free-programming-books](https://ebookfoundation.github.io/free-programming-books/)
- [计算机电子书](https://github.com/it-ebooks-0)
- [CS自学指南](https://csdiy.wiki/)
- [awesome](https://github.com/sindresorhus/awesome)
- [《动手学深度学习》](https://zh.d2l.ai/)
- [Java 全栈知识体系](https://pdai.tech/)
- [freecodecamp](https://www.freecodecamp.org/learn/)
- [system-design-primer](https://github.com/donnemartin/system-design-primer)
- [awesome-software-architecture](https://github.com/mehdihadeli/awesome-software-architecture)
- [generative-ai-for-beginners](https://github.com/microsoft/generative-ai-for-beginners)
- [30-Days-Of-Python](https://github.com/Asabeneh/30-Days-Of-Python)
- [developer-roadmap](https://github.com/kamranahmedse/developer-roadmap)
- [89 things I know about Git commits](https://www.jvt.me/posts/2024/07/12/things-know-commits/)
- [java-design-patterns](https://github.com/iluwatar/java-design-patterns)
- [coding-interview-university](https://github.com/jwasham/coding-interview-university)
- [Reverse Engineering For Everyone!](https://0xinfection.github.io/reversing/)
- [developer2gwy](https://github.com/miss-mumu/developer2gwy)
- [build-your-own-x](https://github.com/codecrafters-io/build-your-own-x)
- [everyone-can-use-english](https://github.com/ZuodaoTech/everyone-can-use-english)
- [python-whydo](https://github.com/chinesehuazhou/python-whydo)
- [algo](https://github.com/wangzheng0822/algo)
- [PL-Compiler-Resource](https://github.com/shining1984/PL-Compiler-Resource)