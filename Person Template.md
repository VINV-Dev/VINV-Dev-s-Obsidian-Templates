---
type: Person
personal: <%tp.file.cursor(1)%>
mentor: <%tp.file.cursor(2)%>
archive: false
---
# <%tp.file.title%><%tp.file.move("/People/" + tp.file.title)%>
keywords:: 

<%tp.file.cursor(3)%>
## Summary
```dataview
LIST rows.item.text
FLATTEN file.lists AS item
WHERE contains(item.outlinks, [[<%tp.file.title%>]])
GROUP BY file.link
```
## Zettel Mentions
```dataview
LIST file.links
FROM "Zettelkasten"
WHERE contains(file.outlinks, [[<%tp.file.title%>]])
SORT file.name asc
```

## Created COntent
```dataview
LIST rows.file.link
FROM "Sources"
WHERE contains(creator, [[<%tp.file.title%>]])
GROUP BY medium
```
