# Phase 01: Foundation and Working Prototype

This phase turns the validated source into the first usable production layer: direction documents for language, slides, and the mobile-first ebook, plus a static HTML preview that renders a sample slide and ebook chapter excerpt. It is intentionally self-contained so the first Auto Run produces visible progress without needing user decisions or external tools.

## Tasks

- [x] Inspect the existing project context before creating anything:
  - Read `fluxo padrão/00_estado-projeto.md`, `fluxo padrão/01_briefing-inicial.md`, `fluxo padrão/04_roteiro-mestre-rascunho.md`, `fluxo padrão/07_fontes-e-evidencias.md`, `fluxo padrão/08_fonte-mestre-validada.md`, and `diretrizes/notebooklm-fluxo-producao.md`.
  - Confirm the active checkpoint is creation of product direction documents before asking NotebookLM for final slides or ebook chapters.
  - Reuse the existing folder pattern: `diretrizes/` for direction documents, `prompts/` for external-tool prompts, `outputs/` for received outputs, and `revisoes/` for audits.
  - Completion note (2026-06-29): inspected the six requested source/direction files plus existing `diretrizes/` examples. Confirmed the active checkpoint is to create product direction documents before requesting final slides or ebook chapters from NotebookLM, and confirmed the existing folder pattern (`diretrizes/`, `prompts/`, `outputs/`, `revisoes/`) should be reused. No associated images were found for this task.

- [x] Create `diretrizes/00-indice-producao.md` as a structured Markdown production index:
  - Include YAML front matter with `type: reference`, `title: Indice de Producao`, `created` using the current local date, `tags: [controle-carga, producao, notebooklm]`, and `related` wiki-links to `[[Fonte Mestre Validada]]`, `[[Diretriz Apresentacao Slides]]`, `[[Diretriz Ebook Mobile First]]`, and `[[Criterios Linguagem Densidade Nivel Operacional]]`.
  - Summarize the current project status, the source hierarchy, the products to be created, and the rule that final products must be generated in parts rather than in one large prompt.
  - Link the existing source files by path and state the role of each file in one concise paragraph.
  - Completion note (2026-06-29): created `diretrizes/00-indice-producao.md` with structured YAML front matter, required wiki-links, current project status, source hierarchy, planned slide/ebook products, the NotebookLM by-parts production rule, and path links to the core source files with concise role descriptions. No associated images were found or analyzed for this task.

- [x] Create `diretrizes/criterios-linguagem-densidade-nivel-operacional.md` as the shared editorial standard:
  - Include YAML front matter with `type: reference`, `title: Criterios de Linguagem, Densidade e Nivel Operacional`, `created` using the current local date, `tags: [linguagem, densidade, trainees, controle-carga]`, and `related` wiki-links to `[[Fonte Mestre Validada]]`, `[[Diretriz Apresentacao Slides]]`, and `[[Diretriz Ebook Mobile First]]`.
  - Define the target reader as trainees in Educacao Fisica preparing to act as personal trainers with the general public.
  - Specify the required tone: practical, formative, operational, professional, rigorous without becoming academic-heavy.
  - Include explicit rules for what to include, what to simplify, what to avoid, and how to phrase adjustments without making the trainee sound insecure.
  - Add a short checklist the future agent can use to reject outputs that become too clinical, too athletic-performance focused, too generic, or too dense.
  - Completion note (2026-06-29): created `diretrizes/criterios-linguagem-densidade-nivel-operacional.md` as the shared editorial standard with structured YAML front matter, required wiki-links, target reader definition, tone requirements, inclusion/simplification/avoidance rules, professional phrasing guidance, slide/ebook density rules, technical level guidance, and a rejection checklist for outputs that drift clinical, athletic-performance focused, generic, or dense. Reused the existing `diretrizes/criterios-linguagem-densidade-operacional.md` as source pattern. No associated images were found or analyzed for this task.

- [x] Create `diretrizes/diretriz-apresentacao-slides.md` as the slide-deck direction document:
  - Include YAML front matter with `type: reference`, `title: Diretriz Apresentacao Slides`, `created` using the current local date, `tags: [slides, aula, notebooklm, controle-carga]`, and `related` wiki-links to `[[Roteiro Mestre]]`, `[[Fonte Mestre Validada]]`, and `[[Criterios Linguagem Densidade Nivel Operacional]]`.
  - Define the presentation as a 60 to 90 minute internal training for trainees, with 8 blocks matching `fluxo padrão/04_roteiro-mestre-rascunho.md`.
  - Propose a slide structure per block: opening problem, core concept, applied decision frame, instructor example entry point, and synthesis.
  - Include a recommended total slide range, speaker-support notes style, and rules for avoiding overloaded slides.
  - Include mandatory slide elements: carga externa vs carga interna, RPE/RIR plus tecnica, matriz de decisao, sinais de fadiga, frases modelo, frases a evitar, and final pergunta-guia.
  - Completion note (2026-06-29): created `diretrizes/diretriz-apresentacao-slides.md` with structured YAML front matter, required wiki-links, 60-90 minute trainee-training definition, 8-block mapping from the roteiro mestre, per-block slide structure, recommended total slide range, speaker-support notes style, overload-prevention rules, mandatory slide elements, acceptance criteria, and the rule to generate the deck in NotebookLM by stages. No associated images were found or analyzed for this task.

- [x] Create `diretrizes/diretriz-ebook-mobile-first.md` as the ebook direction document:
  - Include YAML front matter with `type: reference`, `title: Diretriz Ebook Mobile First`, `created` using the current local date, `tags: [ebook, mobile-first, trainees, controle-carga]`, and `related` wiki-links to `[[Fonte Mestre Validada]]`, `[[Roteiro Mestre]]`, and `[[Criterios Linguagem Densidade Nivel Operacional]]`.
  - Define the ebook as a mobile-first study and consultation material, not a dense textbook.
  - Map the 8 roteiro blocks into chapters with medium length, short sections, operational examples, and mini checklists.
  - Require recurring components: quick definition boxes, "observe antes de ajustar" prompts, decision checklists, communication phrases, and chapter recaps.
  - Include acceptance criteria for mobile readability: short paragraphs, clear headings, no wide tables unless converted to cards, and no dependence on lecturer-only oral examples.
  - Completion note (2026-06-29): updated `diretrizes/diretriz-ebook-mobile-first.md` with structured YAML front matter, required wiki-links, explicit mobile-first study/consultation definition, 8-block chapter mapping, medium-length chapter guidance, required recurring components, mobile readability acceptance criteria, and NotebookLM staged-production guidance. Reused the existing ebook direction draft and aligned references to the validated source, roteiro mestre, and operational language criteria. No associated images were found or analyzed for this task.

- [x] Create `prototipos/preview-produtos.html` as a dependency-free working prototype:
  - Build a single static HTML file with inline CSS and no external assets.
  - Render three visible sections: product header, sample slide preview, and sample mobile ebook preview.
  - Use only content grounded in `fluxo padrão/08_fonte-mestre-validada.md`: the guiding question, carga externa vs carga interna, the acute decision matrix, signs of fatigue, and professional communication phrases.
  - Make the layout responsive: desktop shows slide and mobile preview side by side; narrow screens stack the sections cleanly.
  - Avoid decorative marketing layout; make it feel like an educational production preview for an internal training material.
  - Completion note (2026-06-29): created `prototipos/preview-produtos.html` as a single dependency-free static HTML file with inline CSS only. The preview includes a product header, sample slide preview, and sample mobile ebook preview grounded in `fluxo padrão/08_fonte-mestre-validada.md` content: the guiding question, carga externa vs carga interna, the acute decision matrix, signs of fatigue, and professional communication phrases. Verified desktop side-by-side layout and mobile stacked layout with headless Chrome screenshots. No associated source images were found or analyzed for this task.

- [x] Add a short validation note inside `prototipos/preview-produtos.html` near the bottom:
  - State which source files informed the preview.
  - State that the preview is not the final slide deck or final ebook.
  - State that the next phase should create NotebookLM prompt packs from the direction documents.
  - Completion note (2026-06-29): added a bottom validation note to `prototipos/preview-produtos.html` naming the source files that informed the preview, clarifying that the file is not the final slide deck or final ebook, and directing the next phase to create NotebookLM prompt packs from the direction documents with production in parts. Verified the required copy with `rg` and rendered the static HTML with headless Google Chrome. Analyzed 2 associated preview screenshots from `.maestro/playbooks/Working/`.

- [x] Verify Phase 01 deliverables:
  - Confirm these files exist: `diretrizes/00-indice-producao.md`, `diretrizes/criterios-linguagem-densidade-nivel-operacional.md`, `diretrizes/diretriz-apresentacao-slides.md`, `diretrizes/diretriz-ebook-mobile-first.md`, and `prototipos/preview-produtos.html`.
  - Open or inspect `prototipos/preview-produtos.html` and confirm it renders meaningful slide and ebook previews without requiring a build step.
  - Check that the new Markdown files contain YAML front matter and wiki-links.
  - Confirm no final production prompt asks NotebookLM to generate the entire slide deck or ebook in one pass.
  - Completion note (2026-06-29): verified all required Phase 01 deliverable files exist. Rendered `prototipos/preview-produtos.html` directly with headless Google Chrome, with no build step, and confirmed the screenshot contains a meaningful product header, sample slide preview, and mobile ebook preview. Confirmed the Markdown direction files contain YAML front matter and wiki-links; during verification, corrected `diretrizes/diretriz-apresentacao-slides.md` by adding the missing structured front matter/wiki-links and aligning its criteria reference to `diretrizes/criterios-linguagem-densidade-nivel-operacional.md`. Confirmed prompt/direction files do not ask NotebookLM to generate the entire slide deck or ebook in one pass; the matching instructions explicitly require staged production. No associated source images were found for this task; generated and analyzed 1 verification screenshot in `.maestro/playbooks/Working/`.
