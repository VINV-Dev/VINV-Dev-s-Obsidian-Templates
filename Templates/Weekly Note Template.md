---
type: Weekly
archive: false
---

# <%tp.file.title%><%tp.file.move("/Periodic/" + tp.file.title.slice(0,4) + "/" + tp.file.title)%>

[[<% tp.date.now("YYYY-[W]ww", -7, tp.file.title, "YYYY-[W]ww") %>|<---Prev]]|-----------|[[<% tp.date.now("YYYY-[W]ww", +7, tp.file.title, "YYYY-[W]ww") %>|Next--->]]
up:: [[<% tp.date.now("YYYY-MM", +0, tp.file.title, "YYYY-[W]ww") %>]]
---

## Highlights

<%tp.file.cursor()%>

## Days Summary

```dataview
LIST rows.item.text
FLATTEN file.lists AS item
WHERE contains(up, [[<%tp.file.title%>]]) AND meta(item.section).subpath = "Highlights"
GROUP BY item.section
```

## Related to this week

```dataview
LIST rows.file.link
FROM !"Periodic"
WHERE contains(file.outlinks.up, [[<%tp.file.title%>]])
GROUP BY type
```
