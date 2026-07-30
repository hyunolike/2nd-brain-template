# Wiki Log

> Chronological record of wiki actions. This file is append-only: add entries at
> the end and never rewrite or remove an earlier entry.
>
> Entry heading format: `## [YYYY-MM-DD] <action> | <subject>`
>
> Allowed actions: `ingest`, `create`, `update`, `query`, `lint`, `archive`,
> `delete`, `map`, and `repair`.
>
> Each entry lists every affected repository-relative path. After 500 entries,
> rotate the completed file to `log-YYYY.md` and begin a new `log.md`; preserve the
> completed file unchanged.

## [2026-07-21] ingest | 2nd-Brain 개인지식 관리 원본 배치

- Selection: `understand-chat` identified the 2nd-Brain PKM core subgraph and its one-hop canonical neighbors; their leading frontmatter referenced 13 unique raw sources.
- Created:
  - `raw/notebooklm/2026-07-16-all-notes.md`
  - `raw/notebooklm/codegraph-github.md`
  - `raw/notebooklm/graphify-github.md`
  - `raw/notebooklm/llm-wiki-skill-github.md`
  - `raw/notebooklm/llm-wiki-zotero-notebooklm-youtube.md`
  - `raw/notebooklm/notebooklm-py-github.md`
  - `raw/notebooklm/understand-anything-github.md`
  - `raw/notebooklm/zotero-mcp-github.md`
  - `raw/web/NomaDamasslides-grab Best harness + editor + linter for generating slides in Claude Code  Codex - Claude Design Open Source Alternative.md`
  - `raw/web/stablyaiorca Orca is the ADE for working with a fleet of parallel agents. Run any coding agent with your own subscription. Available on desktop and mobile..md`
  - `raw/youtube/📺 How To Build LLM Wiki In Obsidian 🧠 A Memory Layer For Any Agentic AI.md`
  - `raw/youtube/📺 LLM Wiki를 업그레이드하는 외부 지식 시스템! 연구자를 위한 최강의 조합 Zotero × Notebook × Obsidian x Claude Code.md`
  - `raw/youtube/📺 Orca Is the Free Cursor Killer Nobody's Talking About!.md`
- Updated: `SCHEMA.md`, `AGENTS.md` to register importer-preserved raw directories and legacy hash-coverage handling.
- Integrity: all 13 target files are byte-identical to the source vault; all 8 recorded post-frontmatter body hashes match; 5 legacy web/video captures have no recorded `sha256` and retain their original missing final LF as explicit coverage and format gaps.
- Canonical state: unchanged at 0 pages; `index.md` was not modified.

## [2026-07-21] lint | 0 issues found

- Raw files in the imported source set: 13.
- Source/target byte-identical files: 13.
- Recorded post-frontmatter body hashes checked and matched: 8.
- Documented legacy hash-coverage and final-LF format gaps: 5.
- Invalid UTF-8, BOM, CRLF, body-hash drift, missing ingest-log paths, and unregistered importer directories: 0.
- Canonical pages and index entries: 0; no canonical navigation update was required.

## [2026-07-21] create | 2nd-Brain canonical 지식 코어

- Evidence: the existing 13-file raw source set was mapped to eight central, reusable PKM subjects; no raw record was duplicated or mutated.
- Created:
  - `concepts/ai-knowledge-workflow.md`
  - `concepts/ai-personal-knowledge-management.md`
  - `concepts/llm-wiki.md`
  - `concepts/research-feedback-loop.md`
  - `concepts/second-brain-research-workflow.md`
  - `comparisons/knowledge-tool-roles.md`
  - `queries/notebooklm-query-compounding.md`
  - `queries/ua-knowledge-graph-workflow.md`
- Updated:
  - `SCHEMA.md`
  - `index.md`
  - `log.md`
- Navigation: the eight-page graph uses only resolvable canonical wikilinks, with at least two distinct non-self links per page.
- Provenance: every source and claim marker resolves to an existing repository-relative raw Markdown path.

## [2026-07-21] lint | 0 issues found

- Canonical pages: 8 total (5 concepts, 1 comparison, and 2 queries); all required frontmatter fields, types, dates, confidence values, contestation fields, and contradiction lists are valid.
- Taxonomy and navigation: 9 registered tags, 8 exact alphabetical index entries, 33 canonical links, minimum 3 outbound links per page, and minimum 2 inbound links per page.
- Provenance: 27 source references and 17 claim-level markers resolve to existing raw Markdown records; no marker is absent from its page source list.
- Raw integrity: 13 Markdown records checked, 8 recorded body hashes matched, and 5 importer-preserved legacy hash/final-LF coverage gaps remain documented.
- Formatting, duplicate slugs, broken links, self-links, orphan pages, source drift, and lint warnings: 0.

## [2026-07-21] repair | lint source-reference count correction

- Correction: the immediately preceding lint entry reports 27 source references, but the measured canonical frontmatter total is 30.
- Unchanged measurements: 17 claim-level markers, 33 canonical links, 8 canonical pages, and 0 lint errors or warnings.
- Updated: `log.md` only; no raw or canonical page was changed.

## [2026-07-30] create | Orca ADE (LLM Wiki 컴파일 PoC)

- Evidence: 두 개의 미컴파일 raw 소스(`raw/web/stablyai...orca...md` web 캡처, `raw/youtube/📺 Orca Is the Free Cursor Killer...md` 리뷰)가 "Orca"를 중심 주제로 다뤄 2-소스 임계값을 충족. 원본은 수정하지 않음.
- Created: `entities/orca.md` (첫 entity 페이지; 이전까지 Entities 섹션은 비어 있었음).
- Updated: `index.md` (Entities 항목 추가, 총계 8 → 9), `log.md`.
- Navigation: `[[knowledge-tool-roles]]`, `[[llm-wiki]]` 두 개의 유효·비자기 canonical 링크로 연결.
- Provenance: 4개 claim-level 마커가 모두 frontmatter `sources`에 등재된 raw 경로로 해석됨.
- Taxonomy: 기존 등록 태그 `automation`, `workflow`만 사용(신규 태그 도입 없음).
- Quality: `confidence: medium` — 핵심 사실은 2소스 교차 검증되나 팀 배경·한계는 단일(YouTube) 소스이고 제품 변화가 빨라 신선도 확인이 필요.

## [2026-07-30] lint | 0 issues found (Orca PoC)

- Canonical pages: 9 total (1 entity, 5 concepts, 1 comparison, 2 queries); `entities/orca.md`의 필수 frontmatter 9개 필드·type·날짜·confidence·contestation·contradictions 모두 유효.
- Navigation: `index.md` 총계 9가 파일시스템 canonical 수와 일치; orca 페이지의 아웃바운드 링크 2개(`[[knowledge-tool-roles]]`, `[[llm-wiki]]`)가 모두 활성 canonical로 해석, broken/self-link 없음.
- Provenance: claim-level 마커 4개가 모두 frontmatter `sources`의 실존 raw 경로로 해석됨.
- Taxonomy: 사용 태그 2개(`automation`, `workflow`) 모두 SCHEMA 등록 태그.
- Formatting: UTF-8, LF only(CR 0), 최종 개행 존재, BOM 없음, 46줄(200줄 임계값 이하).
- Raw integrity: raw 소스는 열람만 하고 변경하지 않음.
