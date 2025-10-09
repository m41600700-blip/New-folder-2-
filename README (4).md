
# Stopwatch using HTML CSS JS

The HTML provides the structure of the stopwatch interface. It includes:

* A heading to display the time (00:00:00)

* Three buttons: Start, Stop, and Reset


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Documentation

[Documentation](https://linktodocumentation)


## Features

- Start button
- Start button
- Fullscreen mode
- Reset button


## Related

Here are some related projects

[Awesome README](https://github.com/matiassingers/awesome-readme)


## Usage/Examples

```javascript
  function watchstart(){
            if(timer!==null){  
                clearInterval(timer);
            }
            timer= setInterval(stopwatch,1000)
        }
        clearInterval(timer)
        function watchstop(){
             clearInterval(timer);
        }
         function watchreset(){
            clearInterval(timer);
             [second, minutes, hour]=[0,0,0];
              displaytime.innerHTML="00:00:00"

        }
}
```


## Demo

Download Image: https://drive.google.com/file/d/1iSB_aTrE5-IxmKzcMZlIyp0AvrO4zHpc/view?usp=share_link


## Appendix

Key Concepts:

* setInterval() runs a function every 10 milliseconds (for milliseconds counting).

* Time is calculated using variables for minutes, seconds, and milliseconds.

* clearInterval() stops the timer when needed.

* Button clicks trigger functions to start, stop, or reset the stopwatch.


## Feedback

If you have any feedback, please reach out to us at fake@fake.com

