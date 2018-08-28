title: SYLPH 是什么?
---

**SYLPH 是一个用于实时流计算的平台,核心是通过工作流描述构建分布式流计算应用程序。**,SYLPH是一套完整的解决方案，主要包括：

- 开发工具：`webUI`, 定义streamSql或streamETl任务
- 运行时：基于`spark2.x`及`flink1.5+` , 依赖`hdfs`和`yarn`
- pipline插件扩展: `java8`, 按需实现`source`,`transform`,`sink`,由插件商店管理
- 基础运维：在`webUI`完成任务创建后一键部署上线,无需人工部署,整个分布式程序由sylph进行管理
- 运行分析: 在sylph`webUI` 上面即可看到任务运行情况,不再需要打隧道查看yarn任务


## 设计原则

- 利用插件系统分离**配置与实现**
- 奉行『**约定优于配置**』，按照[一套统一的约定]进行应用开发，从开发工具，到目录结构。

## 特性

- 快速完成实时计算任务：StreamSql
- 灵活性: 可以简单自主定制 pipeline节点插件
- 便捷的部署：自动重启，一键上线到yarn
- 简单的运维：日志 监控

## 什么样的场景适合用SYLPH

目前SYLPH的定位主要是`实时etl数据处理能力`及`实时流计算`。基于这两大能力，SYLPH有自己的特定应用场景。主要如下：

- 快速实验流计算
- 管理流计算任务