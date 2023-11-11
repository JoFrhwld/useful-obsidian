## Requires 
- Templater, with
  - the option of running templater on new note creation
- Your daily note title formatted as `YYYY-MM-DD`

(These backticks are here just to make the github formatting nice)
```
<%*
let fileDate = moment(tp.file.title, 'YYYY-MM-DD').format('YYYY-MM-DD')
let month = moment(fileDate).format("MM")
let fall_months = ["08", "09", "10", "11", "12"]
let spring_months = ["01", "02", "03", "04", "05"]
let summer_months = ["06", "07"]
let semester_url = "01_Periodic/02_Semesterly/"
if (fall_months.includes(month)){
  semester_url += moment(fileDate).format("YYYY") + 
    "-" + 
    moment(fileDate).add(1, "years").format("YY") + 
    " 1 F"
}
if (spring_months.includes(month)){
  semester_url += moment(fileDate).subtract(1, "years").format("YYYY") + 
    "-" + 
    moment(fileDate).format("YY") + 
    " 2 S"
}
if (summer_months.includes(month)){
  semester_url += moment(fileDate).format("YYYY") + 
    "-" + 
    moment(fileDate).add(1, "years").format("YY") + 
    " 0 Summer"
}
%>
```
semesterly-note:: [[<% semester_url%>|Semester]]

