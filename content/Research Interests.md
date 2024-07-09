---
share: true
---

# Research Interests List
```dataview
TABLE
author as Author,
filter(file.tags, (t) => !contains(t, "#research-interest") AND !contains(t, replace(padleft(author, 1, "#"), " ", "-"))) as Tags
FROM "content/Research Interests"
```
