# INDEX · 实拍证据（t71u）

| 项 | 内容 |
| --- | --- |
| 林令 | **t71u** |
| 模型 | Grok 4.7 |
| 日期 | 2026-10-26（Asia/Shanghai） |
| 环境 | 本地 `http://127.0.0.1:18202`（API `18200`）Plus Admin |
| 账号 | 冒烟 `admin` / 租户 `000000`（只开弹窗/抽屉，**不提交**） |
| 正片 | **52** 条（以拍摄索引表为准） |
| 用途 | 给园区产品经理核对壳层。PNG **不入库**本仓库 |

对照结论见 `观感提炼-实拍对照-t71u.md`。锁色修订稿见 `UQ-UIXI-PC-001-Vben主题风格-t71u修订稿.md`。

---

## 1. 解压路径说明

拍摄索引原文把落盘根写成：

`/workspace/smartpark/local-test-20261027/ui-shots/`

该目录是**拍摄机路径**。本 git 仓库没有这批 PNG，不要在 `apps/` 或主题包里找图。

本刀读到的全量包：

| 项 | 值 |
| --- | --- |
| 上传文件名 | `ui-shots-full.tgz`（附件落盘名 `ui-shots-full_a73c.tgz`） |
| 解压后根 | `ui-shots/` |
| 包内索引 | `ui-shots/INDEX.md`（条目数 52，与下表一致） |
| 解压 PNG | **61** = 正片 52 + 辅帧 9 |
| 辅帧（不计入 52） | `other/00-login-fail.png`、`other/00-login-captcha-waiting.png`、`other/00-after-login-seed.png`、`other/_login-form-crop.png`、`other/_captcha-crop.png`、`other/_captcha_sample.png`、`other/_api-captcha.png`、`system/user-list-seed.png`、`system/role-list-seed.png` |
| 非图 | `ui-shots/INDEX.md`、`_vben-dev.log`、`_targets.txt`、`_captcha_now.txt`；`uq/`、`tenant/` 为空目录 |

并入主题包时：索引用本文件，图片向拍摄机目录或 `ui-shots-full.tgz` 取。不要把 61 张 PNG 抄进业务仓库。

正片路径在下表同时写**包内相对路径**和拍摄机绝对路径。

画面含浏览器铬。个别帧有 Google 翻译气泡，忽略，不是产品 UI。文件 1280×800；抽屉图宽约为 CSS 宽度的 2/3，读宽度档时以修订稿 §4.2 的 class 为准，不要把图宽当成 400px 抽屉。

---

## 2. 按模块统计

| 模块 | 目录 | 正片条数 | 右抽屉 | 居中弹窗 | 无浮层 | 路由缺口帧 |
| --- | --- | --- | --- | --- | --- | --- |
| 分析 / 工作台 | `dashboard/` | 2 | 0 | 0 | 2 | 0 |
| 登录后落地 / 个人中心 | `other/` | 3 | 0 | 0 | 3 | 0 |
| 系统（含租户、OSS） | `system/` | 27 | 9 | 4 | 13 | 1 |
| 监控 | `monitor/` | 6 | 0 | 0 | 4 | 2 |
| 工具 | `tool/` | 2 | 0 | 1 | 1 | 0 |
| 工作流 / 任务 / 请假 | `workflow/` | 12 | 2 | 2 | 7 | 1 |
| **合计** |  | **52** | **11** | **7** | **30** | **4** |

11 + 7 + 30 + 4 = 52。

抽屉 11 条里，租户新增是**骨架加载中**，字段未出全，只能证明「从右滑入」，不能当字段稿。

弹窗 7 条均为居中，没有右贴边的窄 Modal。本批**没有**审批用约 400px Modal。

---

## 3. 抽屉覆盖（11）

| 页面 | 路由 | 包内路径 | 只读宽度类（未改源码） |
| --- | --- | --- | --- |
| 用户 · 新增 | `/system/user` | `system/user-drawer-add.png` | `w-[600px]` |
| 角色 · 新增（含菜单树） | `/system/role` | `system/role-drawer-add.png` | `w-[800px]` |
| 菜单 · 新增 | `/system/menu` | `system/menu-drawer-add.png` | `w-[600px]` |
| 部门 · 新增 | `/system/dept` | `system/dept-drawer-add.png` | `w-[600px]` |
| 岗位 · 新增 | `/system/post` | `system/post-drawer-add.png` | `w-[600px]` |
| 客户端 · 新增 | `/system/client` | `system/client-drawer-add.png` | `w-[600px]` |
| 租户 · 新增（骨架） | `/tenant/tenant` | `system/tenant-drawer-add-loading.png` | `w-[600px]` |
| 租户套餐 · 新增（含菜单树） | `/tenant/tenantPackage` | `system/tenant-package-drawer-add.png` | `w-[800px]` |
| OSS 配置 · 编辑 | `/system/oss-config/index` | `system/oss-config-drawer-edit.png` | `w-[650px]` |
| SpEL · 编辑 | `/workflow/spel` | `workflow/spel-drawer-edit.png` | `w-[600px]` |
| 请假 · 新增（页脚含暂存） | `/demo/leave` | `workflow/leave-drawer-add.png` | `w-[600px]` |

页脚：除请假为「取消 / 暂存 / 确认」外，成片可见的都是「取消 + 确认」。

---

## 4. 弹窗覆盖（7）

| 页面 | 路由 | 包内路径 | 只读宽度（未改源码） |
| --- | --- | --- | --- |
| 字典类型 · 新增 | `/system/dict` | `system/dict-modal-add.png` | 未写宽度类，默认 Modal（`w-130`，约 520px） |
| 参数 · 新增 | `/system/config` | `system/config-modal-add.png` | `w-[550px]` |
| 通知公告 · 新增（富文本） | `/system/notice` | `system/notice-modal-add.png` | `w-[800px]` |
| 文件 · 上传（无页脚） | `/system/oss` | `system/oss-modal-upload.png` | 未写宽度类；`:footer="false"` |
| 代码生成 · 导入表 | `/tool/gen` | `tool/gen-modal-import.png` | `w-[800px]` |
| 流程分类 · 新增 | `/workflow/category` | `workflow/category-modal-add.png` | `min-h-[500px]`，宽为默认 Modal |
| 流程定义 · 新增 | `/workflow/processDefinition` | `workflow/processDefinition-modal-add.png` | `w-[550px]`。钩子是 `useVbenModal`，**画面是居中弹窗** |

---

## 5. 正片全表（52）

拍摄机绝对路径 = `/workspace/smartpark/local-test-20261027/ui-shots/` + 下表「包内路径」。

| 页面名 | 路由 | 浮层 | 包内路径 |
| --- | --- | --- | --- |
| 登录后落地 · 分析页 | `/analytics` | 否 | `other/00-after-login.png` |
| 个人中心 · 基本设置 | `/profile` | 否 | `other/profile.png` |
| 个人中心 · 安全设置 | `/profile` | 否 · 安全设置 tab | `other/profile-security.png` |
| 分析页 | `/analytics` | 否 | `dashboard/analytics.png` |
| 工作台 | `/workspace` | 否 | `dashboard/workspace.png` |
| 用户管理 · 列表 | `/system/user` | 否 | `system/user-list.png` |
| 用户管理 · 新增抽屉 | `/system/user` | 抽屉 | `system/user-drawer-add.png` |
| 角色管理 · 列表 | `/system/role` | 否 | `system/role-list.png` |
| 角色管理 · 新增抽屉 | `/system/role` | 抽屉 | `system/role-drawer-add.png` |
| 菜单管理 · 列表 | `/system/menu` | 否 | `system/menu-list.png` |
| 菜单管理 · 新增抽屉 | `/system/menu` | 抽屉 | `system/menu-drawer-add.png` |
| 部门管理 · 列表 | `/system/dept` | 否 | `system/dept-list.png` |
| 部门管理 · 新增抽屉 | `/system/dept` | 抽屉 | `system/dept-drawer-add.png` |
| 岗位管理 · 列表 | `/system/post` | 否 | `system/post-list.png` |
| 岗位管理 · 新增抽屉 | `/system/post` | 抽屉 | `system/post-drawer-add.png` |
| 字典管理 · 列表 | `/system/dict` | 否 · 左类型右数据 | `system/dict-list.png` |
| 字典管理 · 新增弹窗 | `/system/dict` | 弹窗 | `system/dict-modal-add.png` |
| 参数设置 · 列表 | `/system/config` | 否 | `system/config-list.png` |
| 参数设置 · 新增弹窗 | `/system/config` | 弹窗 | `system/config-modal-add.png` |
| 通知公告 · 列表 | `/system/notice` | 否 | `system/notice-list.png` |
| 通知公告 · 新增弹窗 | `/system/notice` | 弹窗 | `system/notice-modal-add.png` |
| 客户端管理 · 列表 | `/system/client` | 否 | `system/client-list.png` |
| 客户端管理 · 新增抽屉 | `/system/client` | 抽屉 | `system/client-drawer-add.png` |
| 租户 · 错误路由 | `/system/tenant` | 缺口 | `system/tenant-missing.png` |
| 租户管理 · 列表 | `/tenant/tenant` | 否 | `system/tenant-list.png` |
| 租户管理 · 新增抽屉 | `/tenant/tenant` | 抽屉 · 骨架未出字段 | `system/tenant-drawer-add-loading.png` |
| 租户套餐 · 列表 | `/tenant/tenantPackage` | 否 | `system/tenant-package-list.png` |
| 租户套餐 · 新增抽屉 | `/tenant/tenantPackage` | 抽屉 | `system/tenant-package-drawer-add.png` |
| 文件管理 · 列表 | `/system/oss` | 否 | `system/oss-list.png` |
| 文件管理 · 上传弹窗 | `/system/oss` | 弹窗 | `system/oss-modal-upload.png` |
| OSS 配置 · 列表 | `/system/oss-config/index` | 否 | `system/oss-config-list.png` |
| OSS 配置 · 编辑抽屉 | `/system/oss-config/index` | 抽屉 | `system/oss-config-drawer-edit.png` |
| 在线用户 | `/monitor/online` | 否 | `monitor/online.png` |
| 缓存监控 | `/monitor/cache` | 否 | `monitor/cache.png` |
| Admin 监控 | `/monitor/Admin` | 否 · iframe:9090 未加载 | `monitor/admin.png` |
| SnailJob | `/monitor/snailjob` | 否 · iframe:8800 未加载 | `monitor/snailjob.png` |
| 登录日志 | `/monitor/logininfor` | 缺口 · 菜单无此项 | `monitor/logininfor-missing.png` |
| 操作日志 | `/monitor/operlog` | 缺口 · 菜单无此项 | `monitor/operlog-missing.png` |
| 代码生成 · 列表 | `/tool/gen` | 否 | `tool/gen.png` |
| 代码生成 · 导入表弹窗 | `/tool/gen` | 弹窗 | `tool/gen-modal-import.png` |
| 流程分类 · 列表 | `/workflow/category` | 否 | `workflow/category.png` |
| 流程分类 · 新增弹窗 | `/workflow/category` | 弹窗 | `workflow/category-modal-add.png` |
| 流程定义 · 列表 | `/workflow/processDefinition` | 否 · 左树右表 | `workflow/processDefinition.png` |
| 流程定义 · 新增弹窗 | `/workflow/processDefinition` | 弹窗 | `workflow/processDefinition-modal-add.png` |
| 流程实例 | `/workflow/processMonitor/processInstance` | 否 | `workflow/processInstance.png` |
| 全部待办 | `/workflow/processMonitor/allTaskWaiting` | 否 | `workflow/allTaskWaiting.png` |
| 我的待办 | `/task/taskWaiting` | 否 | `workflow/taskWaiting.png` |
| SpEL 列表 | `/workflow/spel` | 否 | `workflow/spel.png` |
| SpEL · 编辑抽屉 | `/workflow/spel` | 抽屉 | `workflow/spel-drawer-edit.png` |
| 请假 · 错误路由 | `/workflow/leave` | 缺口 | `workflow/leave-missing.png` |
| 请假申请 · 列表 | `/demo/leave` | 否 | `workflow/leave.png` |
| 请假申请 · 新增抽屉 | `/demo/leave` | 抽屉 | `workflow/leave-drawer-add.png` |

---

## 6. 路由校正（照抄拍摄 INDEX，并结构化）

原文：

- `/system/tenant` → 正确 **`/tenant/tenant`**；套餐正确 **`/tenant/tenantPackage`**。
- `/system/oss-config` → 正确 **`/system/oss-config/index`**。
- `/workflow/leave` 404 → 请假在 **`/demo/leave`**；`/workflow/processInstance`、`/workflow/task` 404 → 实际 **`/workflow/processMonitor/processInstance`**、**`/task/taskWaiting`** 等。
- 登录日志 / 操作日志：当前菜单无入口，直链 404。
- Admin(9090) / SnailJob(8800) iframe 本地未起（snail-job 已关）。
- 租户「新增」抽屉曾长时间骨架未出字段（有 loading 截图）。
- 未截（可选续）：`/task/myDocument`、`/task/taskFinish`、`/task/taskCopyList`。

| 误开路径 | 结果 | 应使用 | 证据帧 |
| --- | --- | --- | --- |
| `/system/tenant` | 404 | `/tenant/tenant` | `system/tenant-missing.png` · `system/tenant-list.png` |
| （套餐无单独误开帧） | — | `/tenant/tenantPackage` | `system/tenant-package-list.png` |
| `/system/oss-config` | 索引标明需校正 | `/system/oss-config/index` | `system/oss-config-list.png` |
| `/workflow/leave` | 404 | `/demo/leave` | `workflow/leave-missing.png` · `workflow/leave.png` |
| `/workflow/processInstance` | 404 | `/workflow/processMonitor/processInstance` | `workflow/processInstance.png` |
| `/workflow/task` | 404 | `/task/taskWaiting` | `workflow/taskWaiting.png` |
| （全部待办） | 可用 | `/workflow/processMonitor/allTaskWaiting` | `workflow/allTaskWaiting.png` |
| `/monitor/logininfor` | 菜单无入口，404 | 本环境无页 | `monitor/logininfor-missing.png` |
| `/monitor/operlog` | 菜单无入口，404 | 本环境无页 | `monitor/operlog-missing.png` |
| `/monitor/Admin` | 壳在，iframe 空 | 依赖本地 9090 | `monitor/admin.png` |
| `/monitor/snailjob` | 壳在，iframe 空 | 依赖本地 8800（已关） | `monitor/snailjob.png` |

---

## 7. 缺口（照抄并补充主题向缺口）

拍摄索引已列：

- 登录日志、操作日志无菜单。
- Admin / SnailJob iframe 未起。
- 租户新增抽屉骨架未出字段。
- 未截：`/task/myDocument`、`/task/taskFinish`、`/task/taskCopyList`。

主题包还缺这些帧（不在 52 正片目标内，但裁定色板时会用到）：

| 缺口 | 说明 |
| --- | --- |
| 登录成功正片 | 仅有辅帧 `other/00-login-fail.png` 等，不计入 52。够证明字标是 Plus Admin，不够当登录效果图 |
| 字典**数据**抽屉 | 类型弹窗已拍。数据增改的右抽屉未单独成片 |
| 审批 Modal ≈400px | 梯控档。本批无 |
| 校验失败态 | 无必填报红帧 |
| 深色一帧 | 无。正式板默认不要深色 |
| DevTools 读 `--primary` / `--destructive` | 本刀用像素取样，没有在浏览器里读 CSS 变量 |
| 园区 `/uq/site`、`/uq/infra` | 本批是平台壳，没有园区业务页 |

---

## 8. 模块目录（与拍摄索引相同）

- `system/` 系统管理（含租户 / OSS）
- `monitor/` 系统监控
- `tool/` 系统工具
- `workflow/` 工作流 / 任务 / 请假
- `dashboard/` 分析页 / 工作台
- `other/` 登录后落地、个人中心（辅帧另有登录失败与验证码裁切）

分辨率：正片文件多为桌面 1280×800。登录因远端 Redis/MySQL 常需约 15–17s；拍摄时本地曾把 alova timeout 调到 60s 以便截图。该超时**不是**主题的一部分，不要写进效果图说明当成产品行为。

---

## 变更

| 时刻（Asia/Shanghai） | 说明 |
| --- | --- |
| 2026-10-26 | t71u：按 `ui-shots/INDEX.md` 结构化 52 条，统计抽屉 11 / 弹窗 7，路由校正与缺口照抄并列表化。PNG 不入库。 |
