#  Background Change Effect On Website Using HTML CSS and JavaScript

This feature allows you to change the background image of your webpage either manually (on button click) or automatically (after a time delay) using a combination of HTML, CSS, and JavaScript.

✅ 1. HTML – Structure the Web Page

* You start by writing simple HTML to create a basic layout. This includes:

* The page body

* A container with a heading

* A button (or other UI element) to trigger the background image change

## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Demo

* [link](https://drive.google.com/file/d/117Al-37ztHIBmnudGL_IwWH2Zv1cXxYm/view?usp)


## Usage/Examples

```javascript
let imgbox=document.querySelector(".img-box") 
let imgwrap=document.querySelector(".img-wrap")
let originalimg=document.getElementById("originalimg")
let line=document.getElementById("line")
originalimg.style.width=imgbox.offsetWidth+"px" 
let leftspace= imgbox.offsetLeft;
imgbox.onmousemove=function(e){
   let boxwidth= e.pageX-leftspace+"px";
   imgwrap.style.width=boxwidth;
   line.style.left=boxwidth

}



```


## Appendix
🌐 Overview: Background Image Change Effect (HTML + CSS + JavaScript)
🎯 Goal:

Create a website where the background image changes dynamically — either when a user clicks a button or automatically over time.




## Lessons Learned

Creating a "Change Background Image" feature using HTML, CSS, and JavaScript helps you learn and apply several important web development concepts. Here are the key lessons learned from building such a project:
✅ Lessons Learned
1. 🧱 HTML Structure Basics

* You learn how to structure a web page using elements like <body>, <button>, <div>, etc.

* Practice linking external CSS and JavaScript files properly using <link> and <script> tags.

