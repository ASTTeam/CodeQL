# 《深入理解CodeQL》

![CodeQL](https://socialify.git.ci/ASTTeam/CodeQL/image?description=1&font=Inter&forks=1&issues=1&name=1&owner=1&pattern=Floating%20Cogs&pulls=1&stargazers=1&theme=Light)

本项目收集CodeQL相关内容，包括CodeQL的设计原理实现方法或使用CodeQL进行的漏洞挖掘案例等。其优点在于可以利用已知的漏洞信息来挖掘类似的漏洞，就像处理数据一样寻找漏洞。基于语义的代码分析思想在SAST领域更将会是一把利剑，这种思想更是下一代代码审计工具的发展方向。但CodeQL往往更适合开发人员对自己项目的漏洞自检，在某些环节处理上还存在较大问题，技术瓶颈有待提高。作者：[0e0w](https://github.com/0e0w)

本项目创建于2021年12月13日，最近的一次更新时间为2022年12月24日。

- [01-CodeQL资源](https://github.com/ASTTeam/CodeQL#01-CodeQL%E8%B5%84%E6%BA%90)
- [02-CodeQL基础](https://github.com/ASTTeam/CodeQL#02-codeql%E5%9F%BA%E7%A1%80)
- [03-CodeQL语言](https://github.com/ASTTeam/CodeQL#03-CodeQL%E8%AF%AD%E8%A8%80)
- [04-CodeQL进阶](https://github.com/ASTTeam/CodeQL#04-CodeQL%E8%BF%9B%E9%98%B6)
- [05-CodeQL案例](https://github.com/ASTTeam/CodeQL#05-CodeQL%E6%A1%88%E4%BE%8B)
- [06-CodeQL参考](https://github.com/ASTTeam/CodeQL#06-CodeQL%E5%8F%82%E8%80%83)

## 01-CodeQL资源

本章节收集整理CodeQL的相关资源内容，文章内容质量参差不齐，建议深入学习官方资源！

一、官方资源
- [ ] https://codeql.github.com/docs
- [ ] https://github.com/github/codeql
- [ ] https://github.com/github/codeql-go
- [ ] https://github.com/github/codeql-cli-binaries
- [ ] https://github.com/github/vscode-codeql-starter
- [ ] https://github.com/github/codeql-learninglab-actions
- [ ] https://github.com/github/securitylab/issues
- [ ] https://github.com/github/securitylab
- [ ] https://lgtm.com/help/lgtm/ql/learning-ql
- [ ] https://lgtm.com

二、优秀资源
- [ ] [《深入理解CodeQL》](https://github.com/ASTTeam/CodeQL)@0e0w
- [x] [《CodeQL 学习笔记》](https://www.yuque.com/loulan-b47wt/rc30f7/)@楼兰
- [x] [《Codeql学习笔记》](https://github.com/safe6Sec/CodeqlNote)@safe6Sec
- [x] [《记录学习codeql的过程》](https://github.com/Firebasky/CodeqlLearn)@Firebasky
- [x] [《CodeQL Java 全网最全的中文学习资料》](https://github.com/SummerSec/learning-codeql)@SummerSec
- [x] [《代码分析平台CodeQL学习手记》](https://www.4hou.com/posts/o6wX)@fanyeee
- [ ] [《静态分析☞CodeQL/Soot/SAST》](https://github.com/pen4uin/static-analysis)@pen4uin
- [x] [《Finding security vulnerabilities with CodeQL》](https://github.com/githubsatelliteworkshops/codeql)@GitHub Satellite Workshops
- [ ] [《CodeQL 寻找 JNDI利用 Lookup接口》](https://github.com/SummerSec/LookupInterface)@SummerSec
- [ ] ~~[《CodeQL中文入门教程》](https://github.com/Cl0udG0d/codeqlCnLearn)@Cl0udG0d~~
- [ ] https://github.com/haby0/mark
- [ ] https://github.com/johnjohncom/webinar-2021sep-codeql2
- [ ] https://github.com/githubsatelliteworkshops/codeql-cpp
- [ ] https://github.com/pwntester/codeql_grehack_workshop
- [ ] https://github.com/haby0/sec-note

三、视频资源
- [ ] [《CodeQL合集》](https://www.bilibili.com/video/BV1TL411L7ha)
- [ ] [《使用 CodeQL 挖掘 Java 应用漏洞》](https://www.bilibili.com/video/BV153411r7HW)
- [ ] [《Discover vulnerabilities with CodeQL》](https://www.bugbounty-videos.com/discover-vulnerabilities-with-codeql/)@admin4571
- [ ] https://www.youtube.com/watch?v=y_-pIbsr7jc
- [ ] https://www.youtube.com/watch?v=G_yDbouY0tM

四、学术刊物
- https://codeql.github.com/publications

五、其他资源
- 先知
- [x] https://xz.aliyun.com/search?keyword=Codeql
- [ ] [CodeQL 提升篇](https://xz.aliyun.com/t/10852)@Ironf4
- [ ] https://xz.aliyun.com/t/7789
- [ ] https://xz.aliyun.com/t/10829
- [ ] https://xz.aliyun.com/t/10756
- [ ] https://xz.aliyun.com/t/10755
- [ ] https://xz.aliyun.com/t/10707
- [ ] https://xz.aliyun.com/t/10046
- [ ] https://xz.aliyun.com/t/9275
- [ ] https://xz.aliyun.com/t/7979
- [ ] https://xz.aliyun.com/t/7657
- 跳跳糖
- [x] https://tttang.com/?keyword=codeql
- [ ] https://tttang.com/archive/1511
- [ ] https://tttang.com/archive/1512
- [ ] https://tttang.com/archive/1322
- [ ] https://tttang.com/archive/1353
- [ ] https://tttang.com/archive/1415
- [ ] https://tttang.com/archive/1378
- [ ] https://tttang.com/archive/1314
- [ ] https://tttang.com/archive/1497
- [ ] https://tttang.com/archive/1570
- [ ] https://tttang.com/archive/1660
- [ ] https://tttang.com/archive/1704
- 安全客
- [x] https://www.anquanke.com/search?s=codeql
- [ ] https://www.anquanke.com/post/id/266823
- [ ] https://www.anquanke.com/post/id/157583
- [ ] https://www.anquanke.com/post/id/212305
- [ ] https://www.anquanke.com/post/id/193171
- [ ] https://www.anquanke.com/post/id/266824
- 知乎
- [ ] https://www.zhihu.com/search?type=content&q=codeql
- [ ] https://zhuanlan.zhihu.com/p/354275826
- [ ] https://zhuanlan.zhihu.com/p/137569940
- [ ] https://zhuanlan.zhihu.com/p/479431942
- [ ] https://zhuanlan.zhihu.com/p/451369565
- [ ] https://zhuanlan.zhihu.com/p/92769710
- [ ] https://zhuanlan.zhihu.com/p/463665699
- [ ] https://zhuanlan.zhihu.com/p/451364774
- [ ] https://zhuanlan.zhihu.com/p/466504018
- [ ] https://zhuanlan.zhihu.com/p/448538180
- [ ] https://zhuanlan.zhihu.com/p/475499290
- [ ] https://zhuanlan.zhihu.com/p/466932373
- 微信
- [ ] https://mp.weixin.qq.com/s/jVZ3Op8FYBmiFAV3p0li3w
- [ ] https://mp.weixin.qq.com/s/KQso2nvWx737smunUHwXag
- [ ] https://mp.weixin.qq.com/s/sAUSgRAohFlmzwSkkWjp9Q
- [ ] https://mp.weixin.qq.com/s/3mlRedFwPz31Rwe7VDBAuA
- [ ] https://mp.weixin.qq.com/s/zSI157qJXYivSvyxHzXALQ
- [ ] https://mp.weixin.qq.com/s/Rqo12z9mapwlj6wGHZ1zZA
- [ ] https://mp.weixin.qq.com/s/DW0PJfRC0LtMOYx1CQPWpA
- Freebuf
- [x] https://search.freebuf.com/search/?search=codeql#article
- [ ] https://www.freebuf.com/articles/web/283795.html
- [ ] https://www.freebuf.com/articles/network/316551.html
- [ ] https://www.freebuf.com/sectool/291916.html
- [ ] https://wiki.freebuf.com/detail?wiki=106&post=319285
- Github
- [ ] https://github.com/Semmle/SecurityQueries
- [ ] https://github.com/artem-smotrakov/ql-fun
- [ ] https://github.com/s0/language-ql
- [ ] https://github.com/pwntester/codeql-cs-template
- [ ] https://github.com/ghas-bootcamp/ghas-bootcamp
- [ ] https://github.com/zbazztian/codeql-inject
- [ ] https://github.com/zbazztian/codeql-tools
- [ ] https://github.com/JLLeitschuh/lgtm_hack_scripts
- [ ] https://github.com/silentsignal/jms-codeql
- [ ] https://github.com/Marcono1234/codeql-jdk-docker
- [ ] https://github.com/j3ssie/codeql-docker
- [ ] https://github.com/microsoft/codeql-container
- [ ] https://github.com/zbazztian/codeql-debug
- [ ] https://github.com/dsp-testing/codeql-action
- [ ] https://github.com/uainc/codeql-example-01
- [ ] https://github.com/advanced-security/custom-codeql-bundle
- [ ] https://github.com/iflody/codeql-workshop
- [ ] https://github.com/dassencio/parallel-code-scanning
- [ ] https://github.com/advanced-security/codeql-basics
- [ ] https://github.com/vchekan/CodeQL
- [ ] https://github.com/ThibaudLopez/GHAS
- [ ] https://github.com/synacktiv/QLinspector
- [ ] https://github.com/advanced-security/codeql-workshop-2021-learning-journey
- Medium
- [ ] [《The journey of CodeQL》 ](https://medium.com/@qazbnm456/the-journey-of-codeql-part-1-cc4c6f3c610a)@Boik Su
- [ ] [《CodeQL thần chưởng》](https://testbnull.medium.com/codeql-th%E1%BA%A7n-ch%C6%B0%E1%BB%9Fng-part-1-544a2b0df9d7)@Jang
- [ ] [Hunting for XSS with CodeQL](https://medium.com/codex/hunting-for-xss-with-codeql-57f70763b938)@Daniel Santos
- [ ] [Detect dangerous RMI objects with CodeQL](https://medium.com/geekculture/detecting-dangerous-rmi-objects-with-codeql-33e03686921f)@Artem Smotrakov
- [ ] [About the CodeQL for research](https://medium.com/@lalida_a/about-the-codeql-for-research-c0686053337a)@Lalida Aramrueng
- [ ] [Detecting Jackson deserialization vulnerabilities with CodeQL](https://medium.com/geekculture/detecting-jackson-deserialization-vulnerabilities-with-codeql-8ec6353c5cc6)@Artem Smotrakov
- [ ] [Using CodeQL to detect client-side vulnerabilities in web applications](https://medium.com/@theRaz0r/using-codeql-to-detect-client-side-vulnerabilities-in-web-applications-1f4e4c773433)@Arseny Reutov
- 其他博客
- [ ] https://bestwing.me/codeql.html
- [ ] https://lfysec.top/2020/06/03/CodeQL%E7%AC%94%E8%AE%B0/
- [ ] https://docs.microsoft.com/zh-cn/windows-hardware/drivers/devtest/static-tools-and-codeql
- [ ] https://codeantenna.com/a/fnmZS3Qg4F
- [ ] https://www.cnblogs.com/goodhacker/p/
- [ ] https://geekmasher.dev/posts/sast/codeql-introduction
- [ ] http://blog.gamous.cn/post/codeql
- [ ] https://www.cnblogs.com/goodhacker/p/13583650.html
- [ ] https://yourbutterfly.github.io/note-site/module/semmle-ql/codeql
- [ ] https://fynch3r.github.io/tags/CodeQL
- [ ] https://blog.ycdxsb.cn/categories/research/codeql
- [ ] https://cloud.tencent.com/developer/article/1645870
- [ ] https://jorgectf.github.io/blog/post/practical-codeql-introduction
- [ ] https://www.slideshare.net/shabgrd/semmle-codeql
- [ ] https://blog.szfszf.top/article/59
- [ ] https://firebasky.github.io/2022/03/22/Codeql-excavate-Java-quadratic-deserialization
- [ ] https://www.synacktiv.com/en/publications/finding-gadgets-like-its-2022.html
- [ ] https://github.com/waderwu/extractor-java
- [ ] https://github.com/zbazztian/codeql-tools
- [ ] https://paper.seebug.org/1921
- [ ] https://github.com/webraybtl/codeQlpy

## 02-CodeQL基础

 本章节介绍CodeQL的基础用法及设计思路实现原理等！

- AST、source、sink、
- CodeQL的处理对象并不是源码本身，而是中间生成的AST结构数据库，所以我们先需要把我们的项目源码转换成CodeQL能够识别的CodeDatabase。
- 1、创建数据库。2、对数据库进行查找。3、分析查询结果发现漏洞
- Engine、Database、Queries
- AutoBuilder、extractor、trap、逻辑谓词、连接词、逻辑连接词、predicate
- CodeQL的缺点？不能直接通过打包好的程序进行代码审计。

一、CodeQL安装

二、CodeQL语法
- https://github.com/semmle/ql

三、CodeQL数据库
- https://github.com/waderwu/extractor-java
- https://lgtm.com/help/lgtm/generate-database
- 生成数据库之前，需要先保证被分析程序可以正常跑起来。
- 创建数据库
  - codeql database create java-db --language=java
  - codeql database create java-db --language=java --command='mvn clean install'
  - codeql database create cpp-database --language=cpp --command=make
  - codeql database create csharp-database --language=csharp --command='dotnet build /t:rebuild
  - codeql database create csharp-database --language=csharp --command='dotnet build /p:UseSharedCompilation=false /t:rebuild'
  - codeql database create java-database --language=java --command='gradle clean test'
  - codeql database create java-database --language=java --command='mvn clean install'
  - codeql database create java-database --language=java --command='ant -f build.xml'
  - codeql database create new-database --language=java --command='./scripts/build.sh'
- 分析数据库
  - codeql database analyze java-db CWE-020.ql --format=csv --output=result.csv

## 03-CodeQL语言

本章节介绍QL语言的语法规则，包括优秀规则等内容。CodeQL为王，规则为先！

一、基础语法

二、规则编写
- Java
- C#
- Go

三、官方规则

四、优秀规则
- [ ] [《My CodeQL queries collection》](https://github.com/cldrn/codeql-queries)@cldrn
- [ ] https://github.com/cor0ps/codeql
- [ ] https://github.com/GeekMasher/security-queries
- [ ] https://github.com/Marcono1234/codeql-java-queries
- [ ] https://github.com/imagemlt/myQLrules
- [ ] https://github.com/advanced-security/codeql-queries
- [ ] https://github.com/jenkins-infra/jenkins-codeql
- [ ] https://github.com/ice-doom/CodeQLRule
- [ ] https://github.com/zbazztian/codeql-queries

## 04-CodeQL进阶

本章节是针对不同的开发语言进行CodeQL扫描的例子，本章节待整理。

一、Java安全分析
- https://codeql.github.com/codeql-query-help/java
- https://codeql.github.com/codeql-standard-libraries/java
- https://lgtm.com/search?q=language%3Ajava&t=rules
- [ ] https://github.com/msrkp/codeql_for_gadgets
- [ ] https://github.com/chaimu100/java-test-for-codeql
- [ ] https://github.com/synacktiv/QLinspector

二、C#安全分析
- https://codeql.github.com/codeql-query-help/csharp/
- [ ] https://lgtm.com/search?q=language%3Acsharp&t=projects

三、Golang安全分析
- https://codeql.github.com/codeql-query-help/go/
- https://lgtm.com/search?q=language%3Ago&t=rules
- [ ] https://lgtm.com/search?q=language%3Ago&t=projects
- [ ] https://codeql.github.com/codeql-standard-libraries/go
- [ ] https://github.com/github/codeql-ctf-go-return
- [ ] https://github.com/gagliardetto/codemill
- [ ] http://f4bb1t.com/post/2020/12/16/codeql-for-golang-practise3
- [ ] https://www.freebuf.com/articles/web/253491.html

四、Python
- https://codeql.github.com/codeql-query-help/python/
- [ ] https://github.com/10thmagnitude/custom-codeql-python
- [ ] https://github.com/AlexAltea/codeql-python

五、C++安全分析
- [ ] https://github.com/trailofbits/itergator
- [ ] https://github.com/0xcpu/codeql-uboot
- [ ] https://github.com/RadCet/CodeQL

六、Ruby
- https://github.com/agius/codeql_ruby

七、CodeQL工具
- [ ] https://github.com/ice-doom/codeql_compile
- [x] https://github.com/hudangwei/codemillx
- [ ] https://github.com/gagliardetto/codemill
- [ ] https://github.com/pwntester/codeql.nvim
- [ ] https://github.com/gagliardetto/codebox

## 05-CodeQL案例

本章节介绍CodeQL的具体使用案例，包括自己通过CodeQL挖掘的漏洞等内容。

一、大型应用分析
- 分析Shiro
  - https://www.anquanke.com/post/id/256967
- 分析Fastjson
  - https://xz.aliyun.com/t/7482
  - https://www.buaq.net/go-98696.html
  - https://www.anquanke.com/post/id/281733
- 分析Log4j
  - https://www.anquanke.com/post/id/255721
  - https://www.freebuf.com/articles/web/318141.html
  - https://mp.weixin.qq.com/s/JYco8DysQNszMohH6zJEGw
- 分析Dubbo
  - https://github.com/github/codeql-dubbo-workshop
  - https://mp.weixin.qq.com/s/B-uhbd5FApxSXnjPEFzArQ
  - https://securitylab.github.com/research/apache-dubbo
- 分析kylin
  - https://xz.aliyun.com/t/8240
- 分析grafana
  - https://xz.aliyun.com/t/10648
  - [用codeql分析grafana最新任意文件读取](https://github.com/safe6Sec/codeql-grafana)
- 分析Hadoop
  - https://mp.weixin.qq.com/s/CyhWw4t8LdGhCpixacb6Xg
- 分析Struts2
  - https://www.anquanke.com/post/id/157583

二、代码审计案例
- https://www.anquanke.com/post/id/203674
- https://www.jianshu.com/p/99942852a3aa
- https://www.anquanke.com/post/id/202987
- https://mp.weixin.qq.com/s/LmOFGAhqAKiO8VDQW4vvLg
- https://github.com/hac425xxx/codeql-snippets
- https://github.com/elManto/StaticAnalysisQueries

## 06-CodeQL参考

- https://github.com/ASTTeam/CodeQL
- https://github.com/pwntester
- [微信公众号：xsser的博客](https://mp.weixin.qq.com/mp/profile_ext?action=home&__biz=MzA4NzA5OTYzNw==&scene=123#wechat_redirect)
- [微信公众号：楼兰学习网络安全](https://mp.weixin.qq.com/s/7wJKMVyc36U-PciZGmjrcg)

## Stargazers

[![Stargazers @ASTTeam/CodeQL](https://reporoster.com/stars/ASTTeam/CodeQL)](https://github.com/ASTTeam/CodeQL/stargazers)

## Forkers

[![Forkers @ASTTeam/CodeQL](https://reporoster.com/forks/ASTTeam/CodeQL)](https://github.com/ASTTeam/CodeQL/network/members)

![](01-CodeQL资源/TEMP/wx.png)

[![Stargazers over time](https://starchart.cc/ASTTeam/CodeQL.svg)](https://starchart.cc/ASTTeam/CodeQL)
