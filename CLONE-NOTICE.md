# 克隆来源声明 / Clone Notice

> **本仓库（`hjphh11/folia-major`）是第三方克隆，不是官方仓库，也不是 GitHub Fork。**
> **This repository is an unofficial clone, not the upstream project and not a GitHub fork.**

## 来源 / Source

| 项目 | 值 |
| --- | --- |
| 原仓库 / Upstream | <https://github.com/chthollyphile/folia-major> |
| 原项目名 / Project | Folia（Lyrics Reimagined // 辞曲新境） |
| 原作者 / Original author | [chthollyphile](https://github.com/chthollyphile) 及 [全部贡献者](https://github.com/chthollyphile/folia-major/blob/main/CONTRIBUTORS.md) |
| 克隆基线 / Cloned baseline | `main` @ [`1f2c32a5d91afd1446a9ca8e7d4305ca6f9f22ed`](https://github.com/chthollyphile/folia-major/commit/1f2c32a5d91afd1446a9ca8e7d4305ca6f9f22ed)（v0.7.13，2026-10-04） |
| 许可证 / License | AGPL-3.0（原 `LICENSE` 文件原样保留，未作任何修改） |

本仓库由原仓库的 `main` 分支克隆而来，保留了完整的上游提交历史，仅在此基础上追加了本说明与 README 顶部的克隆标注。
代码、文档、图片、徽章、界面设计与商标等全部权利均归原作者及贡献者所有。**本仓库不主张任何著作权**，仅作个人部署使用。

## 与上游的差异 / Differences from upstream

除下列两项外，仓库内容与上游基线提交完全一致（业务代码、构建配置、依赖清单均未改动）：

1. **新增克隆标注**：本文件 `CLONE-NOTICE.md`，以及 `README.md` 顶部的克隆声明段落。
2. **移除上游 CI 工作流**：删除了 `.github/workflows/` 下的 9 个上游 GitHub Actions 文件
   （`electron-release.yml`、`nightly-pre-release.yml`、`canary-pre-release.yml`、`release-candidate.yml`、
   `pr-unit-tests.yml`、`docker-stack-*.yml`、`sync-server-docker-publish.yml`、`codemap-sync.yml`）。
   原因：向本仓库推送所使用的 GitHub OAuth 凭据不具备 `workflow` scope，无法创建 workflow 文件；
   且这些工作流用于上游的桌面端发布与镜像发布，与本次 Web 部署无关，避免误触发上游发布流程。

如需恢复这些上游 CI 文件（例如为了让本仓库能持续合并上游更新），执行：

```bash
gh auth refresh -s workflow      # 为凭据补充 workflow scope
git fetch upstream
git checkout upstream/main -- .github/workflows
git commit -m "chore: restore upstream workflows"
git push
```

## 使用限制 / Usage restrictions

- 本仓库及其中代码依据 **AGPL-3.0** 授权。任何使用、修改、分发或通过网络提供服务的行为，都必须遵守该许可证
  （包括保留版权声明与许可证文本、向网络服务的用户提供对应源代码）。
- 遵照原仓库的[法律与免责声明](https://github.com/chthollyphile/folia-major#法律与免责声明)：
  仅限**个人学习、技术交流与非营利测试**使用，**禁止任何商业盈利用途**。
- 应用中涉及的在线音乐流媒体、歌词、专辑封面及其他内容，其版权归对应权利人所有；请通过官方平台支持正版。
- 不得以任何方式暗示本克隆仓库由原作者维护、认可或背书；不得使用原项目名称、标识进行误导性宣传。
- 转载、再分发或以本仓库为基础发布衍生版本时，请保留本声明、原 `LICENSE` 与原作者署名。

## 免责 / Disclaimer

本仓库为个人自用部署产物，与原作者及贡献者**无任何关联**，未获得其授权或背书。
原作者不对本仓库的内容、可用性与运行结果承担任何责任；使用本仓库产生的风险与后果由使用者自行承担。

---

*最后更新：本声明随克隆提交一并写入，如后续同步上游更新请一并核对本文件。*
