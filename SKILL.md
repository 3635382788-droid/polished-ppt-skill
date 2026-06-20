---
name: polished-ppt
description: Create premium, visually polished, editable PowerPoint decks by orchestrating presentation editing, visual design, generated images, browser screenshots, charts, diagrams, and source-document extraction. Use when the user asks for beautiful/high-end/professional PPTs, presentation-ready decks, slide redesigns, defense/report decks, template-based PPT edits, project showcase decks, or wants multiple skills/tools combined to produce a polished .pptx.
---

# Polished PPT

## Core Rule

Produce an editable `.pptx`, not image-only slides. For final deck creation or editing, use the `presentations` skill and its artifact-tool workflow. Preserve a supplied template unless the user asks for a redesign.

Use this skill as an orchestration layer:

- Use `presentations` for PPTX import, editable slide construction, template following, rendering, QA, and export.
- Use `imagegen` for generated bitmap assets such as cover art, hero backgrounds, product illustrations, and scene images.
- Use `frontend-design` judgment for visual systems, spacing, hierarchy, and avoiding generic AI-looking layouts.
- Use browser/Chrome control when real project pages, localhost apps, dashboards, or websites should be captured as screenshots.
- Use spreadsheet/chart tooling for tables, metrics, KPI cards, and native charts.
- Use document/PDF tooling when source material comes from Word, PDF, reports, papers, or existing manuals.
- Use Mermaid or native shapes for architecture diagrams, workflows, module maps, and sequence/process views.

## Workflow

1. Define the deck mode:
   - `create`: build a new deck from materials.
   - `template-following`: use an existing PPT as the visual template.
   - `targeted-edit`: modify only requested slides.
   - `visual-upgrade`: keep the same story but redesign for a more polished look.

2. Build the source ledger:
   - Extract facts from user files, existing slides, docs, screenshots, spreadsheets, or code.
   - Record where each important claim or asset came from in the presentations workspace source notes.
   - Do not invent metrics, screenshots, logos, product UI, dates, or project claims.

3. Design the deck system before coding:
   - Pick one dominant palette, one supporting tone, and one accent.
   - Define heading/body fonts and a role-based type scale.
   - Choose 3-5 reusable slide patterns.
   - Decide where real screenshots, generated images, charts, or diagrams add evidence.
   - Read [references/design-playbook.md](references/design-playbook.md) for design patterns.

4. Create or edit slides:
   - Keep each slide to one message.
   - Prefer visual proof over paragraphs: screenshots, flows, module maps, diagrams, KPI cards, before/after, or architecture blocks.
   - Use editable text, shapes, tables, charts, and images.
   - For project showcase decks, include a clear module ownership slide, a feature workflow slide, and at least one real UI or system screenshot when available.

5. Verify the deck:
   - Render final slides whenever possible.
   - Inspect for overflow, clipping, weak contrast, crowded pages, inconsistent spacing, and broken image crops.
   - Check old-topic remnants after deletions or rewrites.
   - Read [references/qa-checklist.md](references/qa-checklist.md) before delivery.

## Output Standard

Deliver the final `.pptx` path and a short summary of what changed or what was created. Mention any render/tool caveat only when it affects confidence.

For Chinese coursework or defense decks, keep wording concise and formal. Prefer titles such as `项目总览`, `系统架构`, `核心功能`, `模块实现`, `测试结果`, `项目亮点`, and `总结致谢`.
