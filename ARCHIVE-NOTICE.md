# 归档说明 / Archive Notice

## 中文

**这不是本仓库作者的原创项目，而是一份源码存档 + 本地派生构建。**

| 项 | 内容 |
|---|---|
| 项目名 | `dsh-purge` — DeepSeek Harness 网络安全红队工具 / 破甲插件 |
| 版本 | **1.1.78**（本地构建号；上游为 **1.1.77**，本仓 = 上游 + 0.2.1 覆盖层，见 `LOCAL-OVERLAY.md`） |
| 原作者 | **小杨**（`@YuJunZhiXue`），见 `LICENSE`：`Copyright 2026 YuJunZhiXue` |
| 原仓库 | https://github.com/YuJunZhiXue/dsh-purge |
| 原仓库状态 | **已恢复可访问**（此前一度 `Could not resolve to a Repository`），`master` 当前为 **1.1.77** |
| 许可 | **Apache-2.0**（上游自 1.1.7x 起由 MIT 改为此许可，已附带 `NOTICE` 与 `LICENSE-COMMERCIAL.md`；本仓原样保留） |
| 存档来源 | 早期版本取自本机已安装的插件目录（v1.1.71）；当前版本取自上游 `master` 的 codeload 压缩包（v1.1.77），再叠加本地覆盖层 |
| 更新日期 | 2026-10-24 |
| 存档范围 | 99 个文件（`lib/`、`bin/`、`presets/`、`scripts/`、`docs/`、`client.js`、`cordis.patch.yml`、README、release-notes、LICENSE、NOTICE 等） |

### 本仓做了哪些改动（Apache-2.0 §4(b) 要求声明）

相对上游 `master`（v1.1.77），本仓只多出以下内容，全部记录在案：

1. `lib/core.js` —— 追加 DSH 0.2.1 的 5 处补丁锚点（`harness-dev-context` 目标、#32 / #53 / #68 / #77）；
2. `package.json` —— 版本号 1.1.77 → **1.1.78**，`dshTarget` 指向 `0.2.1-rc.3`；
3. `LOCAL-OVERLAY.md` —— 上述增量的说明与回滚方式；
4. `ARCHIVE-NOTICE.md` —— 本文件；
5. 两个 README 顶部的一行存档横幅；
6. `.gitignore` —— 恢复 `*.pre-fix-*` 规则，防止补丁前备份文件再次进仓。

**没有删除、没有改写上游的任何源码或文档。** 上游在 1.1.71 → 1.1.77 之间自行移除了 `skills/redteam/*.md`（23 个技能文件），因此当前树中不含这些文件；它们仍可从本仓历史提交 `b483e1e` 完整取回。

### 署名

依据原作者在 `README.zh-CN.md`「署名要求」一节的要求：

> 借用本项目的名称、思路、代码或提示词，必须署名，并写明来源仓库：YuJunZhiXue/dsh-purge。

本仓库照此执行：

- 全部源码、文档、提示词、技能文件**版权归原作者 小杨（YuJunZhiXue）所有**。
- 本仓库**不主张任何著作权**，也不以任何形式商业售卖。
- `NOTICE` 与 `LICENSE` 原样保留，未作任何修改。
- 本仓库**不是官方发布**，构建号 1.1.78 仅在本仓存在；请勿据此判断上游发版。
- 如原作者要求下架，删除即可，无需理由。

### 为什么会有这个仓库

最初是为了在上游仓库不可访问时，保留一份可复现的技术资料（含 `release-notes.md` 里 1.1.x 全量变更记录）。上游恢复后，本仓转为「镜像 + 最小兼容覆盖层」，便于在本机 DSH 0.2.1 上复现验证，不构成对原作者任何权利的侵犯或主张。

### 免责

原项目自带的「严正法律免责与合规使用声明」在 `README.zh-CN.md` 中原样保留，其约束力不因本存档而改变。使用本项目代码即表示接受该声明。存档者不对任何第三方使用行为负责。

---

## English

**This is not the original work of this repository's owner — it is a source archive plus a small local derivative build.**

| Field | Value |
|---|---|
| Project | `dsh-purge` — DeepSeek Harness cybersecurity red-team / prompt-patch plugin |
| Version | **1.1.78** (local build number; upstream is **1.1.77**; this repo = upstream + 0.2.1 overlay, see `LOCAL-OVERLAY.md`) |
| Original author | **小杨 (Xiao Yang)**, GitHub `@YuJunZhiXue` — see `LICENSE`: `Copyright 2026 YuJunZhiXue` |
| Upstream | https://github.com/YuJunZhiXue/dsh-purge |
| Upstream status | **Available again** (it was briefly unreachable); `master` is currently **1.1.77** |
| License | **Apache-2.0** (upstream relicensed from MIT and now ships `NOTICE` + `LICENSE-COMMERCIAL.md`, both kept as-is here) |
| Source of this copy | Earlier version from the locally installed plugin (v1.1.71); current version from the upstream `master` codeload archive (v1.1.77) with the local overlay applied |
| Updated on | 2026-10-24 |
| Scope | 99 files: `lib/`, `bin/`, `presets/`, `scripts/`, `docs/`, `client.js`, `cordis.patch.yml`, READMEs, `release-notes.md`, `LICENSE`, `NOTICE` |

### What this repository changed (Apache-2.0 §4(b) disclosure)

Relative to upstream `master` (v1.1.77), the only additions are:

1. `lib/core.js` — five DSH 0.2.1 patch anchors (`harness-dev-context` target; #32 / #53 / #68 / #77);
2. `package.json` — version 1.1.77 → **1.1.78**, `dshTarget` set to `0.2.1-rc.3`;
3. `LOCAL-OVERLAY.md` — explanation and rollback for the above;
4. `ARCHIVE-NOTICE.md` — this file;
5. a one-line archive banner at the top of both READMEs;
6. `.gitignore` — restores the `*.pre-fix-*` rule so pre-patch backups cannot be committed again.

**No upstream source or document was deleted or rewritten.** Upstream itself dropped `skills/redteam/*.md` (23 skill files) between 1.1.71 and 1.1.77, so they are absent from the current tree; they remain recoverable from this repo's history at commit `b483e1e`.

### Attribution

The original `README.zh-CN.md` requires attribution and a link to the source repository for anyone reusing the name, ideas, code, or prompts. This archive complies:

- All source code, docs, prompts and skill files remain **copyright © 小杨 (YuJunZhiXue)**.
- `NOTICE` and `LICENSE` are kept byte-for-byte, unmodified.
- No copyright is claimed here, and nothing is sold.
- **This is not an official release**; build number 1.1.78 exists only in this repository — do not read it as an upstream release.
- The author may request removal at any time; it will be deleted without argument.

### Why this exists

It began as a preservation copy while the upstream repository was unreachable. Now that upstream is back, this repository serves as a mirror plus the smallest possible compatibility overlay, so DSH 0.2.1 behaviour can be reproduced and verified locally.

### Disclaimer

The original project's legal/compliance statement in `README.zh-CN.md` is preserved verbatim and remains in force. Using this code means accepting it. The archivist is not responsible for third-party use.
