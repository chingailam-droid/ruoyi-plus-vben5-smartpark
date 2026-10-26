# 文首来源节改写稿 · UQ-REQ-MOB-002 园擎易管需求大纲

```yaml
稿别: 文首改写稿（待贴回大纲）
适用: UQ-REQ-MOB-002 v0.1
日期: 2026-10-26
时区: Asia/Shanghai
对照结论: 未通过
终稿: 否
```

本稿只替换该大纲的文首状态和来源节。不收录需求正文。上传稿状态为「可评审草案」，无参考仓路径与快照 SHA。按来源锁定规则标待重对照。

需求大纲与模块纲要在 Screen 区间上可以去重对齐到 67。该对齐是两份上传稿的互核，写进来源节时仍记对照结论未通过。

## 建议替换的状态块

```yaml
编号: UQ-REQ-MOB-002
版本: v0.1
状态: 待重对照
对照结论: 未通过
终稿: 否
品牌: zslink
产品: 园擎
项目: UniquePark
端: 园擎易管（UniquePark Work）
```

上游与互链保持原有 UQ 编号。IA-002、PRD、角色与平台底座的 SHA 待盒内填入来源表。

## 建议新增的「来源」节

放在状态块之后、结论摘要之前。

### 来源

| 项 | 内容 |
| --- | --- |
| 文档参考仓 | `ref-docs/zslink-saas-doc`（盒内）。本环境未挂载 |
| 库 / 脚本参考仓 | `ref-docs/zslink-saas-yd`（若有）。本环境未挂载 |
| 权威快照 SHA | 待填。不用代码仓 SHA，不用 draft 副本 SHA |
| 快照日 | 待填（Asia/Shanghai） |
| 对照范围 | 待填。计划范围：易管现场作业面、公共基础、八项能力、Screen 映射、在线/离线边界、与易办的报修协同、IDENT-01 不阻塞登录。计划范围不是已完成范围 |
| 归纳落点 | `UQ-REQ-MOB-002` |
| 本环境已读 | 任务 uploads 中的本大纲与 `UQ-REF-SOURCE-LOCK`；模块侧见 `UQ-MOD-WORK-001` 的文首改写稿 |
| 对照结论摘要 | 未通过。§4 验收要点不计入对照通过 |

### 直引边界

协同表里的工单状态、巡检规则、告警策略以对照后的 UQ 归纳为准。旧值班手册、旧工单说明、旧 App 路径只记在本表，不进入正文当权威。

### 关闭「待重对照」的条件

权威快照 SHA、实际对照范围、差异摘要、RESULT 更新四项齐备之后，才去掉待重对照。首切片选报修还是访客仍待拍板，来源节不代填。N2、效果图 / Figma、合并 `main` 保持停止。

## 与本目录其他稿的关系

- 互核与建议改写点：[RESULT-RECONCILE-WORK-t318u.md](./RESULT-RECONCILE-WORK-t318u.md)
- 模块文首：[SOURCE-HEAD-UQ-MOD-WORK-001-t318u.md](./SOURCE-HEAD-UQ-MOD-WORK-001-t318u.md)
- 易办配对：[RESULT-RECONCILE-GO-t318u.md](./RESULT-RECONCILE-GO-t318u.md)
- 不可达说明：[GAP-REF-UNREACHABLE-t318u.md](./GAP-REF-UNREACHABLE-t318u.md)
