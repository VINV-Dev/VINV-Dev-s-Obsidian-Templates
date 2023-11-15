---
type: Project
up: 
due: 
priority: 
archive: false
---
# <%tp.file.title,%>
<%tp.file.move("1 - Projects/" + tp.file.title)%>

up:: 

## Purpose


## Brainstorming


## Barinstorming


## Roadmap


## Next steps


## References & Resources
```dataview
LIST rows.file.link
WHERE archive = false AND contains(up, [[<%tp.file.title%>]])
GROUP BY type
```