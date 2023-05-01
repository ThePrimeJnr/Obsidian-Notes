<< [[00. Daily Notes/<% fileDate = moment(tp.file.title, 'DD-MM-YYYY, dddd').subtract(1, 'd').format('YYYY/MMMM/DD-MM-YYYY, dddd') %>|Yesterday]] | [[00. Daily Notes/<% fileDate = moment(tp.file.title, 'DD-MM-YYYY, dddd').add(1, 'd').format('YYYY/MMMM/DD-MM-YYYY, dddd') %>|Tomorrow]] >>

> [!Quote]+ Quote of the Day  
> <% tp.web.daily_quote() %>

> [!warning]+ OverDue  
> ```tasks  
> not done  
> sort by priority 
> sort by due date  
> due before <% tp.date.now("YYYY-MM-DD") %>  
> hide backlink  
> limit 5  
> ```

> [!todo]+ Today's Tasks  
> ```tasks  
> not done  
> due after <% tp.date.yesterday("YYYY-MM-DD") %>  
> sort by priority 
> sort by due date   
> hide due date  
> hide backlink  
> limit 5  
> ```

> [!success]+ Completed Tasks  
> ```tasks  
> done <% tp.date.now("YYYY-MM-DD") %>  
> hide due date  
> hide backlink

## TODOs
- [ ] *