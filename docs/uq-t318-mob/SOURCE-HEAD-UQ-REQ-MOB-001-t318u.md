# 文首来源节改写稿 · UQ-REQ-MOB-001 园擎易办需求大纲

```yaml
稿别: 文首改写稿（待贴回大纲，未并入正本）
适用: UQ-REQ-MOB-001 v0.1
日期: 2026-10-26
时区: Asia/Shanghai
对照结论: 仍未通过
终稿: 否
证据: ./RESULT-RECONCILE-GO-t318u.md
```

本稿只替换文首。不收录需求正文。精选包已经读过，结论仍是未通过，SHA 仍空。不要把本稿贴成对照完成稿。

## 建议替换的状态块

```yaml
编号: UQ-REQ-MOB-001
版本: v0.1
状态: 待重对照
对照结论: 仍未通过
终稿: 否
品牌: zslink
产品: 园擎
项目: UniquePark
端: 园擎易办（UniquePark Go）
```

## 建议新增的「来源」节

### 来源

| 项 | 内容 |
| --- | --- |
| 文档参考仓 | `ref-docs/zslink-saas-doc`（盒内绝对路径 `/workspace/smartpark/ref-docs/zslink-saas-doc`）。本环境未挂载；阅读载体是精选包 `t318u-mob-reconcile-repack-20261026` |
| 库 / 脚本参考仓 | `ref-docs/zslink-saas-yd`。本环境只有目录树索引，脚本与页面说明未读 |
| 权威快照 SHA | 待填。禁止用代码仓 SHA 或 draft 副本 SHA 填这里 |
| 已读文档日期 | `RND-REQ-002` 本版 2026-05-22（已发布）；`RND-MOD-MC-101/102/104` 2026-06-24；`RND-MOD-MAMC-INDEX` 2026-06-25。日期不是 git SHA |
| 对照范围 | 已读：终端与分期、角色、八项能力、非范围、配套接口 §5。未读：REQ-001、MC-008 正文、IA-002、yd 脚本 |
| 归纳落点 | `UQ-REQ-MOB-001` |
| 对照结论摘要 | 仍未通过。待办、邀约、报修主链路、infra-identity 同向。v1.1 分期与 AUD-011、报修用户角色、预定/缴费/发票/多类申请尚未收口。详见 RESULT GO-E01–GO-E16 |

旧路径与旧权限码只留在 RESULT 证据表，不进入正文当权威。

### 关闭条件

git SHA、实际看过的底座卷与 IA-002、以及 RESULT 里「差异未收口」各项被纳入或写入非范围之后，才可以改结论。关闭前不开 N2，不做效果图，不合 `main`。
