---
type: Source
medium: <%tp.file.cursor(1)%>
archive: false
---
# <%tp.file.title,%>
<%tp.file.move("/Sources/" + tp.file.title)%>
**LINK**: <%tp.file.cursor(2)%>
created:: [[<%tp.date.now("YYYY-MM-DD")%>]]]
finished:: 
creator:: <%tp.file.cursor(3)%>
up:: 
keywords:: 

## Takeaways

---

## Highlights
<%tp.file.cursor(4)%>

## Related Notes
```dataview
LIST rows.file.link
WHERE contains(file.outlinks, [[<%tp.file.title%>]])
GROUP BY type
```
