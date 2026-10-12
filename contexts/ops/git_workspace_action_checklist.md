# 宸ヤ綔鍖?Git 琛屽姩娓呭崟锛坕nfra + 椤圭洰鎷嗗垎锛?
> 鑳屾櫙锛?026-10-12 璧?`adhoc_jobs/ai_yh` 涓哄祵濂楃嫭绔嬩粨锛岃繙绋?[thunderderder/dxz](https://github.com/thunderderder/dxz)锛屽垎鏀?`mvp-sep2026`锛涙牴浠?`context-infrastructure` 涓嶅啀璺熻釜璇ョ洰褰曘€? 
> 鏈枃鏄?*浣犺浜叉墜鍋氱殑姝ラ**锛涚姸鎬佷互浣犳墽琛屽墠鏈湴 `git status` 涓哄噯銆?
---

## 鍦板浘锛氫袱涓?git锛屼竴涓枃浠跺す

骞虫椂浠嶅彧鎵撳紑 `D:\code_project\context-infrastructure`锛屼絾 **commit / push 瑕佺湅浣犲湪鍝釜鐩綍寮€缁堢**銆?
| 浣犲湪鍋氫粈涔?| 鏈湴璺緞 | GitHub 浠撳簱 | 棰戠巼 |
|------------|----------|-------------|------|
| 涓滃皬鏅猴紙浠ｇ爜銆侀儴缃层€乣docs/working.md`锛?| `adhoc_jobs\ai_yh\` | [thunderderder/dxz](https://github.com/thunderderder/dxz) | 缁忓父 push |
| Skill銆乄ORKSPACE銆丱BSERVATIONS銆乭eartbeat | 浠撳簱**鏍圭洰褰?* | [thunderderder/context-infrastructure](https://github.com/thunderderder/context-infrastructure) | 鍔?skill 鏃?push |
| 鍏朵粬鐙珛浠撻」鐩紙count_yolo銆乤gent-qa鈥︼級 | `adhoc_jobs\<椤圭洰>\` | 瑙?`rules/WORKSPACE.md` 瀵瑰簲琛?| 鍋氳椤圭洰鏃?|

**骞冲彴**锛氭彁浜ゅ湪鏈湴锛圥owerShell / Cursor 缁堢锛夛紱**GitHub 缃戦〉**鐢ㄦ潵纭 push 鎴愬姛銆佺湅 diff锛屼笉蹇呭湪缃戦〉涓婃棩甯告彁浜ゃ€?
**鍐欐竻鍗曟椂鏈湴蹇収锛堜緵瀵圭収锛?*

- `adhoc_jobs/ai_yh`锛氬垎鏀?`mvp-sep2026`锛屽凡鏈夋湰鍦版彁浜わ紝**灏氭湭** `git push` / 鏈 upstream銆?- 鏍逛粨锛氬垎鏀?`ai_yh/mvp-sep2026`锛?*宸叉殏瀛?*浠庣储寮曠Щ闄?`adhoc_jobs/ai_yh`锛堢害 80 鏂囦欢锛夛紱`rules/WORKSPACE.md` 宸叉敼銆侀渶 `git add` 鍚庝笌涓婁竴骞舵彁浜わ紱鍙︽湁澶ч噺鍏朵粬鏈彁浜ゆ敼鍔紙YH銆乽va 绛夛級鈥斺€?*涓嶈涓€娆℃€у叏鎻愪氦**銆?
---

## 闃舵 A锛氫笢灏忔櫤鎺ㄥ埌 GitHub锛堥」鐩富鎴樺満锛?
**鐩綍**锛歚cd D:\code_project\context-infrastructure\adhoc_jobs\ai_yh`  
**杩滅▼**锛欸itHub `thunderderder/dxz`

- [ ] **A1** `git status` 鈫?搴旀樉绀?`## mvp-sep2026`锛屽綋鍓嶈矾寰勫湪 `...\adhoc_jobs\ai_yh`銆?- [ ] **A2**锛堝彲閫夛級`git fetch origin`锛屽姣旀湰鏈轰笌杩滅▼锛? 
  `git log --oneline -3`  
  `git log origin/mvp-sep2026 --oneline -3`  
  杩滅▼澶氫负杈冩棭浜ゆ帴蹇収锛屼笌鏈満**鍙兘涓嶆槸鍚屼竴鏉″巻鍙?*锛屽睘姝ｅ父銆?- [ ] **A3** 浠ユ湰鏈轰负鍑嗭紙鎺ㄨ崘锛夛細

  ```powershell
  git push -u origin mvp-sep2026 --force-with-lease
  ```

  鑻ュ繀椤讳繚鐣欒繙绋嬫棫鎻愪氦锛氬厛 `git merge origin/mvp-sep2026 --allow-unrelated-histories`锛岃В鍐茬獊鍚庡啀 `git push -u origin mvp-sep2026`銆?
- [ ] **A4** 娴忚鍣ㄦ墦寮€ [dxz / mvp-sep2026](https://github.com/thunderderder/dxz/tree/mvp-sep2026)锛岀‘璁ゆ渶鏂?commit銆?
**浠ュ悗**锛氫笢灏忔櫤鍙湪姝ょ洰褰?`git add` / `commit` / `push`锛屼笉瑕佸湪鏍圭洰褰曟彁浜?`adhoc_jobs/ai_yh` 鍐呮枃浠躲€?
---

## 闃舵 B锛氭牴浠撶櫥璁般€屼笉鍐嶈窡韪?ai_yh銆嶏紙infra锛?
**鐩綍**锛歚cd D:\code_project\context-infrastructure`  
**杩滅▼**锛欸itHub `thunderderder/context-infrastructure`

- [ ] **B1** `git diff --cached --stat` 鈫?搴斾富瑕佹槸 `adhoc_jobs/ai_yh/` 鍒犻櫎锛岀害 80 鏂囦欢锛?*涓嶆槸**涓婂崈鏂囦欢銆?- [ ] **B2** `git add rules/WORKSPACE.md`
- [ ] **B3** 鍙彁浜よ劚閽?+ 璺敱锛堝嬁甯︿笂 YH/uva 绛夊叾瀹冩敼鍔級锛?
  ```powershell
  git commit -m "chore: stop tracking adhoc_jobs/ai_yh (nested dxz repo)"
  ```

- [ ] **B4** Push锛堝綋鍓嶅湪 `ai_yh/mvp-sep2026` 涓婂彲鍏堟帹杩欐潯鍒嗘敮锛夛細

  ```powershell
  git push origin ai_yh/mvp-sep2026
  ```

  闀胯繙鍙妸璇?commit cherry-pick 鍒?`main`锛屾牴浠撴棩甯告敼鐢?`main` 鍔?skill锛堣闃舵 C锛夈€?
- [ ] **B5** 鍦?GitHub 鎵撳紑 context-infrastructure锛岀‘璁ゆ湰娆?commit **鏈?*璇甫 `adhoc_jobs/YH` 绛夊ぇ娈甸」鐩?diff銆?
---

## 闃舵 C锛氭牴浠撳垎鏀範鎯紙涓嶆€ワ級

- [ ] **C1** 鏍逛粨鍒嗘敮鍚?`ai_yh/mvp-sep2026` 鈮?椤圭洰浠?`adhoc_jobs\ai_yh` 閲岀殑 `mvp-sep2026`锛涢」鐩?git 鍦?`adhoc_jobs\ai_yh\.git`銆?- [ ] **C2**锛堝彲閫夛級`git checkout main`锛宍git pull origin main`锛屾洿鏂版湰鍦?infra 涓荤嚎銆?- [ ] **C3**锛堝彲閫夛級灏嗛樁娈?B 鐨?commit cherry-pick 鍒?`main`锛屼互鍚庢牴鐩綍鍦?`main` 涓婃敼 skill銆?- [ ] **C4**锛堝彲閫夛級鍒犻櫎鏃犵敤鏈湴鍒嗘敮 `dxz-subtree-split`銆乣dxz-mvp-sep2026`锛堝湪 A3 纭 dxz 杩滅▼浠ユ湰鏈轰负鍑嗗悗锛夈€?
**鍙拷鐣?*锛歚remotes/upstream-ci/*` 涓轰笂娓?grapeot 闀滃儚锛岄櫎闈炰富鍔ㄥ悎涓婃父 infra銆?
---

## 闃舵 D锛氭棩甯稿垎宸?
| 鍦烘櫙 | 鏈湴 | 杩滅▼ |
|------|------|------|
| 涓滃皬鏅哄紑鍙?/ 閮ㄧ讲 | `adhoc_jobs\ai_yh` | `thunderderder/dxz` |
| 鍔?skill銆乭eartbeat銆丱BSERVATIONS | 浠撳簱鏍?| `thunderderder/context-infrastructure` |
| ECS 閮ㄧ讲 | 椤圭洰鍐?`deploy\pack_deploy.ps1` | 瀵嗛挜锛歚%USERPROFILE%\.ssh\context_deploy_ecs.pem` 鎴栨牴鐩綍 `rules\skills\deploy.pem` |

Cursor 鍙户缁墦寮€鏁翠釜 `context-infrastructure`锛?*鐗堟湰璁板綍**鎸変笂琛ㄥ垎浠撴彁浜ゃ€?
---

## 闃舵 E锛氭殏涓嶅鐞?
- [ ] 鏍逛粨鍏朵綑 1000+ 鏉℃湭鎻愪氦鏀瑰姩锛堝綊妗ｃ€乊H銆乽va鈥︼級鈥斺€斿崟鐙垎鎵规暣鐞嗐€?- [ ] `uva`銆乣YH` 绛夋媶鎴愬祵濂楃嫭绔嬩粨鈥斺€旀寜闇€鍐嶅仛銆?- [ ] 鍒犻櫎鏈湴 `adhoc_jobs\ai_yh\voice\_nested_git_backup_20261012`锛堜粎澶囦唤锛屽垹涓嶅奖鍝?git锛夈€?
---

## 浠婂ぉ 15 鍒嗛挓鏈€灏忚矾寰?
1. `cd adhoc_jobs\ai_yh` 鈫?`git push -u origin mvp-sep2026 --force-with-lease`锛?*dxz**锛?2. `cd` 鍒版牴鐩綍 鈫?`git add rules/WORKSPACE.md` 鈫?`git commit -m "chore: stop tracking adhoc_jobs/ai_yh (nested dxz repo)"` 鈫?`git push origin ai_yh/mvp-sep2026`锛?*context-infrastructure**锛?
---

## 鐩稿叧

- 鐩綍璺敱锛歚rules/WORKSPACE.md`锛堜笢灏忔櫤涓€琛屽惈 dxz 杩滅▼锛?- 椤圭洰灞€閮ㄨ鍒欙細`adhoc_jobs/ai_yh/AGENTS.md`锛圙it 涓?infra 寮辫€﹀悎璇存槑锛?- 宓屽浠撹剼鎵嬫灦锛歚rules/skills/project_scaffold.md`銆乣rules/skills/overlay/project_scaffold_local.md`
