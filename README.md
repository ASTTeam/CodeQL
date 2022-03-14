# 《深入理解漏洞挖掘神器CodeQL》

本项目用来收集整理CodeQL相关的内容。CodeQL在SAST领域越来越重要，可以利用已知的安全漏洞来挖掘类似的漏洞。本人开始持续学习CodeQL，持续用其进行漏洞挖掘。作者：[0e0w](https://github.com/0e0w)

本项目创建于2021年12月13日，最近的一次更新时间为2022年3月14日。

- [01-CodeQL技术资源]()
- [02-CodeQL基础内容]()
- [03-CodeQL高级使用]()
- [04-CodeQL使用案例]()
- [05-CodeQL参考资源]()

## 01-CodeQL技术资源

一、官方资源
- https://github.com/github/codeql
- https://github.com/github/codeql-go
- https://github.com/github/codeql-cli-binaries
- https://github.com/github/vscode-codeql-starter
- https://github.com/github/codeql-learninglab-actions

二、优秀资源
- https://lgtm.com/help/lgtm/ql/learning-ql
- https://lgtm.com
- https://github.com/SummerSec/learning-codeql
- https://github.com/safe6Sec/CodeqlNote
- https://github.com/SummerSec/LookupInterface
- https://github.com/ice-doom/codeql_compile
- https://github.com/Firebasky/CodeqlLearn
- https://github.com/j3ssie/codeql-docker
- https://github.com/Firebasky/CodeqlLearn
- [《代码分析平台CodeQL学习手记》](https://www.4hou.com/posts/o6wX)

三、其他资源
- https://tttang.com/archive/1415
- https://github.com/advanced-security/codeql-queries
- https://www.anquanke.com/post/id/203674
- https://www.anquanke.com/post/id/266823
- https://tttang.com/archive/1322

## 02-CodeQL基础内容

一、CodeQL安装

一、QL语言

- https://github.com/semmle/ql

二、CodeQL数据库

- 创建数据库

  - ```bash
    codeql database create java-database --language=java
    ```

  - ```bash
    codeql database create java-database --language=java --command='mvn clean install'
    ```

- 分析数据库

  - ```bash
    codeql database analyze java-database ql/security/CWE/CWE-020/UntrustedDataToExternalAPI.ql  --format=csv --output=result.csv
    ```

## 03-CodeQL高级使用

## 04-CodeQL使用案例

- https://www.jianshu.com/p/99942852a3aa

## 05-CodeQL参考资源