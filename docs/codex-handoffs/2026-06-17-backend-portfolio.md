# Backend Portfolio Handoff

## Context

- Branch: `feat/backend-portfolio-pr-log`
- Site target: GitHub Pages static `index.html`
- Visual sources used:
  - Pull Request Portfolio concept: `/Users/iamxoghks/.codex/generated_images/019ed16b-4f15-70b0-aa5b-6bf75031f63f/ig_01e3b9e46f3bd59e016a3188c45df48191a226cfc602f97465.png`
  - Build Log concept: `/Users/iamxoghks/.codex/generated_images/019ed16b-4f15-70b0-aa5b-6bf75031f63f/ig_01e3b9e46f3bd59e016a3189b428a081919f7b78260ff66faf.png`
  - Runtime Field Terminal concept: `/Users/iamxoghks/.codex/generated_images/019ed16b-4f15-70b0-aa5b-6bf75031f63f/ig_026a26535d212cba016a31d5f8df9881919958dd1f35f8dfa1.png`

## Implemented Direction

- Reworked the site to follow the Runtime Field Terminal direction.
- Removed the green forest/photo background after user feedback.
- First screen now starts from the terminal window itself:
  - prompt bar and runtime status
  - 김태환 / iamxoghks identity
  - stack grid with local SVG icons
  - active objectives
  - terminal tabs for Terminal, Runtime Node, API Surface, Build Log
  - project nodes, vibe coding work, metrics, ask runtime, progress bar
- Removed the visible outer terminal border after user feedback; internal elements remain angular/square.
- Removed outer page background effects, page padding, shell radius, shell shadow, and shell backdrop filter so the viewport starts directly as the terminal surface.
- Removed duplicated lower notes and footer link repetition.
- Reworked Build Log tab to show build/process checks instead of repeating project names.
- Replaced the separated footer row with plain `made by Codex` text at the bottom of the terminal flow.
- Refreshed portfolio copy from GitHub profile/repository data read on 2026-06-17:
  - GitHub profile public repo count
  - TanTan README: map-based gym discovery, JWT/Spring Security, Redis, Elasticsearch, WebSocket optimization
  - Atlas README: SCM order/inventory/shipment/return/settlement flow, API Gateway, service split, Redis/Elasticsearch/Kafka
  - MHiT README: baseball ticketing plus shuttle reservation DB project, ERD, SQL query/procedure validation
  - Vibe work README summaries for Noa Sudoku, codex-receipts, tufte-viz-codex, valentine-memory
- Polished portfolio content so the terminal metaphor reads as an evidence console rather than a fake runtime:
  - removed fake timestamps, `Internal Node Address`, `Ask Runtime`, `README indexing`, `fresh/running` style labels
  - changed tabs to Overview, Architecture, API / Data, Decision Log
  - shifted lower content toward review focus, architecture decisions, API/data surfaces, and system-design evidence
- Applied browser-comment cleanup after the terminal redesign:
  - removed duplicated `Portfolio Target` / `Source Profile` endpoint boxes from the overview
  - changed the top right summary from generic backend signals to project-specific backend work for TanTan, Atlas, and MHiT
  - changed the stack area from boxed cards to a terminal-style icon list with only line separators
  - renamed the top status label from `Backend Evidence Console` to `Backend Portfolio`
  - reduced bottom metrics to clearer portfolio facts: public repos, backend projects, main contribution, project domains
  - removed the duplicated `Review Focus` action block
  - kept the progress-bar UI but changed its caption to the key review axes
- Applied typography and stack update:
  - switched site typography to Pretendard and removed the top runtime status dot
  - increased UI text sizes slightly across terminal header, body copy, stack rows, logs, side rows, metrics, and footer
  - expanded the Stack section from 6 items to 14 TanTan/Atlas-backed backend technologies
  - added local SVG icons for security, JWT, JPA, WebSocket/STOMP, gateway, OpenAPI, Docker/Kubernetes, and S3/File Service
  - grouped Stack items by README-style categories: Backend, Data, Event / Realtime, Infra / Docs
- Combined Notion profile content via `ntn pages get a7c661f3bf90411985841425c9082a85`:
  - added VARO edtech/metaverse startup experience without exposing birth date, phone number, or personal contact details
  - reflected Java/Spring edtech platform, Janus streaming, whiteboard, WebSocket chat, and Nginx proxy experience
  - added Nginx to the Infra / Docs stack group and updated overview metrics/progress text with work experience/domain range

## QA Notes

- Local preview: `python3 -m http.server 4174`
- In-app browser checked:
  - desktop viewport `1440 x 1024`
  - mobile viewport `390 x 844`
- Verified:
  - desktop `scrollWidth === 1440`
  - mobile `scrollWidth === 390`
  - background CSS no longer references image URLs
  - stack icons load from local `assets/icons/*.svg`
  - API Surface tab click updates selected state
  - outer shell border width is `0px`
  - outer shell radius is `0px`, shadow is `none`, page padding is `0px`
  - body pseudo backgrounds are disabled with `content: none`
  - stack items, command buttons, tags, and progress segments use `0px` corner radius
  - Decision Log tab no longer repeats project names
  - no `footer` element remains; `made by Codex` is plain bottom text via `.panel-credit`
- Portfolio copy avoids fake runtime status and uses backend evidence-oriented labels.
- Latest requested cleanup verified:
  - no duplicate `Portfolio Target` / `Source Profile` strings should remain
  - stack items should remain unboxed
  - progress caption should read as a backend review axis, not a generic portfolio scope
- Latest typography/stack cleanup verified:
  - Stack shows 14 non-duplicative items, with 3 columns on desktop, 2 columns around 819px, and 1 column on narrow mobile
  - added SVG icons parse successfully and load without broken images
  - increased text sizes do not introduce horizontal overflow at 1440px, 819px, or 390px
- Latest stack grouping cleanup verified:
  - stack headings show `Backend / 5`, `Data / 3`, `Event / Realtime / 2`, and `Infra / Docs / 4`
  - grouped stack remains unboxed and uses terminal-style separators
  - no horizontal overflow or clipped stack labels at 819px or 390px

## Resume Prompt

Continue polishing `/Users/iamxoghks/Documents/GitHub/iamxoghks.github.io` on branch `feat/backend-portfolio-pr-log`. Preserve the terminal-first Backend Portfolio direction, keep stack icons loaded from local SVG assets, keep the expanded stack unboxed and non-duplicative, keep the bottom credit as plain text rather than a divided footer row, and verify with Codex in-app browser before handoff.
