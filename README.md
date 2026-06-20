# Polished PPT Skill

`polished-ppt` is a Codex skill for creating premium, presentation-ready PowerPoint decks. It orchestrates multiple Codex capabilities into one repeatable workflow for building beautiful, editable `.pptx` files.

## 功能总结

这个 skill 主要用于制作和美化高质量 PPT，适合课程答辩、项目展示、产品汇报、系统说明、竞赛路演等场景。

核心能力包括：

- **可编辑 PPT 生成与修改**：基于 `presentations` 工作流创建、导入、编辑、渲染并导出 `.pptx`。
- **高级视觉设计编排**：结合 `frontend-design` 的设计判断，统一配色、字体层级、间距、版式和页面节奏。
- **封面与视觉素材生成**：结合 `imagegen` 生成封面图、场景图、产品插画、模块视觉图等。
- **真实项目截图整合**：通过浏览器/Chrome 控制能力截取本地项目、网页、系统后台或仪表盘页面，增强答辩可信度。
- **图表与数据页制作**：结合表格、图表和 KPI 卡片，把营业额、销量、订单统计等数据做成清晰页面。
- **文档资料提炼**：从 Word、PDF、说明书、报告等材料中提取关键信息，转成适合 PPT 的短句结构。
- **流程图与架构图**：使用 Mermaid 或 PPT 原生形状绘制系统架构、业务流程、模块关系和时序流程。
- **质量检查**：内置 QA checklist，检查文字溢出、旧内容残留、图片裁切、版式不一致、图表缺少单位等问题。

## When To Use

Use this skill when you want Codex to:

- create a polished PowerPoint deck from source materials;
- redesign an existing PPT to look more professional;
- turn a project, document, codebase, or report into a defense/presentation deck;
- combine screenshots, diagrams, generated visuals, charts, and concise writing;
- preserve a template while replacing content;
- produce an editable `.pptx`, not image-only slides.

## Skill Structure

```text
polished-ppt/
├── SKILL.md
├── agents/
│   └── openai.yaml
└── references/
    ├── design-playbook.md
    └── qa-checklist.md
```

## Installation

Copy this folder into your Codex skills directory:

```bash
mkdir -p ~/.codex/skills
cp -R polished-ppt ~/.codex/skills/
```

Then start a new Codex thread or restart Codex so the skill can be discovered.

## Example Prompt

```text
Use $polished-ppt to turn my project materials into a polished defense PPT.
```

中文示例：

```text
Use $polished-ppt 帮我把这个项目 PPT 做得更高级、更漂亮，并加入截图、流程图和总结页。
```

## Notes

- Final slides should remain editable where practical.
- Generated images are for visual support and should not pretend to be real product evidence.
- Real screenshots, metrics, dates, logos, and product claims should come from user-provided or verified sources.

