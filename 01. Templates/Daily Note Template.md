Tags: #Daily-Notes
<< [[00. Daily Notes/<% fileDate = moment(tp.file.title, 'DD-MM-YYYY, dddd').subtract(1, 'd').format('YYYY/MMMM/DD-MM-YYYY, dddd') %>|Yesterday]] | [[00. Daily Notes/<% fileDate = moment(tp.file.title, 'DD-MM-YYYY, dddd').add(1, 'd').format('YYYY/MMMM/DD-MM-YYYY, dddd') %>|Tomorrow]] >>

> [!Quote]+ Quote of the Day  
> <% tp.web.daily_quote() %>

> [!warning]+ OverDue  
> ```tasks  
> not done  
> sort by priority 
> sort by due date  
> due before <% tp.date.now("YYYY-MM-DD") %>  
> limit 5  
> ```

> [!todo]+ Today's Tasks  
> ```tasks  
> not done  
> due after <% tp.date.yesterday("YYYY-MM-DD") %>  
> sort by due date   
> sort by priority 
> hide due date  
> limit 5  
> ```

> [!success]+ Tasks Completed Today  
> ```tasks  
> done <% tp.date.now("YYYY-MM-DD") %>  
> hide due date  

## Morning Routines:
- [ ] Check and Attend to Urgent Emails
- [ ] Confirm Meetings on Calendar
- [ ] Review Projects and Assignments for the Day
- [ ] Engage on Social Media (Twitter, WhatsApp, LinkedIn)
- [ ] Plan and Set Tasks for the Day

## Meetings:
- [ ] *

## To-dos:
- [ ] *
