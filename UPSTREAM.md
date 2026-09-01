# 上游同步政策（UPSTREAM）

## 釘選版本

| 項目 | 值 |
|---|---|
| 上游 repo | https://github.com/msitarzewski/agency-agents |
| 分支 | `main` |
| 釘選快照日期 | 2026-09-01 |
| 釘選 commit SHA | _待補_ |

> 建議動作：`git clone https://github.com/msitarzewski/agency-agents upstream-ref`
> 然後 `git -C upstream-ref rev-parse HEAD` 取得 SHA 填入上表與 `ATTRIBUTION.md`。

## 同步原則

1. **不自動 merge。** 上游更新後，逐檔 `diff` 本 repo 已收錄的檔案對應的上游檔案。
2. **只同步已收錄的檔案。** 上游新增的 Agent 不會自動納入；是否新增由選錄標準決定。
3. **語意變更才重譯。** 上游若只是錯字、排版微調，可略過；若角色設定、流程、規則有實質變化，
   重新翻譯對應段落並在 `CHANGELOG.md` 記錄。
4. **保留一個週期的舊版。** 上游若移除或大幅改寫某 Agent，本 repo 在下一次發佈前保留舊版，
   並在 `CHANGELOG.md` 標註「上游已移除／大改」。
5. **檢視頻率：** 每季一次，或當上游發佈重大版本時。

## 同步檢查清單

- [ ] 更新 `upstream-ref` 到最新 `main`
- [ ] 記錄新的 commit SHA 到本檔與 `ATTRIBUTION.md`
- [ ] 對每個已收錄檔案跑 `diff`
- [ ] 重譯有語意變更的段落
- [ ] 更新 `docs/術語對照表.md`（若出現新術語）
- [ ] 更新 `CHANGELOG.md`
- [ ] 通知姊妹 repo `ai-to-agent-agency-course-zh-TW` 是否需要同步調整教材
