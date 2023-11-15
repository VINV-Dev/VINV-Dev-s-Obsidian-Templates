---
type: Quarterly
archive: false
---

# <%tp.file.title%><%tp.file.move("/Periodic/" + tp.file.title.slice(0,4) + "/" + tp.file.title)%>

[[<%tp.date.now("YYYY-[Q]Q", - 1, tp.file.title, "YYYY-[Q]Q")%>|<---Prev]]|--------|[[<%tp.date.now("YYYY-[Q]Q", +93, tp.file.title, "YYYY-[Q]|Next--->Q")%>]]
up:: [[<%tp.date.now("YYYY", +0, tp.file.title, "YYYY-[Q]Q")%>]]
---

## Highlights

<%tp.file.cursor()%>

## Months Summary

```dataview
LIST rows.item.text
FLATTEN file.lists AS item
WHERE contains(up, [[<%tp.file.title%>]]) AND meta(item.section).subpath = "Highlights"
GROUP BY file.section
```

## R

## Consumed Media

```dataview
LIST rows.file.link
FROM "Sources"
WHERE contains(file.outlinks.up.up.up, [[<%tp.file.title%>]]) AND finished
GROUP BY type
```
