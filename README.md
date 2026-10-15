# MixMatter for Codex Cloud

照片的编辑印刷风格重构：半色调、双色印刷、平面色块与撕纸拼贴。

本仓库提供 Codex 可发现的 MixMatter skill。作者：Fan Jiale / Galok。
上游：https://github.com/galokme/MixMatter

## 文件

- `.agents/skills/mixmatter/SKILL.md`：风格和处理规则。
- `.agents/skills/mixmatter/references/`：完整提示词和质量标准。
- `LICENSE`：上游 MIT 许可证。

Skill 文件与此前本地安装版本一致，未改写作者规则；不代表追踪上游最新版本。

## 在 Codex Cloud 中使用

1. 创建或编辑云端环境，选择本仓库 `soapahhhhhh/soap`，使用 `main` 分支。
2. 该 skill 本身无需 npm、Python 包或常驻服务，保持依赖配置精简即可。
3. 完成环境准备并发布后，从该环境开启新任务。
4. 先发送下面的检查指令，确认技能及图片工具是否可用。
5. 再上传照片，使用 MixMatter 请求图片编辑。

### 检查指令

> 请加载 .agents/skills/mixmatter/SKILL.md，确认两个 references 文件完整，并检查当前任务实际可用的图片生成或编辑工具。先报告能力，不生成图片。不要仅凭 skill 已加载就声称可以出图。

### 处理照片

上传照片并发送：

> 用 $mixmatter 处理这张图。保留人物身份、主要姿态和原始长宽比，不新增文字。使用当前任务实际可用的图片编辑工具返回结果；如果没有图片工具，明确说明，并提供针对这张图可直接用于图片模型的完整提示词。

## 能力与配置

本仓库提供规则，不自带图片模型、API 凭据或托管服务。
实际出图取决于云端任务的工具权限。若无图片工具，skill 会提供可用于图片模型的提示词。

仓库上传完成、环境发布成功和实际出图验证是三个独立步骤。
本仓库不预先宣称环境已经发布或图片生成已经验证。

官方文档：
- https://learn.chatgpt.com/docs/environments/cloud-environments
- https://learn.chatgpt.com/docs/build-skills
- https://learn.chatgpt.com/docs/image-generation
