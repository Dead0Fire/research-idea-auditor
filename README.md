# Research Idea Auditor — 可复用科研审计 Skill

这是一个基于 Agent Skills `SKILL.md` 规范编写的独立技能包，作用是将模糊 idea 拆成真实问题、相关工作、机制假设、实验检验与具体决策。它不具备自己运行外部实验、访问私有论文库或自动长期跟踪的能力；这些能力取决于运行它的 AI 工具与授予的访问权限。

## 文件

- `SKILL.md`：Skill 元信息与核心执行流程。
- `references/evidence-and-literature.md`：文献检索与查重标准。
- `references/edge-vlm-checklist.md`：端侧多模态推理专项检查。
- `references/modes-and-templates.md`：输入、输出、solo 组会、两周计划模板。
- `references/source-notes.md`：源观点整合与风险修正。
- `examples/edge-vlm-spec-decoding.md`：针对约 2B VLM 投机解码的示例。

## 使用方式

将完整目录放入支持 Agent Skills 的工具所使用的 skills 目录（以具体工具文档为准），不要只复制 SKILL.md 而丢失它引用的文件。也可直接把 SKILL.md 作为会话指令使用，但参考文件需要一并提供。

常见调用示例：

- “审计这个 idea：利用视觉信息为 2B VLM 的免训 draft 提高接受率。请先判断问题真实性和最接近工作。”
- “对这个想法做 prior-art 检索，给我最相近 5 篇论文和真实差异，不要编造。”
- “切换 mentor-review，用审稿人的思路质询我，只留下能在一周内验证的问题。”
- “把目前的模糊猜测改成 48 小时内能回答的最小实验。”
- “根据下面的失败日志做 failure-review，优先排除测量误差和替代解释。”

## 注意

本包是技能文件，不表示已安装到你的账号或任何终端工具。是否支持 ZIP 导入、使用哪一路径及如何激活，取决于你使用的客户端。