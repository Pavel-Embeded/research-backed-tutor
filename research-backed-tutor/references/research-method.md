# Research method

Use this reference for a substantial knowledge investigation. The objective is auditable high coverage of important concepts, not a claim to have found every item in an index or on the web.

## Plan the search

Use [investigation-guide.md](investigation-guide.md) to label relationships and [mastery-loop.md](mastery-loop.md) to turn learner questions and failed outputs into research gaps. A search can converge before the teaching and project checks converge; finishing retrieval never authorizes a false mastery claim.

1. Write the learner's question as a concept, its prerequisites, neighboring ideas, applications, and disputed or fast-changing points. Tag each branch `core`, `prerequisite`, `extension`, or `out of scope` and revise the map as evidence arrives.
2. Derive Chinese and English terms, older and newer names, common abbreviations, spelling variants, and searches for contrasts and failure cases. Record the date and the actual query for each source family.
3. Round 1 finds overview and seed sources. Round 2 follows references and cited-by trails, introduces synonyms, and searches missing branches. A final pass targets disagreements and gaps. If a round changes the map, repeat focused searches until the remaining additions are minor or access is exhausted.

## Source tracks

| Track | Discover | Inspect and record |
| --- | --- | --- |
| Papers | CNKI and Google Scholar when accessible; cross-check through publisher pages, DOI, OpenAlex, Crossref, Semantic Scholar, or relevant field indexes | Review/landmark/recent/contrary work; publication status, methods, limitations, and whether full text, abstract, or metadata was actually read |
| GitHub | Repository and file search with relevant terms | README, representative source or examples, tests, recency, license, and what the project really demonstrates; never infer correctness or permission to copy from stars alone |
| CSDN | Site search and targeted web search | Author and date, original versus reposted material, working examples, and agreement with primary sources; use it to expose beginner misconceptions, not as sole proof |
| Textbooks | WorldCat, Google Books, Open Library, publisher catalogs, university syllabi, and accessible chapters | Edition, intended audience, table of contents, covered concepts, and whether only a catalog/preview was available |
| Expert teaching | Original course pages, lectures, interviews, or writing by relevant researchers, textbook authors, or practitioners | Speaker's contribution, exact idea taught, source date, and how the explanation agrees or conflicts with stronger evidence |

For a topic outside software, still check GitHub and CSDN with topic-specific terms and record when they add little. Do not pad the lesson with irrelevant repositories or blogs. Use lawful search or site interfaces; do not bypass paywalls or bulk-collect protected content. Report access limits and index limits.

Keep a distinct log row for named expert teaching. Verify the person's relevant contribution and the specific explanation actually available. If only an anonymous course page or a famous person's unrelated remarks appear, say that no suitable named expert explanation was found; use the course for its content without relabeling it.

## Evidence and integration

Give every retained source a link or stable identifier, publication date when available, source type, accessed material (`full text`, `chapter`, `abstract`, `preview`, `metadata`, or `snippet`), and the concepts it supports. Rank support by directness and quality, not prestige or popularity. Primary papers, established textbooks, and official documentation normally support factual claims better than a blog or project README; an experiment or working artifact can support a specific implementation claim. Compare independent sources for key definitions, derivations, and contested claims. Mark a conclusion as uncertain when evidence conflicts or only secondary summaries are accessible.

Keep a compact working matrix:

| Concept or claim | Priority | Best evidence and access level | Cross-check | Gap or dispute |
| --- | --- | --- | --- | --- |

Keep a query log:

| Round/date | Platform and exact query | Useful results | Excluded results and reason | New concept or gap |
| --- | --- | --- | --- | --- |

Assign parallel tracks clear deliverables: key concepts, annotated sources, query log, access level, contradictory findings, and uncovered branches. The main agent checks cited material before using it, merges duplicates, and resolves inconsistent terminology. Do not equate three agents' agreement with three independent sources if they all repeat the same origin.

The search can stop when a gap-focused pass adds no important branch, correction, or source that changes a core claim. State any inaccessible databases, paywalled texts, uncertain claims, and topic areas still lacking evidence. Never label the search exhaustive or claim to have read material only seen in a result list.
