# 本地增量（相对上游 1.1.77）

本目录 = 上游 YuJunZhiXue/dsh-purge master（1.1.77）+ 0.2.1 适配增量，版本号 1.1.78。

上游 1.1.77 在 dsh 0.2.1 上还有 3 条补丁整条打不中（#32 / #53 / #77），#68 少一条新锚点：

1. 	argetFiles() 新增 harness-dev-context → dsh-harness-dev-context/lib/index.js（0.2.1 把 Web 面提示词搬到了这个新包）。
2. #32 目标加 harness-dev-context，新增两条 needle：...whose URL the runtime context names. 与 description: "Advertised URL of ..."。
3. #53 目标加 harness-dev-context（"不许另开服务器" 那句）。
4. #68 新增 0.2.1 那行 if (firstAttempt) for (const message of decision.messages) if (message.source.kind === "runtime-context") { 的兜底。
5. #77 新增 0.2.1 的 if (this.revised.size > 0) this.revised.clear(); 锚点。

验证（对 0.2.1-rc.2 的 293 个包、0.2.1-rc.3 的 294 个包各跑一遍、在目录副本上真打）：

    before : {"pending":64,"applied":8,...}
    apply  : 64 → 全命中，0 pending，二次 apply 无漂移
    js/yaml: 900+ 文件 node --check / YAML 解析全过

回滚：删掉这 5 处增量即可回到上游 1.1.77 行为；或直接从上游 master 重装。
