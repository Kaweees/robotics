---
uuid: <% tp.file.creation_date("YYYYMMDDHHmmss") %>
created-on: <% tp.file.creation_date("YYYY-MM-DDTHH:mm:ss") %>
last-modified-on: <% tp.file.last_modified_date("YYYY-MM-DDTHH:mm:ss") %>
aliases: 
tags:
  - type/timeline/weekly
week: 
startDate: 
endDate: 
status: 📤 Upcoming
related: []
---
## 🎯 Objectives

###  🐉 Personal

- [ ] 
- [ ] 
- [ ] 

### 💼 Work

1. *Determine key objectives for each project*
2. *Assign 10 hours of research to learn something new*

- [ ] 
- [ ] 
- [ ] 


### 🤝 Connections

- [ ] 

## 📝 Notes

- 

## 📌 Pinned

```dataview
TABLE WITHOUT ID link(file.link, aliases[2]) as Day, Pinned
FROM #type/timeline/daily 
WHERE contains(related, [[<% tp.file.title %>]]) AND pinned
SORT file.name
```

## 🗓️ Daily Notes

```dataview
TABLE WITHOUT ID link(file.link, file.aliases[2]) as Date, status as "Status"
FROM #type/timeline/daily
WHERE contains(related, [[<% tp.file.title %>]])
SORT date(file.name) ASC
```

