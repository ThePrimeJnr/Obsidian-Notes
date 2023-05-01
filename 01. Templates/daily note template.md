---
tag: dailies  
---

## <% moment(tp.file.title, "YYYY-MM-DD").format("dddd Do MMMM YYYY") %>

<< [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD').subtract(1, 'd').format('YYYY-MM-DD') %>|Yesterday]] | [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD').add(1, 'd').format('YYYY-MM-DD') %>|Tomorrow]] >>

<% tp.web.daily_quote() %>

> [!Quote]+ Quote of the Day  
> <% tp.web.daily_quote() %>

