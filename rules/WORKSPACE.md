# WORKSPACE.md - 鐩綍璺敱閫熸煡

鐩爣锛氳 AI 姣忚疆 session 閮借兘蹇€熺煡閬?鍘诲摢閲屾壘/鏀句粈涔?銆?*鎵句换浣曟枃浠跺墠鍏堟煡杩欓噷銆?*

## 璺敱瑙勫垯

### 椤圭洰涓庝唬鐮?
- 鍐欎唬鐮?/ 璺戣剼鏈?/ 涓€娆℃€ч」鐩細`adhoc_jobs/<project>/`
- 缁撻」褰掓。锛歚archive_jobs/<project>/`锛堢姸鎬?archived锛沨ibernating 浠嶇暀鍦?`adhoc_jobs/`锛?- 宸ュ叿鑴氭湰锛堥偖浠躲€佽涔夋悳绱€佸垎浜姤鍛娿€乨ocx / pptx 鍐呭淇敼绛夛級锛歚tools/`锛?*MD鈫扺ord 瀵煎嚭鏍囧噯**锛歚tools/convert_to_word.py`锛宻kill 鈫?`rules/skills/workflow_md_to_word_export.md`锛沇ord 姣嶇増鏀瑰啓锛歚tools/docx/manifest/`锛宻kill 鈫?`rules/skills/workflow_docx_reference_manifest.md`锛汸PTX锛歚tools/pptx_skill/`锛汸laywright E2E锛歚tools/playwright_test_skill/`锛宻kill 鈫?`rules/skills/workflow_playwright_test.md`锛沄oice Memos intake锛坢acOS锛夛細`tools/intake_skill/`锛宻kill 鈫?`rules/skills/workflow_intake_skill.md`锛?- 瀹氭椂浠诲姟锛歚periodic_jobs/`

### 鐭ヨ瘑涓庤褰?
- 閫氱敤璋冪爺鎶ュ憡锛歚contexts/survey_sessions/`
- 鎬濊€?/ 澶嶇洏 / 鏂规硶璁猴細`contexts/thought_review/`
- 姣忔棩鏃ュ織锛歚contexts/daily_records/`锛圫yncthing 鏀朵欢 `inbox/`銆佺绾夸骇鍑?`processed/`锛涜 `adhoc_jobs/meeting_intake/AGENTS.md`锛?- 鍋ヨ韩璁″垝 / 璁璁粌缂撳瓨锛歚contexts/fitness/`锛圓PI 缂撳瓨 `.cache/` 涓嶅叆搴擄紱skill 鈫?`rules/skills/xunji_trains_api.md`锛?- 鍋ュ悍绠＄悊锛堜綋妫€銆佸仴韬繎鍐碉級锛歚adhoc_jobs/health_management/`锛堟€昏 `鍋ュ悍绠＄悊鎬昏.md`锛涗綋妫€ `浣撴鎶ュ憡/`锛涢棬璇婃鏌?`妫€鏌ユ姤鍛?`锛涜璁版憳瑕?`鍋ヨ韩/xunji_recent.md`锛?- 濠氱ぜ鍙戣█鍑嗗锛歚contexts/wedding_speech/`锛堝洖蹇嗘竻鍗曞嵆绱犳潗锛涘畾绋?`speech.md`锛涘啓娉?鈫?`rules/skills/bestpractice_short_speech_irony.md`锛?- 姝ｅ紡瀵瑰鎶ュ憡锛歚contexts/reports/`
- 椤圭洰 脳 API / 瀵嗛挜鏈洓浣嶅彴璐︼細`contexts/ops/api_registry.md`锛堝璐﹀崟銆佽疆鎹?key銆佺粰椤圭洰鎺ユā鍨嬫椂鍏堟煡锛涘畬鏁?sk- 涓嶈繘姝ゆ枃浠讹級
- 宸ヤ綔鍖?Git / infra 涓庨」鐩媶鍒嗚鍔ㄦ竻鍗曪細`contexts/ops/git_workspace_action_checklist.md`锛堝弻浠?push銆乤i_yh鈫抎xz锛?
### 绯荤粺涓庤鍒?
- Public Skill锛堥€氱敤锛夛細`rules/skills/` + `overlay/`
- Work Skill锛堝伐浣滅粦瀹氾級锛歚rules/work-skills/`锛坉eploy / writing / experience / process / ims锛夛紱IMS 鍏ュ彛 `rules/work-skills/ims/INDEX.md`锛涘洟闃熸妧鑳芥墽琛岀害瀹?`rules/work-skills/ims/team/閰嶇疆IMS绯荤粺/00-閫氱敤鎶€鑳界害瀹?md`
- 褰掔被涓庤縼绉伙細`rules/skills/workflow_skill_organization.md`
- 鏍稿績鍏悊锛圓xioms锛夛細`rules/axioms/`
- 璁板繂绯荤粺锛歚contexts/memory/` + `periodic_jobs/ai_heartbeat/`
- AI Heartbeat 璺緞锛歚D:/code_project/context-infrastructure/periodic_jobs/ai_heartbeat/`

## 鍛藉悕瑙勫垯

- 鐩綍鍜屾枃浠跺悕锛氬皬鍐?+ 涓嬪垝绾?(snake\_case)
- 涓存椂涓€娆℃€ч」鐩細`tmp_<name>/`

## Python 鐜

- 鏍圭洰褰?`.venv/` 涓哄伐浣滃尯绾х幆澧冿紙**CPU** torch锛夛紝鐢?`uv pip install` 绠＄悊渚濊禆
- GPU 鎺ㄧ悊 / 鐢熷浘锛氬叡鐢?`D:\AI\envs\cuda`锛坄python.exe` 鍦?`Scripts\`锛夛紝绾﹀畾 鈫?[`skills/overlay/cuda_env_local.md`](skills/overlay/cuda_env_local.md)銆備笉瑕佷负姣忎釜椤圭洰鍐嶈涓€浠?CUDA torch
- 闇€瑕侀殧绂绘椂鍦?`adhoc_jobs/<project>/.venv/`銆乣tools/pptx_skill/.venv/` 鎴?`tools/playwright_test_skill/.venv/` 寤虹嫭绔嬬幆澧冿紙uva 宸叉湁鐙珛 CUDA venv锛屽嬁涓庡叡浜幆澧冩贩瑁咃級

## 蹇€熸煡璇?
浠ヤ笅 **`### Heartbeat锛歵race 鐧藉悕鍗昤** 灏忚妭鐢?`periodic_jobs/ai_heartbeat/src/v0/workspace_trace_projects.py` 瑙ｆ瀽锛?*鍕挎敼璇ヤ笁绾ф爣棰樻枃瀛?*銆傚鍒犮€屽啓 `.trace.md` + OBSERVATIONS 鎽樿鎸囬拡瀵硅薄銆嶆椂鍙敼涓嬪垪**璺緞琛?*锛坄- adhoc_jobs/...` 褰㈠紡锛夛紱涓婃柟銆屽揩閫熸煡璇€嶅彊杩拌閲岀殑 `(trace)` 浠呬綔瑙嗚鎻愮ず锛?*浠ユ湰鑺傝矾寰勫垪琛ㄤ负鍞竴鏉冨▉**锛岄伩鍏嶅弻婧愭紓绉汇€?
### Heartbeat锛歵race 鐧藉悕鍗?
- adhoc_jobs/ai_yh
- adhoc_jobs/uva
- adhoc_jobs/publications
- adhoc_jobs/about_me

<!-- 娲昏穬椤圭洰锛堜汉绫诲彲璇昏矾鐢憋紝涓庝笂琛?trace 璺緞搴斿榻愶級 -->

<!-- 鏍煎紡锛? `project-name` 鈫?`adhoc_jobs/project_name/` (璇存槑) -->

- `姘告箹鏈虹數璁惧AI闂瓟瀹炶返1-鐢╥ms鍥㈤槦宸ヤ綔娴佺敓鎴恅 鈫?`adhoc_jobs/rag_ai_yh`锛坔ibernating, 姝ｅ湪绛夊緟涓氫富鍙嶉锛?- `姘告箹鏈虹數璁惧AI闂瓟瀹炶返2-鑷垜瀹炶返鐢熸垚` 鈫?`adhoc_jobs/ai_yh`锛?*鐙珛 git** `github.com/thunderderder/dxz`锛屽垎鏀?`mvp-sep2026` **褰掓。/CSV 绾?*锛涗富鎴樺満瑙?`adhoc_jobs/YH` 鈫?`yh-ims-mcp`锛夛紙hibernating锛?trace)
- `楦胯挋鍚堜綔鍗忚` 鈫?`adhoc_jobs/temp_xieyi/`锛坔ibernating锛?- `鏃犱汉鏈烘満鍣ㄨ瑙塦 鈫?`adhoc_jobs/uva/`锛坅ctivate, important锛?trace)
- `绠€鍘嗙敓鎴恅 鈫?`adhoc_jobs/resume_generation/`锛坔ibernating锛?- `鏈哄櫒浜哄涔燻 鈫?`adhoc_jobs/xlerobot/`锛坔ibernating锛?- `AI涓ヨ們鍐欎綔妗岄潰瀹㈡埛绔痐 鈫?`adhoc_jobs/AI-Serious-Writer/`锛坔ibernating锛?- `涓汉涓婚〉`  鈫?`adhoc_jobs/about_me/`锛堣繘搴︽眹鎬伙細`adhoc_jobs/about_me/DEVELOPMENT_PROGRESS.md`锛夛紙activate, general锛?trace)
- `InsightFace 浜鸿劯 1:1 Web MVP` 鈫?`adhoc_jobs/temp_face/`锛堟帹鑽?GPU锛歚run_app_uva_venv.ps1` 鐢?`uva/.venv`锛夛紙hibernating锛?- `椤圭洰鎴愭灉鍙戣〃` 鈫?`adhoc_jobs/publications`锛坅ctivate, important锛歚patent_application`,`thesis` 锛?trace)
-`甯稿痉甯傛嫑鏍囦俊鎭埇鍙朻  鈫?`adhoc_jobs/temp_changde`
- `瀹炴椂璇煶璇嗗埆涓庢憳瑕乣 鈫?`adhoc_jobs/brainwave/`锛坅ctivate, 涓?ai_yh 鍏辩敤 DashScope ASR 搴曞骇锛?- `浼氳褰曢煶 Syncthing 鎶曢€抈 鈫?`adhoc_jobs/meeting_intake/`锛坅ctivate, 鈫?`contexts/daily_records/inbox/`锛涘叆鍙?`AGENTS.md`锛?- `娌虫箹闀夸俊绠辩郴缁焋 鈫?`adhoc_jobs/river-mail/`锛坅ctivate, 鍦ㄧ嚎鍜ㄨ + IMS 琛ㄥ崟澶栭摼锛?- `IMS 鑷劧璇█闂瓟 Agent` 鈫?`adhoc_jobs/agent-qa/`锛坅ctivate, DuckDB+DeepSeek, IMS 鏁版嵁璁块棶鍙岃建涔嬮€氱敤 NLI 绔紱婧愪粨 Gitee `zjyits/ims-system-qa-agent`锛岃璇?鈫?[`skills/overlay/gitee_local.md`](skills/overlay/gitee_local.md)锛?- `姘告箹 IMS 绯荤粺闂瓟锛坔op / MCP 涓绘垬鍦猴級` 鈫?`adhoc_jobs/YH/`锛?*鐙珛 git** `github.com/thunderderder/dxz`锛屽垎鏀?**`yh-ims-mcp`**锛沗src/yh_qa` + `static/index.html`锛宧ttp://127.0.0.1:8765/ 锛涜瘎娴?`scripts/eval_suite.py` / `scripts/test_hops.py`锛沗寮€鍙戠瓥鐣ヤ笌璁″垝.md`銆乣寮€鍙戝師鍒?md`銆乣AGENTS.md`锛夛紙activate, important锛?- `姘告箹 IMS 鏀婚槻婕旂粌鑴辨晱` 鈫?`adhoc_jobs/yh_ims_desensitize/`锛坅ctivate, 璇嶈〃 2026-09-02 瀹氱锛涘叆鍙?`闃舵鎬荤粨.md`锛涜鏁版嵁 `raw/`+`review/`+`findings/` 鍚?PII 涓嶅叆搴擄級
- `Qwen3 鏈湴妯″瀷璇勬祴` 鈫?`adhoc_jobs/temp_local_llm_test/`锛坅ctivate, Chat UI + 閫熷害/鏄惧瓨鎸囨爣锛?- `璁惧渚涘簲鍟嗚皟鐮擿 鈫?`adhoc_jobs/temp_harmony/`锛坔ibernating锛?- `鍩庡競鏇存柊璧勯噾绛栧垝涓氬姟` 鈫?`adhoc_jobs/鍩庡競鏇存柊/`锛坅ctivate, 娣辫闄氦娴侀獙璇佸畾浣?+ 璧勯噾绛栧垝鍥涙婕忔枟璇勪及锛涘伐浣滄寚鍗?闂娓呭崟瑙佺洰褰曞唴锛?- `YOLO 浜ら€氭祦閲忚嚜鍔ㄧ粺璁 鈫?`adhoc_jobs/count_yolo/`锛坅ctivate, 鍏紑妗嗘灦浠?`github.com/thunderderder/count-yolo`锛堝彂甯冭竟鐣岀敱 `tests/test_publishable.py` 瀹堬紱鐪熷疄璺彛鏁版嵁涓嶈繘鍏紑浠擄級锛涘垎灞傞獙鏀?L1鈫扡2鈫扡3锛?- `璧勯噾绛栧垝鏍锋澘/PPT 鐢熸垚` 鈫?`adhoc_jobs/ppt-gen/`锛坅ctivate, 閫氱敤閲戞牱鏉?`deck_golden.pptx` + `build_deck_golden.py`锛涢櫌妯℃澘婧?`璧勯噾绛栧垝涓氬姟鏈夊叧鎯呭喌 v2.pptx`锛?- `閮ㄩ棬娴佺▼鐭ヨ瘑娌夋穩` 鈫?`adhoc_jobs/閮ㄩ棬娴佺▼/`锛坅ctivate, 鏁ｈ惤鍙ｈ堪缁忛獙娌夋穩涓烘枃妗ｏ細閭€鏍囨祦绋嬬瓑锛?026-08-16 璧凤級
- `瀹変箣鐪间笁鏂瑰悎浣滐紙AR 鐪奸暅 + 瑙嗛 AI锛塦 鈫?`adhoc_jobs/瀹変箣鐪?`锛坅ctivate, 姘村姟鎶€鏈?脳 瀹変箣鐪?Demo 鏂规鎴戦櫌鍙備笌锛歚姹囨姤_瀹変箣鐪煎悎浣滃弬涓庡缓璁?md` 鍐呴儴銆乣涓夋柟鍒嗗伐寤鸿绋?md` 瀵瑰锛涗笢娣辨櫤姘村競鍦哄鐓?鈫?`contexts/survey_sessions/dongshen_zhishui_survey_20260831.md`锛?- `鎺掓按绠＄嚎娑夋渤鎶ユ壒鏂规锛堝弬鑰冩牱渚嬫敼缂栵級` 鈫?`adhoc_jobs/鎺掓按绠＄嚎杩囨渤鏂规/`锛坅ctivate, 鐭冲寲澶ч亾娑夋渤鏂规锛歞ocx 鍙傝€冩敼缂栫绾夸氦浠橀棴鐜紝skill 鈫?`rules/skills/workflow_docx_reference_manifest.md`锛?- `鏍煎紡绫绘枃鏈啓浣滃啀鎬濊€僠 鈫?`adhoc_jobs/rethinking/`锛坅ctivate, 涓绘姤鍛?`contexts/survey_sessions/formatted_writing_platform_survey_20260912.md`锛涘鐓?AI-Serious-Writer 涓庢帓姘寸绾胯繃娌虫柟妗堬級
- `鏍煎紡绫绘枃鏈啓浣滃钩鍙拌皟鐮擿 鈫?`adhoc_jobs/format_writing_research/`锛坅ctivate, 骞惰鍒嗙淮鑽夌锛涗互 rethinking 涓绘姤鍛婁负鍑嗭級
- `璧ｅ窞鍙戞敼鎶€鏈鏌 鈫?`adhoc_jobs/璧ｅ窞/`锛坅ctivate, 甯傚彂鏀瑰濮旀墭璇勪及/涓粙瓒呭競鍏ュ彛 + 鏀跨瓥鎬ц祫閲戠敵鎶ュ挩璇㈠鐓э紱棰嗗姹囨姤 `姹囨姤_鍙戞敼鎶€鏈鏌?md`锛涜祫閲戠瓥鍒掑挩璇㈡牱鏈暣鐞?`璋冪爺缁撴灉锛堣祫閲戠瓥鍒掑挩璇級.md`锛涘煄甯傛洿鏂板澶栨潗鏂欎粛鍦?`adhoc_jobs/鍩庡競鏇存柊/璧ｅ窞姹囨姤/`锛?- `鎹㈡簮鎼滅储 bookmarklet` 鈫?`adhoc_jobs/search_hop_bookmarklet/`锛坅ctivate, Chrome 涔︾锛氬綋鍓嶆悳绱㈣瘝璺冲埌 Google/鐭ヤ箮/B绔?DeepSeek/璞嗗寘/鐧惧害/鍏紬鍙?DDG/YouTube/灏忕孩涔︼級
- `灏忔棩瀛愯绋嬫墜鍐宍 鈫?`adhoc_jobs/xiaorizi_trip/`锛坅ctivate, 瀹炰緥閮ㄧ讲浠擄紱绉佷汉 git `github.com/thunderderder/xiaorizi-trip`锛涙暟鎹瘝鐗?`adhoc_jobs/trip-handbook/trips/xiaorizi/trip.json`锛?- `琛岀▼鎵嬪唽妗嗘灦 trip-handbook` 鈫?`adhoc_jobs/trip-handbook/`锛坅ctivate, 鍏紑浠?`github.com/thunderderder/trip-handbook`锛汚I 鍏ュ彛 `AGENTS.md`锛涚浜哄疄渚嬫暟鎹湪鍚勮嚜 repo锛屽 `xiaorizi-trip`锛?- `OpenCode 鎵嬫満杩滅▼` 鈫?`adhoc_jobs/opencode_mobile_remote/`锛坅ctivate, 瀛愬煙 `opencode.thunderder.top`锛沠rp 闅ч亾 + Android 瀹㈡埛绔繛鍗曚綅绗旇鏈?`opencode serve`锛涘叆鍙?`README.md`锛?
<!-- 宸插綊妗ｏ紙缁撻」锛屼笉鍐嶅綋娲昏穬椤圭洰鎵紱璺緞浠嶅彲璺敱锛?-->

- `娣变腑閫氶亾etc鏁版嵁鍒嗘瀽` 鈫?`archive_jobs/娣变腑閫氶亾etc鏁版嵁鍒嗘瀽/`锛坅rchived, 鍏ュ彛 `闃舵鎬荤粨.md`锛涙柟娉曡 `rules/skills/bestpractice_data_analysis_pipeline.md`锛?- `楦胯挋鍐呴儴鍒嗕韩` 鈫?`archive_jobs/harmony/`锛坅rchived, 鍏ュ彛 `闃舵鎬荤粨.md`锛汚I vs 缁堢増瀵规瘮 `review_final/AI_vs_缁堢増瀵规瘮鎬荤粨.md`锛?
