# 《深入理解CodeQL》

本项目收集整理CodeQL相关内容，包括CodeQL的设计原理实现方法或使用CodeQL进行的漏洞挖掘案例等。CodeQL基于语义的代码分析思想在SAST领域将会是一把利剑，CodeQL是下一代代码审计工具。可以通过CodeQL利用已知的漏洞信息来挖掘类似的漏洞，就像处理数据一样寻找漏洞。作者：[0e0w](https://github.com/0e0w)

本项目创建于2021年12月13日，最近的一次更新时间为2022年3月17日。

- [01-CodeQL技术资源](https://github.com/ASTTeam/CodeQL#01-codeql%E6%8A%80%E6%9C%AF%E8%B5%84%E6%BA%90)
- [02-CodeQL基础内容](https://github.com/ASTTeam/CodeQL#02-codeql%E5%9F%BA%E7%A1%80%E5%86%85%E5%AE%B9)
- [03-CodeQL高级进阶](https://github.com/ASTTeam/CodeQL#03-codeql%E9%AB%98%E7%BA%A7%E8%BF%9B%E9%98%B6)
- [04-CodeQL规则工具](https://github.com/ASTTeam/CodeQL#04-codeql%E8%A7%84%E5%88%99%E5%B7%A5%E5%85%B7)
- [05-CodeQL使用案例](https://github.com/ASTTeam/CodeQL#05-codeql%E4%BD%BF%E7%94%A8%E6%A1%88%E4%BE%8B)
- [06-CodeQL参考资源](https://github.com/ASTTeam/CodeQL#06-codeql%E5%8F%82%E8%80%83%E8%B5%84%E6%BA%90)

## 01-CodeQL技术资源

一、官方资源
- [ ] https://codeql.github.com/docs
- [ ] https://github.com/github/codeql
- [ ] https://github.com/github/codeql-go
- [ ] https://github.com/github/codeql-cli-binaries
- [ ] https://github.com/github/vscode-codeql-starter
- [ ] https://github.com/github/codeql-learninglab-actions
- [ ] https://github.com/github/securitylab
- [ ] https://lgtm.com/help/lgtm/ql/learning-ql
- [ ] https://lgtm.com

二、优秀资源
- [ ] [《深入理解CodeQL》](https://github.com/ASTTeam/CodeQL)@0e0w
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
- [ ] https://www.youtube.com/watch?v=y_-pIbsr7jc
- [ ] https://www.youtube.com/watch?v=G_yDbouY0tM

四、学术刊物
- https://codeql.github.com/publications

五、其他资源
- 先知
- [ ] https://xz.aliyun.com/search?keyword=Codeql
- [ ] https://xz.aliyun.com/t/7789
- 跳跳糖
- [ ] https://tttang.com/archive/1322
- [ ] https://tttang.com/archive/1353
- [ ] https://tttang.com/archive/1415
- 安全客
- [ ] https://www.anquanke.com/post/id/266823
- [ ] https://www.anquanke.com/post/id/157583
- [ ] https://www.anquanke.com/post/id/212305
- 知乎
- [ ] https://zhuanlan.zhihu.com/p/354275826
- 微信
- [ ] https://mp.weixin.qq.com/s/jVZ3Op8FYBmiFAV3p0li3w
- [ ] https://mp.weixin.qq.com/s/KQso2nvWx737smunUHwXag
- [ ] https://mp.weixin.qq.com/s/sAUSgRAohFlmzwSkkWjp9Q
- [ ] https://mp.weixin.qq.com/s/3mlRedFwPz31Rwe7VDBAuA
- [ ] https://mp.weixin.qq.com/s/zSI157qJXYivSvyxHzXALQ
- [ ] https://mp.weixin.qq.com/s/Rqo12z9mapwlj6wGHZ1zZA
- Freebuf
- Githab
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

## 02-CodeQL基础内容

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

## 03-CodeQL高级进阶

一、Java安全分析
- https://codeql.github.com/codeql-query-help/java
- https://codeql.github.com/codeql-standard-libraries/java
- https://lgtm.com/search?q=language%3Ajava&t=rules
- [ ] https://github.com/msrkp/codeql_for_gadgets
- [ ] https://github.com/chaimu100/java-test-for-codeql

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

## 04-CodeQL规则工具

一、CodeQL规则
- Java
- C#
- Go
- [ ] [《My CodeQL queries collection》](https://github.com/cldrn/codeql-queries)@cldrn
- [ ] https://github.com/cor0ps/codeql
- [ ] https://github.com/GeekMasher/security-queries
- [ ] https://github.com/Marcono1234/codeql-java-queries
- [ ] https://github.com/imagemlt/myQLrules
- [ ] https://github.com/advanced-security/codeql-queries
- [ ] https://github.com/jenkins-infra/jenkins-codeql

二、CodeQL工具
- [ ] https://github.com/ice-doom/codeql_compile
- [x] https://github.com/hudangwei/codemillx
- [ ] https://github.com/gagliardetto/codemill
- [ ] https://github.com/pwntester/codeql.nvim
- [ ] https://github.com/gagliardetto/codebox

## 05-CodeQL使用案例

一、大型应用分析
- 分析Shiro
  - https://www.anquanke.com/post/id/256967
- 分析Fastjson
  - https://xz.aliyun.com/t/7482
  - https://www.buaq.net/go-98696.html
- 分析Log4j
  - https://www.anquanke.com/post/id/255721
  - https://mp.weixin.qq.com/s/JYco8DysQNszMohH6zJEGw
- 分析Dubbo
  - https://github.com/github/codeql-dubbo-workshop
  - https://mp.weixin.qq.com/s/B-uhbd5FApxSXnjPEFzArQ
  - https://securitylab.github.com/research/apache-dubbo
- 分析kylin
  - https://xz.aliyun.com/t/8240
- 分析grafana
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

## 06-CodeQL参考资源

- https://github.com/ASTTeam/CodeQL
- https://github.com/pwntester

![](01-CodeQL技术资源/TEMP/wx.png)

[![Stargazers over time](https://starchart.cc//ASTTeam/CodeQL.svg)](https://starchart.cc/ASTTeam/CodeQL)