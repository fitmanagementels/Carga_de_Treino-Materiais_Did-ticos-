# Phase 04: Mobile Ebook Draft

This phase creates the first mobile-first ebook draft for trainees, using NotebookLM ebook outputs if available and falling back to the validated source when they are not. The result should be a readable study and consultation artifact, not just a plan for one.

## Tasks

- [x] Inspect ebook inputs and decide the source mode without asking the user:
  - Read `fluxo padrão/08_fonte-mestre-validada.md`, `fluxo padrão/04_roteiro-mestre-rascunho.md`, `diretrizes/diretriz-ebook-mobile-first.md`, `diretrizes/criterios-linguagem-densidade-operacional.md`, and `prompts/notebooklm-ebook-estrutura-e-capitulos.md`.
  - Check whether `outputs/produtos-ebook/` contains NotebookLM ebook outline or chapter outputs.
  - If NotebookLM ebook outputs exist, use them as the first source and correct them against `fluxo padrão/08_fonte-mestre-validada.md`.
  - If NotebookLM ebook outputs do not exist, create a local draft from `fluxo padrão/08_fonte-mestre-validada.md` and label the audit status as "rascunho local aguardando rodada NotebookLM".
  - Completion note 2026-06-30: required ebook inputs were inspected. `outputs/produtos-ebook/` currently contains only `README.md`, so there are no NotebookLM ebook outline or chapter outputs to use as first source. Source mode selected for the next task: local draft from `fluxo padrão/08_fonte-mestre-validada.md`, corrected against the 8-block master roteiro and ebook/language directives, with audit status `rascunho local aguardando rodada NotebookLM`.

- [x] Create `ebook/controle-carga-mobile.md` as the structured Markdown ebook draft:
  - Include YAML front matter with `type: reference`, `title: Ebook Mobile Controle de Carga`, `created` using the current local date, `tags: [ebook, mobile-first, controle-carga, trainees]`, and `related` wiki-links to `[[Diretriz Ebook Mobile First]]`, `[[Fonte Mestre Validada]]`, and `[[Roteiro Mestre]]`.
  - Organize the ebook into 8 chapters matching the master roteiro.
  - For each chapter, include: learning goal, short conceptual explanation, operational decision guidance, trainee-facing example, mini checklist, and recap.
  - Convert the acute decision matrix into mobile-friendly cards instead of a wide table.
  - Keep paragraphs short and avoid lecturer-only references that would not make sense during independent reading.
  - Completion note 2026-06-30: created `ebook/controle-carga-mobile.md` as a local-source mobile-first ebook draft with required YAML front matter, 8 chapters mapped to the master roteiro, recurring learning goals, short explanations, operational guidance, trainee-facing examples, mini checklists, recaps, and mobile-friendly decision cards replacing the acute adjustment table. No task-associated images were found or analyzed.

- [x] Create `ebook/controle-carga-mobile.html` as a dependency-free mobile reading prototype:
  - Use semantic HTML, inline or local CSS, and no external build step.
  - Render the ebook with a narrow comfortable reading measure, sticky or simple table of contents, readable typography, and clear chapter sections.
  - Include mobile-friendly cards for carga externa/carga interna, RPE/RIR plus tecnica, acute adjustment decisions, fatigue signs, and professional communication phrases.
  - Add print styles so the file can be saved as PDF later without navigation clutter dominating the pages.
  - Completion note 2026-06-30: created `ebook/controle-carga-mobile.html` as a dependency-free static HTML prototype rendered from the approved Markdown ebook. The prototype includes semantic chapter sections, a mobile-friendly index, a narrow reading measure, XSTEAM-inspired local CSS, quick-reference cards for carga externa/carga interna, RPE/RIR plus tecnica, acute adjustment decisions, fatigue signs, and communication phrases, plus print styles that remove navigation/progress UI for later PDF export. Verified 8 chapter sections, 13 decision cards, no external HTTP assets, balanced section tags, and a fresh 390px-wide Chrome screenshot in `.maestro/playbooks/Working/controle-carga-mobile-preview.png`. No task-associated source images were found; 1 generated verification screenshot was inspected.

- [ ] Encode the operational trainee workflow explicitly in the ebook:
  - Before adjusting, observe readiness and the first exposures to the exercise.
  - During the set, compare self-report, fluency, range, stability, rhythm, and compensations.
  - After the set, decide whether to maintain, progress, reduce, recover, simplify, or modify.
  - Communicate the adjustment by stating what was observed, why it matters, and what will change next.
  - Keep the focus on acute session decisions and exclude clinical diagnosis, athletic optimization, and complex periodization.

- [ ] Create `revisoes/produtos/auditoria-ebook-rascunho-01.md` as the first ebook audit:
  - Include YAML front matter with `type: analysis`, `title: Auditoria Ebook Rascunho 01`, `created` using the current local date, `tags: [ebook, auditoria, mobile-first, controle-carga]`, and `related` wiki-links to `[[Ebook Mobile Controle de Carga]]` and `[[Fonte Mestre Validada]]`.
  - Check mobile readability, conceptual fidelity, operational usefulness, language density, source traceability, exclusions, and chapter completeness.
  - List concrete corrections made during the phase and remaining items to verify after user or NotebookLM review.

- [ ] Correct the ebook Markdown and HTML based on the first audit:
  - Apply any fixes identified in `revisoes/produtos/auditoria-ebook-rascunho-01.md`.
  - Split paragraphs or sections that are too dense for mobile reading.
  - Replace wide tables with card-based alternatives.
  - Remove any drift into clinical diagnosis, performance-sport optimization, complex periodization, or registro as central workflow.

- [ ] Verify Phase 04 deliverables:
  - Confirm `ebook/controle-carga-mobile.md`, `ebook/controle-carga-mobile.html`, and `revisoes/produtos/auditoria-ebook-rascunho-01.md` exist.
  - Open or inspect `ebook/controle-carga-mobile.html` and confirm it is readable as a mobile-first artifact without a build step.
  - Confirm all 8 roteiro blocks appear as ebook chapters.
  - Confirm every chapter includes at least one operational element such as a checklist, decision prompt, example, phrase, or recap.
