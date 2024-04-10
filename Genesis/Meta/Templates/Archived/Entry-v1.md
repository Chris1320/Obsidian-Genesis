---
date: <% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>
day: <% moment(tp.file.title, "YYYY-MM-DD").format("dddd") %>
weather: [null]
version: 1
type: entry
---

# Journal Entry for <% moment(tp.file.title, "YYYY-MM-DD").format("Qo of MMMM YYYY") %>

<< [[Entries/<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY") %>/<% moment(tp.file.title, "YYYY-MM-DD").format("MM - MMMM") %>/<% moment(tp.file.title, "YYYY-MM-DD").subtract(1, 'd').format("YYYY-MM-DD") %>E|Previous]] | [[<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>E]] | [[Entries/<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY") %>/<% moment(tp.file.title, "YYYY-MM-DD").format("MM - MMMM") %>/<% moment(tp.file.title, "YYYY-MM-DD").add(1, 'd').format("YYYY-MM-DD") %>E|Next]] >>

## Notes

```dataview
TABLE time AS Time
FROM "Entries/<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY") %>/<% moment(tp.file.title, "YYYY-MM-DD").format("MM - MMMM") %>/<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>/Notes"
SORT file.name ASCENDING
```

## Dreams

```dataview
TABLE time AS Time
FROM "Entries/<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY") %>/<% moment(tp.file.title, "YYYY-MM-DD").format("MM - MMMM") %>/<% moment(tp.file.title, "YYYY-MM-DD").format("YYYY-MM-DD") %>/Dreams"
SORT file.name ASCENDING
```
