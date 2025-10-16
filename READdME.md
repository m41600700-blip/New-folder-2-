
# QR Code Generator Website Using HTML CSS And JavaScript

🧾 Project Description: QR Code Generator Website Using HTML, CSS & JavaScript

Create a QR Code Generator Website using HTML, CSS, and JavaScript that allows users to easily generate QR codes for any text or URL. This project uses simple front-end technologies and demonstrates how to integrate a QR code generation library (like qrcode.js) with a clean and responsive user interface.

Users can type or paste any text or link into the input box, click the “Generate QR Code” button, and instantly see a scannable QR code appear on the screen. The website also provides a download option to save the QR code as an image file.

This project is perfect for beginners who want to practice DOM manipulation, event handling, and API/library integration in JavaScript, while also improving their front-end design skills with CSS.


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Appendix

🔍 Additional Information

This QR Code Generator Website is a simple yet powerful web tool that helps users create unique QR codes instantly. It is built using HTML for structure, CSS for styling, and JavaScript for functionality — making it a great beginner-friendly project to understand how web technologies work together.

The project utilizes a lightweight JavaScript library such as qrcode.js to generate the QR code dynamically in the browser. Users can enter any text, link, phone number, or message, and with one click, a QR code will be generated instantly.

You can also customize the design by adjusting background color, text color, or adding an animation to make the interface more engaging. The generated QR code can be downloaded as a PNG image, making it practical for real-world use — like sharing URLs, contact info, or Wi-Fi credentials.


## Features

✨ Features:

* Generate QR codes for any text, link, or data

* Instant live preview

* Download QR code as an image (PNG)

* Fully responsive and modern UI

* Built with pure HTML, CSS, and JavaScript


## Usage/Examples

```javascript
let imgbox=document.getElementById("imgbox")
    let qrimage=document.getElementById("qrimage")
    let qrtext=document.getElementById("qrtext")
    function GenreateQR(){
        if(qrtext.value.length>0){
            qrimage.src="https://api.qrserver.com/v1/create-qr-code/?size=150x150&data="+qrtext.value; 
            imgbox.classList.add("show-img")
        }else{
            qrtext.classList.add("error")
            setTimeout(()=>{
                qrtext.classList.remove("error")
            },1000)
        }
      
    }
}
```


## Lessons Learned

💡 Learning Outcomes:

* Understand how QR codes work and how to generate them dynamically

* Learn to handle user input and display dynamic content with JavaScript

* Practice front-end layout and responsive design

## Optimizations

🧠 Key Concepts Covered

* DOM manipulation and event handling in JavaScript

* Using external libraries (qrcode.js)

* Implementing image download functionality using canvas.toDataURL()

* Responsive design with CSS

* Front-end user interaction and validation

🛠️ Tools & Technologies

* HTML5 – Page structure and input form

* CSS3 – Styling and responsiveness

* JavaScript (ES6) – Logic and interactivity

* qrcode.js (or similar library) – QR code generation

