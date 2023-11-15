---
type: Daily
archive: false
---

# <%tp.file.title%>

<%tp.file.move("/Periodic/" + tp.file.title.slice(0,4) + "/" + tp.file.title)%>[[<%tp.date.now("YYYY-MM-DD",-1,tp.file.title,"YYYY-MM-DD")%>|<--- Prev>]] | ------- | [[<%tp.date.now("YYYY-MM-DD",+1,tp.file.title,"YYYY-MM-DD")%>|Next --->]]

up:: [[<%tp.date.now("YYYY-[W]WW", +0, tp.file.title, "YYYY-MM-DD")%>]]

## Highlights

## Journal

<%tp.file.cursor()%>
---

## Related to this day

```dataview
LIST rows.file.link
FROM !"Periodic"
FROM [[<%tp.file.title%>]]
GROUP BY type
```
