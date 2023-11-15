---
type: Monthly
archive: false
---

# <%tp.file.title%><%tp.file.move("/Periodic/" + tp.file.title.slice(0,4) + "/" + tp.file.title)%>

[[<%tp.date.now("YYYY-MM", -1, tp.file.title, "YYYY-MM")%>|<---Prev]]|--------|[[<%tp.date.now("YYYY-MM", +32, tp.file.title, "YYYY-MM")%>|Next--->]]

up:: [[<%tp.date.now("YYYY-[Q]Q", +0, tp.file.title, "YYYY-MM")%>]]

## Highlights

<%tp.file.cursor(%>)

## Weeks Summary

```dataview
LIST rows.item.text
FLATTEN file.lists AS item
WHERE contains(up, [[<%tp.file.title%>]]) AND meta(item.section).subpath = "Highlights"
GROUP BY file.section
```

## Related to this Month

```dataview
LIST rows.file.link
FROM !"Periodic"
WHERE contains(file.outlinks.up, [[<%tp.file.title%>]])
GROUP BY type
```
