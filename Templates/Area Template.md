---
type: Area
due: 
archive: false
---

up:: <%tp.file.cursor()%>
## Collections
```dataview
LIST rows.file.link
WHERE archive = false AND contains(up, [[<%tp.file.title%>]])
GROUP BY type
```

## Projects
```dataview
TABLE status AS "Status", due as "Due", notes as "Notes"
FROM [[<%tp.file.title%>]]
WHERE type= "Project" AND archive = false
```
