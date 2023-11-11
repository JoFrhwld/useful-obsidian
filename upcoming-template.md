---
date: 
due:
done: false
---

## Requirements
- The dataview plugin
- Your daily note has a `date` frontmatter field

Any note with a `due:` date in the front matter will appear. 
If there's a `done:` field, the note will not appear after it's set to `true`

## Upcoming
```dataview
table 
  due, 
  due - date(this.file.frontmatter.date) as "days"
where due and date(due) > date(this.file.frontmatter.date) and !done
sort date(due) asc
```
