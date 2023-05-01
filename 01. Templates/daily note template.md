
```
---tag: dailies---
```

<< [[<% fileDate = moment(tp.file.title, 'DD-MM-YYYY, dddd').subtract(1, 'd').format('DD-MM-YYYY, dddd') %>|Yesterday]] | [[<% fileDate = moment(tp.file.title, 'YYYY/MMMM/DD-MM-YYYY, dddd').add(1, 'd').format('YYYY/MMMM/DD-MM-YYYY, dddd') %>|Tomorrow]] >>

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

> [!Warning]+ Unscheduled Tasks  
> ```tasks  
> not done  
> no due date

> [!success]+ Tasks Done Today  
> ```tasks  
> done <% tp.date.now("YYYY-MM-DD") %>  
> hide due date  
> hide backlink

> [!tip]+ Habit Tracker  
> Sleep:: 0  
> Reading:: 0  
> Exercise:: 0  
> Meditation:: 0  
> Writing::

```dataview  
TABLE WITHOUT ID  
file.link as Date,  
choice(Sleep > 7, "🟩", "🟥") as 🛌,  
choice(Exercise > 30, "🟩", "🟥") as 🏃,  
choice(Reading > 30, "🟩", "🟥") as 📚,  
choice(Meditation > 10, "🟩", "🟥") as 🧘,  
choice(Writing > 750, "🟩", "🟥") as ✍️  
FROM #dailies  
WHERE file.day <= date(now) AND file.day >= date(now) - dur(7days)  
SORT file.day ASC  
```

> [!abstract]+ What am I grateful for?  
> - 1  
> - 2  
> - 3
 
>[!Important]+ Highlights of the Day  
>- 1  
>- 2  
>- 3


