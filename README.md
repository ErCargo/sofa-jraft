# SOFAJRAFT

[![Build Status](https://travis-ci.com/alipay/sofa-jraft.svg?branch=master)](https://travis-ci.com/alipay/sofa-jraft)
![License](https://img.shields.io/badge/license-Apache--2.0-green.svg)
[![Maven Central](https://img.shields.io/maven-central/v/com.alipay.sofa/jraft-parent.svg?label=maven%20central)](https://search.maven.org/search?q=g:com.alipay.sofa%20AND%20sofa-jraft)

SOFAJRAFT 是一个基于 [RAFT](https://raft.github.io/) 一致性算法的生产级高性能 Java 实现，支持 MULTI-RAFT-GROUP，适用于高负载低延迟的场景。
使用 SOFAJRAFT 你可以专注于自己的业务领域，由 SOFAJRAFT 负责处理所有与 RAFT 相关的技术难题，并且 SOFAJRAFT 非常易于使用，你可以通过几个示例在很短的时间内掌握它。

## 功能特性
- Leader 选举
- 日志复制和恢复
- 快照和日志压缩
- 集群线上配置变更，增加节点、删除节点、替换节点等
- 主动变更 Leader，用于重启维护，Leader 负载平衡等
- 对称网络分区容忍性
- 非对称网络分区容忍性
- 容错性，少数派故障，不影响系统整体可用性
- 多数派故障时手动恢复集群可用
- 高效的线性一致读，ReadIndex/LeaseRead
- 流水线复制
- 内置了基于 [Metrics](https://metrics.dropwizard.io/4.0.0/getting-started.html) 类库的性能指标统计，有丰富的性能统计指标
- 通过了 [Jepsen](https://github.com/jepsen-io/jepsen) 一致性验证测试
- JRaft 中包含了一个嵌入式的分布式 KV 实现


## 需要
编译需要 JDK 8 及以上、Maven 3.2.5 及以上。

## 文档
- [用户指南](https://github.com/alipay/sofa-jraft/wiki)
- [Counter 例子详解](https://github.com/alipay/sofa-jraft/wiki/Counter-%E4%BE%8B%E5%AD%90%E8%AF%A6%E8%A7%A3)
- [版本发行日志](https://github.com/alipay/sofa-jraft/wiki/%E7%89%88%E6%9C%AC%E5%8F%91%E8%A1%8C%E6%97%A5%E5%BF%97)

## 如何贡献
[如何参与 SOFAJRAFT 代码贡献](https://github.com/alipay/sofa-jraft/wiki/%E5%A6%82%E4%BD%95%E5%8F%82%E4%B8%8E-SOFAJRAFT-%E4%BB%A3%E7%A0%81%E8%B4%A1%E7%8C%AE)

## 致谢
SOFAJRAFT 是从百度的 [braft](https://github.com/brpc/braft) 移植而来，做了一些优化和改进，感谢百度 braft 团队开源了优秀的 C++ RAFT 实现

## 开源许可
SOFAJRAFT 基于 [Apache License 2.0](https://github.com/alipay/sofa-rpc/blob/master/LICENSE) 协议，SOFAJRAFT 依赖了一些三方组件，它们的开源协议也为 Apache License 2.0
另外 SOFAJRAFT 也直接引用了一些开源的代码（可能有一些小小的改动）包括：
- [JCTools](https://github.com/JCTools/JCTools) 中的 NonBlockingHashMap/NonBlockingHashMapLong
- [Netty](https://github.com/netty/netty) 中的 HashedWheelTimer，另外还参考了 Netty 的 Pipeline 设计
- [Protobuf](https://github.com/protocolbuffers/protobuf) 中对 UTF8 String 高效的编码/解码


