
```
---tag: dailies---
```

<< [[<% fileDate = moment(tp.file.title, '-MM-YYYY, dddd').subtract(1, 'd').format('YYYY/MMMM/DD-MM-YYYY, dddd') %>|Yesterday]] | [[<% fileDate = moment(tp.file.title, 'YYYY/MMMM/DD-MM-YYYY, dddd').add(1, 'd').format('YYYY/MMMM/DD-MM-YYYY, dddd') %>|Tomorrow]] >>

> [!Quote]+ Quote of the Day  
> <% tp.web.daily_quote() %>

> [!warning]+ OverDue  
> ```tasks  
> not done  
> sort by due date  
> due before <% tp.date.now("YYYY-MM-DD") %>  
> hide due date  
> hide backlink  
> limit 5  
> ```

> [!todo]+ Today's Tasks  
> ```tasks  
> not done  
> due <% tp.date.now("YYYY-MM-DD") %>  
> sort by priority  
> hide due date  
> hide backlink  
> limit 5  
> ```

> [!success]+ Tasks Done Today  
> ```tasks  
> done <% tp.date.now("YYYY-MM-DD") %>  
> hide due date  
> hide backlink

> [!tip]+ Habit Tracker  
> ALX:: 0  
> ExploreAI:: 0  
> Reading:: 0  
> Writing:: 0  

```dataview  
TABLE WITHOUT ID  
file.link as Date,  
choice(ALX > 7, "🟩", "🟥") as 👨🏽‍💻,  
choice(ExploreAI > 30, "🟩", "🟥") as 📈,  
choice(Reading > 30, "🟩", "🟥") as 📚,  
choice(Writing > 750, "🟩", "🟥") as ✍️  
FROM #dailies  
WHERE file.day <= date(now) AND file.day >= date(now) - dur(7days)  
SORT file.day ASC  
```
