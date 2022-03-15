# 《深入理解CodeQL》

本项目用来收集整理CodeQL相关的内容，包括CodeQL的设计原理实现方法以及使用CodeQL进行漏洞挖掘的案例等。CodeQL在SAST领域将会是一把利剑，被誉为下一代的代码审计工具。低级0day挖掘工程师可以借助CodeQL利用已知的漏洞来挖掘类似的漏洞。本人开始持续学习CodeQL，持续用其进行漏洞挖掘。努力成为低级0day挖掘工程师！作者：[0e0w](https://github.com/0e0w)

本项目创建于2021年12月13日，最近的一次更新时间为2022年3月15日。

- [01-CodeQL技术资源]()
- [02-CodeQL基础内容]()
- [03-CodeQL高级使用]()
- [04-CodeQL辅助工具]()
- [05-CodeQL使用案例]()
- [06-CodeQL参考资源]()

## 01-CodeQL技术资源

一、官方资源
- [ ] https://github.com/github/codeql
- [ ] https://github.com/github/codeql-go
- [ ] https://github.com/github/codeql-cli-binaries
- [ ] https://github.com/github/vscode-codeql-starter
- [ ] https://github.com/github/codeql-learninglab-actions
- [ ] https://github.com/github/securitylab
- [ ] https://codeql.github.com/docs
- [ ] https://lgtm.com/help/lgtm/ql/learning-ql
- [ ] https://lgtm.com
- [ ] https://codeql.github.com

二、优秀资源
- [ ] [《深入理解CodeQL》](https://github.com/ASTTeam/CodeQL)@0e0w
- [ ] [《Codeql学习笔记》](https://github.com/safe6Sec/CodeqlNote)@safe6Sec
- [x] [《记录学习codeql的过程》](https://github.com/Firebasky/CodeqlLearn)@Firebasky
- [ ] [《CodeQL 寻找 JNDI利用 Lookup接口》](https://github.com/SummerSec/LookupInterface)@SummerSec
- [ ] [《CodeQL Java 全网最全的中文学习资料》](https://github.com/SummerSec/learning-codeql)@SummerSec
- [ ] [《代码分析平台CodeQL学习手记》](https://www.4hou.com/posts/o6wX)
- [ ] [《静态分析☞CodeQL/Soot/SAST》](https://github.com/pen4uin/static-analysis)@pen4uin
- [ ] [《Finding security vulnerabilities with CodeQL》](https://github.com/githubsatelliteworkshops/codeql)@GitHub Satellite Workshops
- [ ] https://github.com/pwntester/codeql_grehack_workshop
- [ ] https://github.com/johnjohncom/webinar-2021sep-codeql2
- [ ] https://github.com/githubsatelliteworkshops/codeql-cpp
- [ ] https://github.com/haby0/sec-note
- [ ] ~~[《CodeQL中文入门教程》](https://github.com/Cl0udG0d/codeqlCnLearn)@Cl0udG0d~~

三、其他资源
- [ ] https://tttang.com/archive/1322
- [ ] https://tttang.com/archive/1353
- [ ] https://tttang.com/archive/1415
- [ ] https://www.anquanke.com/post/id/203674
- [ ] https://www.anquanke.com/post/id/266823
- [ ] https://www.anquanke.com/post/id/157583
- [ ] https://www.anquanke.com/post/id/212305
- [ ] https://xz.aliyun.com/search?keyword=Codeql
- [ ] https://github.com/j3ssie/codeql-docker
- [ ] https://github.com/microsoft/codeql-container
- [ ] https://github.com/zbazztian/codeql-debug
- [ ] https://github.com/dsp-testing/codeql-action
- [ ] https://github.com/uainc/codeql-example-01
- [ ] https://github.com/advanced-security/custom-codeql-bundle
- [ ] https://github.com/iflody/codeql-workshop
- [ ] https://github.com/dassencio/parallel-code-scanning
- [ ] https://github.com/gagliardetto/codebox
- [ ] https://github.com/advanced-security/codeql-basics
- [ ] https://github.com/vchekan/CodeQL
- [ ] https://github.com/ThibaudLopez/GHAS
- [ ] https://bestwing.me/codeql.html
- [ ] https://lfysec.top/2020/06/03/CodeQL%E7%AC%94%E8%AE%B0/
- [ ] https://docs.microsoft.com/zh-cn/windows-hardware/drivers/devtest/static-tools-and-codeql
- [ ] https://codeantenna.com/a/fnmZS3Qg4F
- [ ] https://www.cnblogs.com/goodhacker/p/
- [ ] https://geekmasher.dev/posts/sast/codeql-introduction
- [ ] https://mp.weixin.qq.com/s/jVZ3Op8FYBmiFAV3p0li3w
- [ ] https://mp.weixin.qq.com/s/KQso2nvWx737smunUHwXag
- [ ] https://mp.weixin.qq.com/s/sAUSgRAohFlmzwSkkWjp9Q
- [ ] https://blog.ycdxsb.cn/categories/research/codeql
- [ ] https://xz.aliyun.com/t/7789

## 02-CodeQL基础内容

 本章节介绍CodeQL的基础用法及设计思路实现原理等！

- AST、source、sink、
- CodeQL的处理对象并不是源码本身，而是中间生成的AST结构数据库，所以我们先需要把我们的项目源码转换成CodeQL能够识别的CodeDatabase。
- 1、创建数据库。2、对数据库进行查找
- Engine、Database、Queries

一、CodeQL安装

二、QL语言
- https://github.com/semmle/ql

三、CodeQL数据库
- 创建数据库
  - codeql database create java-db --language=java
  - codeql database create java-db --language=java --command='mvn clean install'
- 分析数据库
  - codeql database analyze java-db CWE-020.ql --format=csv --output=result.csv

## 03-CodeQL高级使用

一、Java安全分析
- https://github.com/msrkp/codeql_for_gadgets
- https://github.com/chaimu100/java-test-for-codeql

二、C#安全分析
- https://lgtm.com/search?q=language%3Acsharp&t=projects

三、Golang安全分析
- https://lgtm.com/search?q=language%3Ago&t=projects
- https://codeql.github.com/codeql-standard-libraries/go
- https://github.com/github/codeql-ctf-go-return
- https://github.com/gagliardetto/codemill
- http://f4bb1t.com/post/2020/12/16/codeql-for-golang-practise3

四、Python
- https://github.com/10thmagnitude/custom-codeql-python
- https://github.com/AlexAltea/codeql-python

五、C++安全分析
- https://github.com/trailofbits/itergator
- https://github.com/0xcpu/codeql-uboot
- https://github.com/RadCet/CodeQL

六、Ruby
- https://github.com/agius/codeql_ruby

## 04-CodeQL规则工具

一、CodeQL规则
- [ ] [《My CodeQL queries collection》](https://github.com/cldrn/codeql-queries)@cldrn
- [ ] https://github.com/cor0ps/codeql
- [ ] https://github.com/GeekMasher/security-queries
- [ ] https://github.com/Marcono1234/codeql-java-queries
- [ ] https://github.com/imagemlt/myQLrules
- [ ] https://github.com/advanced-security/codeql-queries

二、CodeQL工具
- [ ] https://github.com/ice-doom/codeql_compile
- [x] https://github.com/hudangwei/codemillx
- [ ] https://github.com/gagliardetto/codemill
- [ ] https://github.com/pwntester/codeql.nvim

## 05-CodeQL使用案例

一、大型应用分析
- 分析Shiro
  - https://www.anquanke.com/post/id/256967
- 分析Fastjson
  - https://www.buaq.net/go-98696.html
  - https://xz.aliyun.com/t/7482
- 分析Log4j
- https://github.com/github/codeql-dubbo-workshop
- https://www.anquanke.com/post/id/255721
- https://mp.weixin.qq.com/s/B-uhbd5FApxSXnjPEFzArQ
- https://securitylab.github.com/research/apache-dubbo
- https://mp.weixin.qq.com/s/JYco8DysQNszMohH6zJEGw
- https://www.anquanke.com/post/id/255721
- https://xz.aliyun.com/t/8240

二、代码审计案例
- https://www.jianshu.com/p/99942852a3aa
- [用codeql分析grafana最新任意文件读取](https://github.com/safe6Sec/codeql-grafana)
- https://mp.weixin.qq.com/s/LmOFGAhqAKiO8VDQW4vvLg

## 06-CodeQL参考资源

- https://github.com/ASTTeam/CodeQL

[![Stargazers over time](https://starchart.cc//ASTTeam/CodeQL.svg)](https://starchart.cc/ASTTeam/CodeQL)