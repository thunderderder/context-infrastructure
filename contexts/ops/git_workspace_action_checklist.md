# 工作区 Git 行动清单（infra + 项目拆分）

> 背景：2026-10-12 起 `adhoc_jobs/ai_yh` 为嵌套独立仓，远程 [thunderderder/dxz](https://github.com/thunderderder/dxz)，分支 `mvp-sep2026`；根仓 `context-infrastructure` 不再跟踪该目录。  
> 本文是**你要亲手做的步骤**；状态以你执行前本地 `git status` 为准。

---

## 地图：两个 git，一个文件夹

平时仍只打开 `D:\code_project\context-infrastructure`，但 **commit / push 要看你在哪个目录开终端**。

| 你在做什么 | 本地路径 | GitHub 仓库 | 频率 |
|------------|----------|-------------|------|
| 东小智（代码、部署、`docs/working.md`） | `adhoc_jobs\ai_yh\` | [thunderderder/dxz](https://github.com/thunderderder/dxz) | 经常 push |
| Skill、WORKSPACE、OBSERVATIONS、heartbeat | 仓库**根目录** | [thunderderder/context-infrastructure](https://github.com/thunderderder/context-infrastructure) | 加 skill 时 push |
| 其他独立仓项目（count_yolo、agent-qa…） | `adhoc_jobs\<项目>\` | 见 `rules/WORKSPACE.md` 对应行 | 做该项目时 |

**平台**：提交在本地（PowerShell / Cursor 终端）；**GitHub 网页**用来确认 push 成功、看 diff，不必在网页上日常提交。

**写清单时本地快照（供对照）**

- `adhoc_jobs/ai_yh`：分支 `mvp-sep2026`，已有本地提交，**尚未** `git push` / 未设 upstream。
- 根仓：分支 `ai_yh/mvp-sep2026`；**已暂存**从索引移除 `adhoc_jobs/ai_yh`（约 80 文件）；`rules/WORKSPACE.md` 已改、需 `git add` 后与上一并提交；另有大量其他未提交改动（YH、uva 等）——**不要一次性全提交**。

---

## 阶段 A：东小智推到 GitHub（项目主战场）

**目录**：`cd D:\code_project\context-infrastructure\adhoc_jobs\ai_yh`  
**远程**：GitHub `thunderderder/dxz`

- [ ] **A1** `git status` → 应显示 `## mvp-sep2026`，当前路径在 `...\adhoc_jobs\ai_yh`。
- [ ] **A2**（可选）`git fetch origin`，对比本机与远程：  
  `git log --oneline -3`  
  `git log origin/mvp-sep2026 --oneline -3`  
  远程多为较早交接快照，与本机**可能不是同一条历史**，属正常。
- [ ] **A3** 以本机为准（推荐）：

  ```powershell
  git push -u origin mvp-sep2026 --force-with-lease
  ```

  若必须保留远程旧提交：先 `git merge origin/mvp-sep2026 --allow-unrelated-histories`，解冲突后再 `git push -u origin mvp-sep2026`。

- [ ] **A4** 浏览器打开 [dxz / mvp-sep2026](https://github.com/thunderderder/dxz/tree/mvp-sep2026)，确认最新 commit。

**以后**：东小智只在此目录 `git add` / `commit` / `push`，不要在根目录提交 `adhoc_jobs/ai_yh` 内文件。

---

## 阶段 B：根仓登记「不再跟踪 ai_yh」（infra）

**目录**：`cd D:\code_project\context-infrastructure`  
**远程**：GitHub `thunderderder/context-infrastructure`

- [ ] **B1** `git diff --cached --stat` → 应主要是 `adhoc_jobs/ai_yh/` 删除，约 80 文件，**不是**上千文件。
- [ ] **B2** `git add rules/WORKSPACE.md`
- [ ] **B3** 只提交脱钩 + 路由（勿带上 YH/uva 等其它改动）：

  ```powershell
  git commit -m "chore: stop tracking adhoc_jobs/ai_yh (nested dxz repo)"
  ```

- [ ] **B4** Push（当前在 `ai_yh/mvp-sep2026` 上可先推这条分支）：

  ```powershell
  git push origin ai_yh/mvp-sep2026
  ```

  长远可把该 commit cherry-pick 到 `main`，根仓日常改用 `main` 加 skill（见阶段 C）。

- [ ] **B5** 在 GitHub 打开 context-infrastructure，确认本次 commit **未**误带 `adhoc_jobs/YH` 等大段项目 diff。

---

## 阶段 C：根仓分支习惯（不急）

- [ ] **C1** 根仓分支名 `ai_yh/mvp-sep2026` ≠ 项目仓 `adhoc_jobs\ai_yh` 里的 `mvp-sep2026`；项目 git 在 `adhoc_jobs\ai_yh\.git`。
- [ ] **C2**（可选）`git checkout main`，`git pull origin main`，更新本地 infra 主线。
- [ ] **C3**（可选）将阶段 B 的 commit cherry-pick 到 `main`，以后根目录在 `main` 上改 skill。
- [ ] **C4**（可选）删除无用本地分支 `dxz-subtree-split`、`dxz-mvp-sep2026`（在 A3 确认 dxz 远程以本机为准后）。

**可忽略**：`remotes/upstream-ci/*` 为上游 grapeot 镜像，除非主动合上游 infra。

---

## 阶段 D：日常分工

| 场景 | 本地 | 远程 |
|------|------|------|
| 东小智开发 / 部署 | `adhoc_jobs\ai_yh` | `thunderderder/dxz` |
| 加 skill、heartbeat、OBSERVATIONS | 仓库根 | `thunderderder/context-infrastructure` |
| ECS 部署 | 项目内 `deploy\pack_deploy.ps1` | 密钥：`%USERPROFILE%\.ssh\context_deploy_ecs.pem` 或根目录 `rules\skills\deploy.pem` |

Cursor 可继续打开整个 `context-infrastructure`；**版本记录**按上表分仓提交。

---

## 阶段 E：暂不处理

- [ ] 根仓其余 1000+ 条未提交改动（归档、YH、uva…）——单独分批整理。
- [ ] `uva`、`YH` 等拆成嵌套独立仓——按需再做。
- [ ] 删除本地 `adhoc_jobs\ai_yh\voice\_nested_git_backup_20261012`（仅备份，删不影响 git）。

---

## 今天 15 分钟最小路径

1. `cd adhoc_jobs\ai_yh` → `git push -u origin mvp-sep2026 --force-with-lease`（**dxz**）
2. `cd` 到根目录 → `git add rules/WORKSPACE.md` → `git commit -m "chore: stop tracking adhoc_jobs/ai_yh (nested dxz repo)"` → `git push origin ai_yh/mvp-sep2026`（**context-infrastructure**）

---

## 相关

- 目录路由：`rules/WORKSPACE.md`（东小智一行含 dxz 远程）
- 项目局部规则：`adhoc_jobs/ai_yh/AGENTS.md`（Git 与 infra 弱耦合说明）
- 嵌套仓脚手架：`rules/skills/project_scaffold.md`、`rules/skills/overlay/project_scaffold_local.md`
