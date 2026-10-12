# WORKSPACE.md - 目录路由速查

目标：让 AI 每轮 session 都能快速知道"去哪里找/放什么"。**找任何文件前先查这里。**

## 路由规则

### 项目与代码

- 写代码 / 跑脚本 / 一次性项目：`adhoc_jobs/<project>/`
- 结项归档：`archive_jobs/<project>/`（状态 archived；hibernating 仍留在 `adhoc_jobs/`）
- 工具脚本（邮件、语义搜索、分享报告、docx / pptx 内容修改等）：`tools/`（**MD→Word 导出标准**：`tools/convert_to_word.py`，skill → `rules/skills/workflow_md_to_word_export.md`；Word 母版改写：`tools/docx/manifest/`，skill → `rules/skills/workflow_docx_reference_manifest.md`；PPTX：`tools/pptx_skill/`；Playwright E2E：`tools/playwright_test_skill/`，skill → `rules/skills/workflow_playwright_test.md`；Voice Memos intake（macOS）：`tools/intake_skill/`，skill → `rules/skills/workflow_intake_skill.md`）
- 定时任务：`periodic_jobs/`

### 知识与记录

- 通用调研报告：`contexts/survey_sessions/`
- 思考 / 复盘 / 方法论：`contexts/thought_review/`
- 每日日志：`contexts/daily_records/`（Syncthing 收件 `inbox/`、管线产出 `processed/`；见 `adhoc_jobs/meeting_intake/AGENTS.md`）
- 健身计划 / 训记训练缓存：`contexts/fitness/`（API 缓存 `.cache/` 不入库；skill → `rules/skills/xunji_trains_api.md`）
- 健康管理（体检、健身近况）：`adhoc_jobs/health_management/`（总览 `健康管理总览.md`；体检 `体检报告/`；门诊检查 `检查报告/`；训记摘要 `健身/xunji_recent.md`）
- 婚礼发言准备：`contexts/wedding_speech/`（回忆清单即素材；定稿 `speech.md`；写法 → `rules/skills/bestpractice_short_speech_irony.md`）
- 正式对外报告：`contexts/reports/`
- 项目 × API / 密钥末四位台账：`contexts/ops/api_registry.md`（对账单、轮换 key、给项目接模型时先查；完整 sk- 不进此文件）
- 工作区 Git / infra 与项目拆分行动清单：`contexts/ops/git_workspace_action_checklist.md`（双仓 push、ai_yh→dxz）

### 系统与规则

- Public Skill（通用）：`rules/skills/` + `overlay/`
- Work Skill（工作绑定）：`rules/work-skills/`（deploy / writing / experience / process / ims）；IMS 入口 `rules/work-skills/ims/INDEX.md`；团队技能执行约定 `rules/work-skills/ims/team/配置IMS系统/00-通用技能约定.md`
- 归类与迁移：`rules/skills/workflow_skill_organization.md`
- 核心公理（Axioms）：`rules/axioms/`
- 记忆系统：`contexts/memory/` + `periodic_jobs/ai_heartbeat/`
- AI Heartbeat 路径：`D:/code_project/context-infrastructure/periodic_jobs/ai_heartbeat/`

## 命名规则

- 目录和文件名：小写 + 下划线 (snake\_case)
- 临时一次性项目：`tmp_<name>/`

## Python 环境

- 根目录 `.venv/` 为工作区级环境（**CPU** torch），用 `uv pip install` 管理依赖
- GPU 推理 / 生图：共用 `D:\AI\envs\cuda`（`python.exe` 在 `Scripts\`），约定 → [`skills/overlay/cuda_env_local.md`](skills/overlay/cuda_env_local.md)。不要为每个项目再装一份 CUDA torch
- 需要隔离时在 `adhoc_jobs/<project>/.venv/`、`tools/pptx_skill/.venv/` 或 `tools/playwright_test_skill/.venv/` 建独立环境（uva 已有独立 CUDA venv，勿与共享环境混装）

## 快速查询

以下 **`### Heartbeat：trace 白名单`** 小节由 `periodic_jobs/ai_heartbeat/src/v0/workspace_trace_projects.py` 解析，**勿改该三级标题文字**。增删「写 `.trace.md` + OBSERVATIONS 摘要指针对象」时只改下列**路径行**（`- adhoc_jobs/...` 形式）；上方「快速查询」叙述行里的 `(trace)` 仅作视觉提示，**以本节路径列表为唯一权威**，避免双源漂移。

### Heartbeat：trace 白名单

- adhoc_jobs/ai_yh
- adhoc_jobs/uva
- adhoc_jobs/publications
- adhoc_jobs/about_me

<!-- 活跃项目（人类可读路由，与上表 trace 路径应对齐） -->

<!-- 格式：- `project-name` → `adhoc_jobs/project_name/` (说明) -->

- `永湖机电设备AI问答实践1-用ims团队工作流生成` → `adhoc_jobs/rag_ai_yh`（hibernating, 正在等待业主反馈）
- `永湖机电设备AI问答实践2-自我实践生成` → `adhoc_jobs/ai_yh`（**独立 git** `github.com/thunderderder/dxz`，分支 `mvp-sep2026` **归档/CSV 线**；主战场见 `adhoc_jobs/YH` → `yh-ims-mcp`）（hibernating）(trace)
- `鸿蒙合作协议` → `adhoc_jobs/temp_xieyi/`（hibernating）
- `无人机机器视觉` → `adhoc_jobs/uva/`（activate, important）(trace)
- `简历生成` → `adhoc_jobs/resume_generation/`（hibernating）
- `机器人学习` → `adhoc_jobs/xlerobot/`（hibernating）
- `AI严肃写作桌面客户端` → `adhoc_jobs/AI-Serious-Writer/`（hibernating）
- `个人主页`  → `adhoc_jobs/about_me/`（进度汇总：`adhoc_jobs/about_me/DEVELOPMENT_PROGRESS.md`）（activate, general）(trace)
- `InsightFace 人脸 1:1 Web MVP` → `adhoc_jobs/temp_face/`（推荐 GPU：`run_app_uva_venv.ps1` 用 `uva/.venv`）（hibernating）
- `项目成果发表` → `adhoc_jobs/publications`（activate, important：`patent_application`,`thesis` ）(trace)
-`常德市招标信息爬取`  → `adhoc_jobs/temp_changde`
- `实时语音识别与摘要` → `adhoc_jobs/brainwave/`（activate, 与 ai_yh 共用 DashScope ASR 底座）
- `会议录音 Syncthing 投递` → `adhoc_jobs/meeting_intake/`（activate, → `contexts/daily_records/inbox/`；入口 `AGENTS.md`）
- `河湖长信箱系统` → `adhoc_jobs/river-mail/`（activate, 在线咨询 + IMS 表单外链）
- `IMS 自然语言问答 Agent` → `adhoc_jobs/agent-qa/`（activate, DuckDB+DeepSeek, IMS 数据访问双轨之通用 NLI 端；源仓 Gitee `zjyits/ims-system-qa-agent`，认证 → [`skills/overlay/gitee_local.md`](skills/overlay/gitee_local.md)）
- `永湖 IMS 系统问答（hop / MCP 主战场）` → `adhoc_jobs/YH/`（**独立 git** `github.com/thunderderder/dxz`，分支 **`yh-ims-mcp`**；`src/yh_qa` + `static/index.html`，http://127.0.0.1:8765/ ；评测 `scripts/eval_suite.py` / `scripts/test_hops.py`；`开发策略与计划.md`、`开发原则.md`、`AGENTS.md`）（activate, important）
- `永湖 IMS 攻防演练脱敏` → `adhoc_jobs/yh_ims_desensitize/`（activate, 词表 2026-09-02 定稿；入口 `阶段总结.md`；行数据 `raw/`+`review/`+`findings/` 含 PII 不入库）
- `Qwen3 本地模型评测` → `adhoc_jobs/temp_local_llm_test/`（activate, Chat UI + 速度/显存指标）
- `设备供应商调研` → `adhoc_jobs/temp_harmony/`（hibernating）
- `城市更新资金策划业务` → `adhoc_jobs/城市更新/`（activate, 深规院交流验证定位 + 资金策划四步漏斗评估；工作指南/问题清单见目录内）
- `YOLO 交通流量自动统计` → `adhoc_jobs/count_yolo/`（activate, 公开框架仓 `github.com/thunderderder/count-yolo`（发布边界由 `tests/test_publishable.py` 守；真实路口数据不进公开仓）；分层验收 L1→L2→L3）
- `资金策划样板/PPT 生成` → `adhoc_jobs/ppt-gen/`（activate, 通用金样板 `deck_golden.pptx` + `build_deck_golden.py`；院模板源 `资金策划业务有关情况 v2.pptx`）
- `部门流程知识沉淀` → `adhoc_jobs/部门流程/`（activate, 散落口述经验沉淀为文档：邀标流程等，2026-08-16 起）
- `安之眼三方合作（AR 眼镜 + 视频 AI）` → `adhoc_jobs/安之眼/`（activate, 水务技术 × 安之眼 Demo 方案我院参与：`汇报_安之眼合作参与建议.md` 内部、`三方分工建议稿.md` 对外；东深智水市场对照 → `contexts/survey_sessions/dongshen_zhishui_survey_20260831.md`）
- `排水管线涉河报批方案（参考样例改编）` → `adhoc_jobs/排水管线过河方案/`（activate, 石化大道涉河方案：docx 参考改编管线交付闭环，skill → `rules/skills/workflow_docx_reference_manifest.md`）
- `格式类文本写作再思考` → `adhoc_jobs/rethinking/`（activate, 主报告 `contexts/survey_sessions/formatted_writing_platform_survey_20260912.md`；对照 AI-Serious-Writer 与排水管线过河方案）
- `格式类文本写作平台调研` → `adhoc_jobs/format_writing_research/`（activate, 并行分维草稿；以 rethinking 主报告为准）
- `赣州发改技术审查` → `adhoc_jobs/赣州/`（activate, 市发改委委托评估/中介超市入口 + 政策性资金申报咨询对照；领导汇报 `汇报_发改技术审查.md`；资金策划咨询样本整理 `调研结果（资金策划咨询）.md`；城市更新对外材料仍在 `adhoc_jobs/城市更新/赣州汇报/`）
- `换源搜索 bookmarklet` → `adhoc_jobs/search_hop_bookmarklet/`（activate, Chrome 书签：当前搜索词跳到 Google/知乎/B站/DeepSeek/豆包/百度/公众号/DDG/YouTube/小红书）
- `小日子行程手册` → `adhoc_jobs/xiaorizi_trip/`（activate, 实例部署仓；私人 git `github.com/thunderderder/xiaorizi-trip`；数据母版 `adhoc_jobs/trip-handbook/trips/xiaorizi/trip.json`）
- `行程手册框架 trip-handbook` → `adhoc_jobs/trip-handbook/`（activate, 公开仓 `github.com/thunderderder/trip-handbook`；AI 入口 `AGENTS.md`；私人实例数据在各自 repo，如 `xiaorizi-trip`）
- `OpenCode 手机远程` → `adhoc_jobs/opencode_mobile_remote/`（activate, 子域 `opencode.thunderder.top`；frp 隧道 + Android 客户端连单位笔记本 `opencode serve`；入口 `README.md`）

<!-- 已归档（结项，不再当活跃项目扫；路径仍可路由） -->

- `深中通道etc数据分析` → `archive_jobs/深中通道etc数据分析/`（archived, 入口 `阶段总结.md`；方法论 `rules/skills/bestpractice_data_analysis_pipeline.md`）
- `鸿蒙内部分享` → `archive_jobs/harmony/`（archived, 入口 `阶段总结.md`；AI vs 终版对比 `review_final/AI_vs_终版对比总结.md`）
