---
title: Orca
created: 2026-07-30
updated: 2026-07-30
type: entity
tags:
  - automation
  - workflow
sources:
  - "raw/web/stablyaiorca Orca is the ADE for working with a fleet of parallel agents. Run any coding agent with your own subscription. Available on desktop and mobile..md"
  - "raw/youtube/📺 Orca Is the Free Cursor Killer Nobody's Talking About!.md"
confidence: medium
contested: false
contradictions: []
---

# Orca

Orca는 Stably가 만든 오픈소스 ADE(agent development environment)로, 여러 코딩 에이전트를 병렬로 오케스트레이션한다. 하나의 프롬프트를 Claude Code·Codex·Grok 등 여러 에이전트에 동시에 보내고, 각 에이전트가 격리된 git worktree에서 작업한 결과를 비교해 가장 나은 것을 병합한다. ^[raw/web/stablyaiorca Orca is the ADE for working with a fleet of parallel agents. Run any coding agent with your own subscription. Available on desktop and mobile..md]

전통적 IDE가 "한 사람이 한 번에 한 가지"를 가정해 설계된 반면, Orca는 "한 사람이 여러 AI 에이전트를 동시에 지휘"하는 것을 전제로 처음부터 설계됐다. 사용자는 코드를 직접 쓰기보다 에이전트를 오케스트레이션하고 검토·병합을 결정한다. ^[raw/youtube/📺 Orca Is the Free Cursor Killer Nobody's Talking About!.md]

## 핵심 기능

- **병렬 worktree:** 한 작업을 여러 에이전트에 팬아웃해 각각 독립된 worktree에서 실행하고 결과를 비교·병합한다. Orca의 중심 기능이다.
- **모든 CLI 에이전트 지원:** 터미널에서 도는 에이전트라면 무엇이든 실행. Claude Code, Codex, Cursor CLI, Copilot, OpenCode 등 다수를 지원한다.
- **Bring Your Own Subscription:** 중간 과금 없이 기존 에이전트 구독을 그대로 연결해 사용하며, 계정 전환과 사용량·rate-limit 추적을 내장한다.
- **모바일 컴패니언:** iOS/Android에서 실행 중인 에이전트 상태 확인·후속 프롬프트 전송. 단, 데스크톱 세션이 살아 있어야 하는 컴패니언 구조다.
- **Design Mode·diff 주석·GitHub/Linear·SSH worktree** 등 검토와 원격 실행을 위한 부가 기능.

## 배경

Y Combinator 지원을 받은 Stably 팀이 개발했고 MIT 라이선스로 완전 오픈소스이며 macOS·Windows·Linux를 지원한다. 팀은 Google Chrome 릴리스 인프라, Uber ML 등의 이력을 배경으로 하고, 별도로 AI 기반 E2E 테스트 제품 Stably도 운영한다. ^[raw/youtube/📺 Orca Is the Free Cursor Killer Nobody's Talking About!.md]

## 한계 (단일 소스, 검증 필요)

YouTube 리뷰 기준: Electron 기반이라 설치 용량·유휴 메모리가 크고, Linux는 AppImage만 제공(.deb/.rpm/Snap/Flatpak 없음), 에이전트 간 순차 파이프라인은 아직 로드맵 단계다. 빠르게 변하는 제품이라 신선도 확인이 필요하다. ^[raw/youtube/📺 Orca Is the Free Cursor Killer Nobody's Talking About!.md]

## 위키 내 위치

Orca는 지식을 저장하는 도구가 아니라 에이전트를 **실행·조율**하는 계층이다. [[knowledge-tool-roles]]가 정리하는 Zotero·NotebookLM·Obsidian 같은 지식 도구와 책임 경계가 다르며, [[llm-wiki]]가 설명하는 "agentic AI를 위한 메모리 레이어"를 소비하는 쪽에 해당한다. 즉 위키는 검증된 장기 지식을 제공하고, Orca 같은 ADE는 그 지식을 활용하는 에이전트를 병렬로 굴린다.

## 열린 질문

- 병렬 에이전트가 공유 지식베이스(LLM Wiki)를 동시에 읽고 쓸 때 provenance와 일관성을 어떻게 유지할 것인가?
- BYO 구독 병렬 실행 시 사용량 급증을 어떤 정책으로 통제할 것인가?
