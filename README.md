<div align="center">

# Gnosis

### Scripture · Context · Understanding

**A full-stack Bible study platform for exploring Scripture, historical commentary, and biblical languages.**

[**Explore the Live App ↗**](https://studygnosis.com) · [**Developer Profile**](https://github.com/yoni871)

React · Vite · Node.js · Express · PostgreSQL · Vercel · Neon

</div>

---

## The product

Bible study often means moving between a Bible reader, historical commentary, language references, and personal notes. **Gnosis brings these tools into one focused reading experience**, designed to help readers move between the biblical text and its context without losing their place.

> **Live demo:** [studygnosis.com](https://studygnosis.com)

<!-- Add an actual desktop screenshot here after exporting it from Gnosis.
![Gnosis reader with Scripture and commentary side by side](assets/reader-desktop.png)
-->

## What Gnosis does

| Capability | Experience |
| --- | --- |
| **Scripture reader** | Navigate books, chapters, and verses, with multi-verse selection and responsive reading layouts. |
| **Historical commentary** | Explore integrated commentaries alongside biblical passages. |
| **Original-language study** | Inspect word-level Hebrew and Greek information in the currently supported passages. |
| **Search** | Find passages and explore paginated results. |
| **Personal study** | Save bookmarks, highlights, notes, and reading progress. |
| **Translations** | Use supported texts and licensed providers where authorized. |

### A closer look

This showcase is ready for three authentic screenshots:

1. **Reader and commentary** — the primary desktop study view.
2. **Original Language Analysis** — the word-analysis modal in a supported passage.
3. **Mobile experience** — navigation and reading on a narrow screen.

Screenshots will be added without exposing source code, user data, or private configuration.

## Engineering overview

Gnosis is designed as a full-stack web application with distinct presentation, application, and persistence layers.

```text
Browser
   │
   ▼
React + Vite frontend
   │  REST requests
   ▼
Node.js + Express backend
   │
   ▼
PostgreSQL (Neon)
   │
   ├── Scripture and translation content
   ├── Commentaries and verse-range associations
   ├── Original-language reference data
   └── User study records and sessions
```

**Selected engineering work**

- **Relational modeling:** connected Bible books, chapters, verses, commentaries, verse ranges, and user study records with migrations and integrity checks.
- **Content ingestion:** built repeatable import processes for large biblical commentary datasets while preserving source structure and mapping commentary to Scripture.
- **Authentication:** implemented access-token renewal, rotating refresh-token sessions, and logout/revocation behavior.
- **Performance:** introduced route-level lazy loading, optimized images, caching controls, and paginated search.
- **Reliability:** used automated frontend, backend, importer, and PostgreSQL migration tests in GitHub Actions.

## Development approach

`Feature branch → Pull request → Automated checks → Main integration → Preview verification → Production release`

Changes are validated in stages before production promotion. The live product and the codebase are managed separately from this public presentation repository.

## Current direction

- **Available:** Scripture reader, commentary, search, personalized study tools, and initial original-language analysis.
- **In development:** Full-canon original-language coverage, including Biblical Aramaic and cross-book word-occurrence navigation.
- **Planned:** Hymn exploration and historical context.

## Project details

**Creator:** Yonatan Demissie  
**Background:** B.S. Computer Science, Texas Tech University  
**Focus:** Full-stack software engineering, relational data systems, and human-centered product design.

Gnosis is a personal software engineering project built at the intersection of biblical studies and modern web development.

---

<div align="center">

**[Visit Gnosis →](https://studygnosis.com)**

*This repository is a public project showcase. The application's source code is maintained separately and is not distributed here.*

</div>
