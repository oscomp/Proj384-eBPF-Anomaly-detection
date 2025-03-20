# 基于eBPF的容器异常智能检测框架与方法

## 项目描述

容器环境的大规模高动态性，为运行其中的微服务造成了安全隐患。容器生命周期短，频繁创建和销毁，导致环境变化迅速，而传统的静态配置管理和监控方法难以适应这种高度动态的环境。现代应用通常由多个微服务组成，每个微服务可能运行在多个容器实例上，形成庞大的集群，大规模的容器部署增加了管理和监控的复杂度。eBPF作为内核跟踪和网络分析的新兴技术，在容器异常检测领域，eBPF可以为容器提供内核级的安全监控，不仅可以提高监测效率，而且能够从监测对象中挖取更精细的容器运行时特征。相比于现有成熟的基于用户态的异常检测技术，eBPF可以有效降低开销。如何在降低开销的同时，突破eBPF本身在内存等方面的受限条件，针对容器运行时特征设计完成一个基于eBPF的容器异常监测方法仍是一个挑战。

本项目要求参赛者基于eBPF设计并开发一个内核级的容器异常智能检测框架，基于该框架实现如CPU、内存、网络等容器资源指标的提取分析方法，如基于系统调用上下文的时序分析方法，并结合各种异常检测方法，实现基于机器学习的容器运行时异常检测。

## 所属赛道

2025全国大学生操作系统比赛的“OS功能设计”赛道

## 参赛要求

- 以小组为单位参赛，最多三人一个小组，且小组成员是来自同一所高校的学生
- 如学生参加了多个项目，参赛学生选择一个自己参加的项目参与评奖
- 请遵循“2025全国大学生操作系统比赛”的章程和技术方案要求

## 项目导师

- 任怡
- email <renyi@nudt.edu.cn>

## 赛题分类

- AI应用
- 安全应用

## 难度

高

## 题目要求

#### 基础功能

1. 设计并开发一个针对容器运行时数据的采集框架（如系统调用、容器各项资源指标、网络监控数据），数据类型不限，但要求基于eBPF在内核处理跟踪点数据。
2. 设计并实现容器异常行为的自动检测算法，包括不限于基于规则的算法、基于统计的算法和基于机器学习的算法。
3. 利用grafana、Prometheus等工具进行数据异常展示，形成分析报告。

#### 扩展功能

1. 采集框架具有使用不同类型数据采集工具的能力，可集成多种用户态采集工具供选择，并支持各类工具的性能比较。
2. 系统具备自我调整能力，能根据实际环境动态调整其异常检测过程，以达到最优检测效果。

## License

 [GPL-2.0](https://opensource.org/licenses/GPL-2.0)

## 预期目标

完成基础功能和扩展功能的开发，提交相应代码，并输出分析说明类文档。

## 参考资料

[1]eBPF. https://ebpf.io/
[2]bpf performance tools. https://github.com/iovisor/bcc
[3]BPF reference guide. https://docs.cilium.io/en/stable/bpf/
[4]Falco. https://falco.org/docs/getting-started/
[5]Zou Z, Xie Y, Huang K, et al. A docker container anomaly monitoring system based on optimized isolation forest[J]. IEEE Transactions on Cloud Computing, 2019, 10(1): 134-145.
[6]Zhang J, Chen P, He Z, et al. Real-Time Intrusion Detection and Prevention with Neural Network in Kernel Using eBPF[C]//2024 54th Annual IEEE/IFIP International Conference on Dependable Systems and Networks (DSN). IEEE, 2024: 416-428.
