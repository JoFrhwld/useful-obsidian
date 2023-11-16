#weekly

See the [daily template](daily-template.md) for explanation

## Planning

## Daily Summary

The source statement ensures that only notes tagged 
#daily *and* link to this weekly note get included in the table, meaning

- Not *every* daily note gets pulled in
- I can link to this weekly note from other notes without filling up the table

```dataview
table dateformat(date, "EEE") as day, did
from #daily and [[]]
sort date asc
```

