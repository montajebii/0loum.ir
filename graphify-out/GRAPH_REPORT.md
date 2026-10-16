# Graph Report - Khanepaye-oloom.github.io  (2026-09-03)

## Corpus Check
- 7 files · ~14,565 words
- Verdict: corpus is large enough that graph structure adds value.

## Summary
- 40 nodes · 38 edges · 8 communities (7 shown, 1 thin omitted)
- Extraction: 100% EXTRACTED · 0% INFERRED · 0% AMBIGUOUS
- Token cost: 0 input · 0 output

## Graph Freshness
- Built from commit: `f1a0befa`
- Run `git rev-parse HEAD` and compare to check if the graph is stale.
- Run `graphify update .` after code changes (no API cost).

## Community Hubs (Navigation)
- package.json
- Library Auto-Generation Workflow
- generate-library.js
- main.js
- keywords
- generateLibrary
- نحوه کار
- CLAUDE.md

## God Nodes (most connected - your core abstractions)
1. `Library Auto-Generation Workflow` - 8 edges
2. `keywords` - 4 edges
3. `generateLibrary()` - 3 edges
4. `main()` - 3 edges
5. `نحوه کار` - 3 edges
6. `scripts` - 2 edges
7. `parseFilename()` - 2 edges
8. `mergeLibraries()` - 2 edges
9. `toggleBtn` - 1 edges
10. `panel` - 1 edges

## Surprising Connections (you probably didn't know these)
- None detected - all connections are within the same source files.

## Import Cycles
- None detected.

## Communities (8 total, 1 thin omitted)

### Community 0 - "package.json"
Cohesion: 0.25
Nodes (7): author, description, license, name, scripts, generate-library, version

### Community 1 - "Library Auto-Generation Workflow"
Cohesion: 0.25
Nodes (7): Library Auto-Generation Workflow, ساختار library.json, ساختار پوشه downloads/, فایل‌های مربوطه, قوانین نامگذاری فایل, مثال اجرای دستی, نکات مهم

### Community 2 - "generate-library.js"
Cohesion: 0.29
Nodes (6): DOWNLOADS_DIR, fs, GRADE_NAMES, OUTPUT_FILE, path, SUBJECT_MAPPING

### Community 3 - "main.js"
Cohesion: 0.50
Nodes (3): closeBtn, panel, toggleBtn

### Community 4 - "keywords"
Cohesion: 0.50
Nodes (4): keywords, education, library, science

### Community 5 - "generateLibrary"
Cohesion: 0.50
Nodes (4): generateLibrary(), main(), mergeLibraries(), parseFilename()

### Community 6 - "نحوه کار"
Cohesion: 0.67
Nodes (3): 1. **Workflow خودکار (GitHub Actions)**, 2. **اجرای دستی**, نحوه کار

## Knowledge Gaps
- **27 isolated node(s):** `toggleBtn`, `panel`, `closeBtn`, `name`, `version` (+22 more)
  These have ≤1 connection - possible missing edges or undocumented components.
- **1 thin communities (<3 nodes) omitted from report** — run `graphify query` to explore isolated nodes.

## Suggested Questions
_Questions this graph is uniquely positioned to answer:_

- **Why does `Library Auto-Generation Workflow` connect `Library Auto-Generation Workflow` to `نحوه کار`?**
  _High betweenness centrality (0.057) - this node is a cross-community bridge._
- **Why does `keywords` connect `keywords` to `package.json`?**
  _High betweenness centrality (0.036) - this node is a cross-community bridge._
- **Why does `نحوه کار` connect `نحوه کار` to `Library Auto-Generation Workflow`?**
  _High betweenness centrality (0.023) - this node is a cross-community bridge._
- **What connects `toggleBtn`, `panel`, `closeBtn` to the rest of the system?**
  _27 weakly-connected nodes found - possible documentation gaps or missing edges._