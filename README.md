# Programming Digital Media

Examples for Programming Digital Media class at Louisiana State University, Spring 2020

- email: <tcarso2@lsu.edu>   
- Office hours: 1pm to 3pm Monday in the Digital Media Center (2006)
- Zoom
  - We will be using zoom to meet during our normal class time 
  - Please email to schedule a personal meeting if you need it
- Ask for help on the [Discord](https://discord.gg/jzG8rS)
  -  you can post a question about anything related to the class and one of your classmate or I will answer it. 
  

---

## Lectures
### Tone.js
- **2-13-20** - Web audio basics and sound file players - [slides](https://lsu-pdm-2020.netlify.com/week_1_t/_site/#/), [textbook](https://pdm.lsupathways.org/3_audio/1_sampler/1_lesson_1/)
- **2-18-20** - Adding effects and intro to synthesis - [slides](https://lsu-pdm-2020.netlify.com/week_1_th/_site/#/), [textbook](https://pdm.lsupathways.org/3_audio/1_sampler/2_lesson_2/)
- **2-20-20** - **20-27-20**  - Making synthesizers from scratch - [slides](https://lsu-pdm-2020.netlify.com/week_2_t/_site/#/)
- **3-3-20** - Scheduling signals and LFOs - [slides](https://lsu-pdm-2020.netlify.com/week_2_th/_site/#/)
- **3-5-20** - Instruments and Sequencers - [slides](https://lsu-pdm-2020.netlify.com/week_3_t/_site/#/), [textbook](https://pdm.lsupathways.org/3_audio/2_synthsandmusic/2_lesson_2/)
- **3-9-20** - Sound Effects and Sequencers - [slides](https://lsu-pdm-2020.netlify.com/week_3_th/_site/#/)
<!-- - **3-6-19** - Rhythm / Scales / Tuning / Distributed smartphone music - [slides](https://lsu-pdm-2019.netlify.com/week_4_t/_static/#/) -->

### Arduino

Video tutorials and notes

* Digital out - [notes](Hardware_Week_1_Th)
    * [Blink](https://www.youtube.com/watch?v=5vkuxBmWNDo)
* Analog Out - [notes](Hardware_Week_2_T)
    * [Fading](https://www.youtube.com/watch?v=vd93XYizHJ8)
* Analog Input 
  * [Potentiometer](https://youtu.be/tU6CDI3UI34)
      * Note: the intro to this was cut off but the circuit that is already there is from the blink tutorial. The thing i'm holding is a potentiometer that allows analog input between 0v and 5v.
  * [Photoresistor](https://youtu.be/0vB-MQ8Xu80)
    * Note: I was referring to the serial monitor through this video but didn't realize that it wasn't recording the screen. You should be able to see it on your computer.


## Resources

- Starter templates
  - [download](https://github.com/tatecarson/tonejs-p5j-starter-template) - shows a basic example project with Tone.js and p5 with a button and slider
    - click the green button to download
  - [p5 web editor](https://editor.p5js.org/tcarso2/sketches/MMvCDJ0C) - if you still can't run a local server. After you're finished click on file -> download to get the zip to turn in your project. 
    - warning: there may be a file size limit, try to use smaller and shorter samples 

### Context not starting? 

Try: 
```
function startContext() {
  console.log("Tone is: ", Tone.context.state)
  document.body.addEventListener("click", () => {
    Tone.context.resume();
    console.log("Tone is: ", Tone.context.state);
  });
}

startContext(); 
```

That has stopped working for some students, if it does try this instead: 
```
function mousePressed() {
  if(Tone.context.state === 'suspended') {
    Tone.context.resume();
  }
}
```

This if statement could go anywhere where the user can trigger it with an event. 

### Tone.js

#### Basics

- [Tone.js Github](https://github.com/Tonejs/Tone.js) - main repository
- [Tone.js API](https://tonejs.github.io/docs/) - documentation
- [Tone.js Wiki](https://github.com/Tonejs/Tone.js/wiki) - covers a few things not explained in the API, ex. Time, envelopes 
- [Tone.js Google Group](https://groups.google.com/forum/#!forum/tonejs) - ask a question here if you can't get it answered in class
- [PDM Online Textbook](https://pdm.lsupathways.org/) - in development for highschool class but covers all necessary material

#### Extras

- [Interactive Presets](https://www.guitarland.com/MusicTheoryWithToneJS/Presets-gh-pages/) - use to experiment and find new sounds, do not copy presets from here else you add something unique to them. 
- [Make music with Tone](https://www.guitarland.com/MusicTheoryWithToneJS/TonejsSetup.html) - some tutorials for making more traditional music with Tone
- [tone-rhythm](https://github.com/scraggo/tone-rhythm) - very helpful for making musical phrases with tone
  - [Ex. Maria](https://codesandbox.io/s/qzq0lvpq0w) - play Maria with tone. This requires knowledge of importing from npm with the 'import' keyword. It will not work with a script tag.
- [Algorithmic Music Tutorial](https://junshern.github.io/algorithmic-music-tutorial/) - uses p5 sound but many of the creative ideas are transferable to Tone.js
---
#### Inspiration

- [Hackpact](https://stc.github.io/HackPact/) - Algorithmic audiovisual sonification studies


### Digital Audio

- [Digital Sound and Music](http://digitalsoundandmusic.com/curriculum/) - explanations and definitions of all things digital sound

### JS Basics

Still having trouble with some basics? 

- [freeCodeCamp](https://www.freecodecamp.org/)
- [codecademy](https://www.codecademy.com/learn/introduction-to-javascript)
- [MDN web docs Javascript](https://developer.mozilla.org/en-US/docs/Web/JavaScript) - includes some tutorials and the standard javascript reference 
- [stackoverflow](https://stackoverflow.com/) - find answers or ask questions to javacript related things. 