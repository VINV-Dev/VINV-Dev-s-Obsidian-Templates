---
type: Yearly
archive: false
---

# <%tp.file.title%><%tp.file.move("/Periodic/" + tp.file.title.slice(0,4) + "/" + tp.file.title)%>

[[<%tp.date.now("YYYY", -1, tp.file.title, "YYYY")%><---Prev]]|--------|[[<%tp.date.now("YYYY", +366, tp.file.title, "YYYY")%>|Next--->]]
---

## Highlights

<%tp.file.cursor()%>

## Quarters  Summary

```dataview
LIST rows.item.text
FLATTEN file.lists AS item
WHERE contains(up, [[<%tp.file.title%>]]) AND meta(item.section).subpath = "Highlights"
GROUP BY item.section
```
