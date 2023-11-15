---
type: Resource
archive: false
---
# <%tp.file.title%><%tp.file.move("/3 - Resources/" + tp.file.title)%>
up:: <%tp.file.cursor%>

## Collections
```dataview
LIST rows.file.link
WHERE archive = false AND contains(up, [[<%tp.file.title%>]])
GROUP BY type
```