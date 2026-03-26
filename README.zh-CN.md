# AI Coding Principles

一组 Claude Code Skills，涵盖编码纪律和系统设计知识。

[English](./README.md)

## Skills

### [ai-coding-discipline](./ai-coding-discipline/SKILL.md)

在所有代码编写任务中强制加载的规则，防止常见的 AI 编码反模式。

| # | 规则 | 说明 |
|---|------|------|
| 1 | 禁止静默回退 | 不要用 `??` / `||` 掩盖不应缺失的值 |
| 2 | 禁止业务逻辑中的 catch-all | 错误应自然传播，仅在 API 边界捕获 |
| 3 | 测试必须能发现代码缺陷 | 断言具体的业务结果，而非仅检查"存在" |
| 4 | 禁止硬编码查找表 | 实现真实逻辑，而非匹配测试用例的假实现 |
| 5 | 红绿测试 (TDD) | 修 bug 时先写失败的测试，再修复代码 |
| 6 | 修复时不删调试日志 | 日志保留到人工确认修复有效后再清理 |

### [ddia-principles](./ddia-principles/SKILL.md)

基于 Martin Kleppmann《Designing Data-Intensive Applications》的精炼参考指南。在设计数据库、选择存储引擎、实现复制/分区、处理分布式事务或构建批处理/流处理管道时加载。

| 部分 | 主题 |
|------|------|
| I: 数据系统基础 | 可靠性、可扩展性、可维护性；数据模型与查询语言；存储与检索（B-tree vs LSM-tree、OLTP vs OLAP）；编码与演化 |
| II: 分布式数据 | 复制（单主、多主、无主）；分区（键范围、哈希、复合）；事务与隔离级别；分布式系统的挑战；一致性与共识 |
| III: 派生数据 | 批处理（MapReduce、Spark、Flink）；流处理（Kafka、CDC、事件溯源）；数据集成模式 |

## 安装

```bash
npx skills add luoling8192/ai-coding-principles
```

## 许可证

[MIT](./LICENSE)
