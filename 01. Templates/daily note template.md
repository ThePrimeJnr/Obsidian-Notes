tag: #dailies  

<< [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD').subtract(1, 'd').format('YYYY-MM-DD') %>|Yesterday]] | [[<% fileDate = moment(tp.file.title, 'YYYY-MM-DD').add(1, 'd').format('YYYY-MM-DD') %>|Tomorrow]] >>

> [!Quote]+ Quote of the Day  
> <% tp.web.daily_quote() %>


```dataview  
TABLE WITHOUT ID  
file.link as Date,  
choice(Sleep > 7, "🟩", "🟥") as 🛌,  
choice(Exercise > 30, "🟩", "🟥") as 🏃,  
choice(Reading > 30, "🟩", "🟥") as 📚,  
choice(Meditation > 10, "🟩", "🟥") as 🧘,  
choice(Writing > 750, "🟩", "🟥") as ✍️FROM #dailiesWHERE file.day <= date(now) AND file.day >= date(now) - dur(7days)  
SORT file.day ASC  
```

> [!tip]+ Habit Tracker  
> Sleep:: 0  
> Reading:: 0  
> Exercise:: 0  
> Meditation:: 0  
> Writing:: 0

```dataview  
TABLE WITHOUT ID  
file.link as Date,  
choice(Sleep > 7, "🟩", "🟥") as 🛌,  
choice(Exercise > 30, "🟩", "🟥") as 🏃,  
choice(Reading > 30, "🟩", "🟥") as 📚,  
choice(Meditation > 10, "🟩", "🟥") as 🧘,  
choice(Writing > 750, "🟩", "🟥") as ✍️FROM #dailiesWHERE file.day <= date(now) AND file.day >= date(now) - dur(7days)  
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


