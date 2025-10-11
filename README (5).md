
#  Working Email Subscription Form With Google Sheets Using HTML CSS & JavaScript


We’ll use Google Apps Script to connect your form to Google Sheets, allowing every submitted email address to be stored instantly. This is a perfect beginner-friendly project for web developers who want to collect email subscribers for newsletters, websites, or landing pages — completely free and easy to set up.
By the end of this tutorial, you’ll have a working email subscription system powered by Google Sheets, without needing PHP, Node.js, or any external services.


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Appendix

📘 Additional Information

This project shows how to create a simple yet powerful email subscription system using HTML, CSS, JavaScript, and Google Sheets — all without any backend hosting or databases.

By connecting your form to Google Apps Script, you can automatically send form submissions (like email addresses) straight to your Google Sheet. This makes it a free and serverless alternative to services like Mailchimp or Firebase for small projects or landing pages.

🔧 Technologies Used

* HTML5 → For form structure and layout

* CSS3 → For styling and responsive design

* JavaScript (ES6) → For handling form submissions and sending data

* Google Apps Script → For backend automation

* Google Sheets → For storing collected email data

💡 Features

* Responsive email subscription form

* Real-time success and error messages

* Automatic data saving to Google Sheets

* No backend server required

* Works with any website (static or hosted)

🧩 Use Cases

* Newsletter sign-up forms

* Landing page subscriptions

* Contact data collection for portfolios or small business sites

* User feedback or waitlist registration forms

⚙️ Requirements

* A Google account (to create a Google Sheet and Apps Script)

* Basic knowledge of HTML, CSS, and JavaScript

* Web browser with internet access




## Documentation

[Documentation](https://linktodocumentation)


## Related

Here are some related projects

[Awesome README](https://github.com/matiassingers/awesome-readme)


## Usage/Examples

```javascript
const scriptURL = 'https://script.google.com/macros/s/AKfycbygm3LqpZy4fqepMXOubaj9Edj4316YgMX1S8KPZFGCIstn0xUTDX3bNjoQAqAVXMtM9g/exec'
  const form = document.forms['submit-to-google-sheet']
  const msg=document.getElementById("msg")

  form.addEventListener('submit', e => {
    e.preventDefault()
    fetch(scriptURL, { method: 'POST', body: new FormData(form)})
      .then(response =>{
            msg.innerHTML="Thanks You For Subscribing!"
            setTimeout(function(){
               msg.innerHTML=""
            },5000)
            form.reset()
      })
      .catch(error => console.error('Error!', error.message))
  })
}
```

