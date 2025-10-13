
# How To Make Text To Voice Converter Using JavaScript | Text To Speech Generator

🗣️ Project Description

Learn how to build a Text To Voice Converter (also known as a Text-to-Speech Generator) using HTML, CSS, and JavaScript. This beginner-friendly project demonstrates how to convert written text into spoken words directly in your web browser — without any external APIs or libraries!


## Acknowledgements

 - [Awesome Readme Templates](https://awesomeopensource.com/project/elangosundar/awesome-README-templates)
 - [Awesome README](https://github.com/matiassingers/awesome-readme)
 - [How to write a Good readme](https://bulldogjob.com/news/449-how-to-write-a-good-readme-for-your-github-project)


## Appendix

💡 How It Works

* User types text into the textarea.

* JavaScript retrieves available voices from the system using speechSynthesis.getVoices().

* When the user clicks “Speak,” the app creates a new SpeechSynthesisUtterance() object and plays it.

* Users can control rate and pitch to customize the speech output.


## Related

⚙️ Example Code (Core Logic)
const speech = new SpeechSynthesisUtterance();
const voicesList = document.querySelector("#voices");
const textarea = document.querySelector("#text");
const rate = document.querySelector("#rate");
const pitch = document.querySelector("#pitch");
const btn = document.querySelector("#speak");

speech.text = "Hello!";

speechSynthesis.onvoiceschanged = () => {
  let voices = speechSynthesis.getVoices();
  voices.forEach((voice, i) => {
    voicesList.options[i] = new Option(voice.name, i);
  });
};

voicesList.addEventListener("change", () => {
  speech.voice = speechSynthesis.getVoices()[voicesList.value];
});

btn.addEventListener("click", () => {
  speech.text = textarea.value;
  speech.rate = rate.value;
  speech.pitch = pitch.value;
  speechSynthesis.speak(speech);
});

[Awesome README](https://github.com/matiassingers/awesome-readme)


## Usage/Examples

```javascript
let speech=new SpeechSynthesisUtterance();
        let voices=[];
        let voiceSelect=document.querySelector("select");
        window.speechSynthesis.onvoiceschanged=()=>{
            voices=window.speechSynthesis.getVoices();
            speech.voice=voices[0];

            voices.forEach((voice,i) => (voiceSelect.options[i]= new Option(voice.name,i)));
        };
        voiceSelect.addEventListener("change",()=>{
            speech.voice= voices[voiceSelect.value];
        });


        document.querySelector("button").addEventListener("click",()=>{
            speech.text=document.querySelector("textarea").value;
            window.speechSynthesis.speak(speech);
        })
}
```

