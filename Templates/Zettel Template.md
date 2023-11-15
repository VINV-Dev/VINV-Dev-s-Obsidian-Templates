---
type: Zettel
archive: false
---

# <%tp.file.title%>

up:: <%tp.file.cursor(1)%>
created:: [[<%tp.date.now("YYYY-MM-DD")%>]]
source:: <%tp.file.move("/Zettelkasten/" + tp.file.title)%><%tp.file.cursor(2)%>
---

<%tp.file.cursor(3)%>

---

## Related Links

### Descendants

```breadcrumbs
type: tree
dir: down
```

## Relationships

```dataview
LIST replace(rows.item.text, "]]", "|This Note]]")
FLATTEN file.lists AS item
WHERE contains(item.outlinks, [[<%tp.file.title%>]])
GROUP BY file.link
```

### Related Links

```dataview
LIST rows.file.link
FROM !"Zettelkasten"
FROM [[<%tp.file.title%>]]
GROUP BY type
```
