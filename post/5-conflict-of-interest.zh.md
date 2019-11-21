# 改善ACL利益冲突检测和审稿匹配流程
我们都知道ACL现在越来越壮大，这很振奋人心，这表明我们的研究社区发展迅速且充满活力。但与此同时，这也意味着会议管理方方面面的工作量也随之增加。特别是保障数千篇论文审稿过程的公平性是一个巨大的挑战，需要每个人在这个过程中做出大量工作，不论是程序委员会主席、领域主席，还是审稿人。

为了改进我们的审稿流程，ACL协会在ACL 2019大会时组建成立了专门的委员会。这个委员会的首要行动是将利益冲突（Conflict-of-Interest，COI）自动化管理，以及改进论文审稿匹配的（半）自动化。委员会广泛讨论了实现自动化的最佳方案，并根据相关决策编制了一份报告。

在本期的博文中，我们将简要介绍我们实施的方向。这也有助于说明为什么今年的ACL 2020大会要求作者和审稿人填写额外的表格（译者注：请参阅前期的博客内容，ACL 2020 PC Blog | 注意！投稿流程发生重大变化）。我们欢迎大家反馈关于该流程的任何建议！

## COI管理
ACL关于何种情况下会构成COI有一套官方的政策文件。具体来说，对于已经提交的论文，如果一个人满足如下条件，则认为是存在COI。
1. 论文的合著者
2. 在过去五年中，曾是其中一位作者的学生或导师
3. 在过去五年中，与其中一位作者有合著或合作过的论文
4. 与作者受雇于同一家公司或机构
5. 其他可能会导致论文审稿产生偏差的情况

为了确定是否存在COI，我们正在从以下来源收集信息，其中包括：
1. 使用START系统（即ACL提交论文的系统）中的用户信息。如果COI来源于上述条件中的#2、#4、#5，则可以被系统自动处理。这些信息只会被大会主席以及大会组织者获取到，并且只有作者或审稿人被加入到本次会议（例如：提交论文，表明自己愿意为本次会议审稿）。
2. 审稿人和作者通过START系统上的投稿；在Semantic Scholar上的论文，这是一个包含海量学术出版物的数据库（这允许我们找到一些没有在START系统中提交的论文以及这些论文的合著者）。

关于我们为什么选择了START系统（而不是其他审稿系统，例如OpenReview或者CMT）以及Semantic Scholar（而不是Google Scholar、ACL Anthology或者orcid）已在流程设计文档中进行过相关讨论。

## 审稿匹配
在近些年，对于\*ACL系列会议，我们通常采用如下流程来匹配论文和审稿人。首先我们会经过一个审稿人投标（reviewers bid）过程，会对论文给出yes/no/maybe的选择。然后领域主席会最终决定分配给每个审稿人的论文。这个过程非常耗时，并且随着会议规模的扩大，领域主席和审稿人的管理难度大大增加。最近的一些\*ACL系列会议引入了Toronto Paper Matching System（TPMS），但是会受限于覆盖度不足的问题，因为并不是所有审稿人都注册登记了该系统。

今年我们正在为ACL开发一个内部的论文匹配系统，其目标是创建一个初步的审稿人论文分配，然后领域主席可以进入系统并直接进行修改从而创建最终的论文分配。简单来说，这个系统会：
1. 从Semantic Scholar中收集ACL审稿人写过的论文
2. 根据（a）投稿到ACL的论文，（b）审稿人撰写过的论文，计算两者之间的相似度分数
3. 计算审稿人与该投稿论文的匹配程度，计算依据是根据审稿人撰写过的论文与该投稿论文的相似度最高的几篇论文的相似度得分
4. 创建审稿人论文分配，尝试分配最适合审稿人审阅的论文，但同时要确保审稿人不会受到太多或太少的审稿量

根据我们在ACL 2020的经验，我们也在考虑未来开展一个shared task来进一步提高审稿人分配算法。我们是NLP人，让我们用自己的技术来改进我们的流程！

## 我应该做什么？
1. 请尽快登录START系统，并修改个人的全局用户信息。首先进入到START系统（https://www.softconf.com/acl2020/），然后点击“Update Profile”。以下是相关截图：

![screenshot.png](https://acl2020.org/assets/images/profile_update_example.png)

以下是Semantic Scholar提供的信息，将告诉大家如何找到自己的Semantic Scholar Profile ID：第一种方法是在搜索引擎中搜索“Semantic Scholar”以及你的名字，然后找到与你本人对应的个人主页。另外一种方法是，在www.semanticscholar.org里搜索一篇你自己的论文，然后点击你的名字，或者直接搜索自己的名字并通过合著者等相关信息在右侧边栏中选择最匹配的条目。

Semantic Scholar与我们保持密切合作。如果你在个人资料中发现一些错误，可以采取如下措施：

你可以在个人资料中添加或删除相关论文（点击“CLAIM AUTHOR PAGE”）并且通过页面右上方的“Contact”按钮来提交论文信息的修改。你可以随时联系Semantic Scholar帮助中心(feedback@semanticscholar.org)来解决你的问题及疑惑。

2. 如果你对ACL 2020审稿感兴趣，或者你打算要提交ACL 2020的论文，请尽快填写ACL 2020作者/审稿人表单（译者注：请参阅前期的博客内容，ACL 2020 PC Blog | 注意！投稿流程发生重大变化）。
3. 如果程序委员会主席或者领域主席向你询问有关用户资料的问题，请及时进行回复。

## 致谢
Amanda和Graham感谢ACL审稿委员会和ACL程序委员会主席提供了建设性的反馈。他们还要感谢Emily Bender主动负责START系统中的COI管理，感谢Arya McCarthy和John Wieting实现了COI管理和审稿人匹配的相关系统程序。