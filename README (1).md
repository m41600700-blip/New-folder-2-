
# Mini Calendar Using  HTML CSS JS
A mini calendar using HTML, CSS, and JavaScript is a simple web-based calendar component that displays the current month, days, and allows basic navigation (e.g., moving to next/previous months). It’s useful for adding a date display or date-picker functionality to websites, dashboards, or apps.


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Documentation

[Documentation](https://linktodocumentation)


## Appendix
Using Tool
Visiual stodio Code
Create a File
* index.html
* style.css
* script.js

This mini calendar project uses HTML to structure the layout, CSS to style the calendar with a clean, modern look, and JavaScript to dynamically generate the correct days for each month, handle navigation between months, and highlight the current day. It’s a beginner-friendly project to learn DOM manipulation and date handling in JavaScript.

## Related

Here are some related projects

[Awesome README](https://github.com/matiassingers/awesome-readme)


## Usage/Examples

```javascript
let  date=document.getElementById("date")
let  day=document.getElementById("day")
let  month=document.getElementById("month")
let  year=document.getElementById("year")
let today=new Date();
let weeksdays=["Sunday","Monday","Tuesday","Thursday","Friday","Saturday"]
let allmonthes=["january","February","March","April","may","Jun","July","Augest","September","October","November","December"]
 

date.innerHTML=(today.getDate()<10?"0":"")+today.getDate();
day.innerHTML=weeksdays(today.getDay());
month.innerHTML=allmonthes(today.getmonth();) 
year.innerHTML=today.getFullYear();
```

