# Digital Prototyping for Design

## Electronics and Coding

The task for this day was to make some music with an Ardunio compatible board using a buzzer as an output. I started with some built in examples using the tone() function. To take it further I wanted to find a more interesting way to control the sounds rather than using a programmed melody. I started out with a potentiometer to control the pitch using the Arduino tone() function. This function generates synthesized square waves. 

I am interested in making a version of this [paper synthesizer](https://www.instructables.com/PaperSynth-an-8-bit-Synthesizer-Made-Out-of-Paper-/) eventually. I wanted to see if I could make my own ribbon potentiometer instead of buying the soft potentiometer that they suggest. I found a couple resources online that I have linked below in references. I made a quick prototype out of an old TMB (metro) card, some conductive tape, and a strip of Velostat. 

It took quite a bit of testing and research to figure out how to get it to work properly since I know very little about electrical engineering. When I first plugged the sensor in it was reacting to touch but also still jumping all over the place when it wasn't being activated. I realized I needed to add a pulldown resistor to keep it at a zero value when it was not pressed. That resolved the problem of it making sounds when touched. I had another issue of it being jumpy and playing multiple notes when it was touched. I solved that by smoothing the analog input from the sensor. I had some problems getting it right and kept getting an error. I went and asked ChatGPT to help me figure out where I was going wrong and I got a great answer! ChatGPT explained to me exactly where I went wrong and suggested a few lines to fix the mistake. I got the paper potentiometer working really well but I was getting sick of the Ardunio tone() screams and beeps. 

I decided to explore the Mozzi Library a bit. Mozzi uses oscillators and filters to make way more interesting sounds. I tried out some of the example codes with the paper potentiometer and was pretty cool. In the future weeks I am interested in making a diy synth based on this paper potentiometer and the Mozzi library. 


<div style="position: relative; width: 100%; height: 0; padding-top: 75.0000%;
 padding-bottom: 0; box-shadow: 0 2px 8px 0 rgba(63,69,81,0.16); margin-top: 1.6em; margin-bottom: 0.9em; overflow: hidden;
 border-radius: 8px; will-change: transform;">
  <iframe loading="lazy" style="position: absolute; width: 100%; height: 100%; top: 0; left: 0; border: none; padding: 0;margin: 0;"
    src="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFaf9KXaPw&#x2F;view?embed" allowfullscreen="allowfullscreen" allow="fullscreen">
  </iframe>
</div>
<a href="https:&#x2F;&#x2F;www.canva.com&#x2F;design&#x2F;DAFaf9KXaPw&#x2F;view?utm_content=DAFaf9KXaPw&amp;utm_campaign=designshare&amp;utm_medium=embeds&amp;utm_source=link" target="_blank" rel="noopener"> Electronics and Coding Lab Notes</a> by agjarv


### References 

- [Arduino Tone Generator](https://diyelectromusic.wordpress.com/2020/06/01/arduino-tone-generator/) by Kevin at diyelectronicmusic.wordpress.com

- [Ribbon Potentiometer](https://www.instructables.com/Make-a-Ribbon-Controller/) on Inscrutables

- [DIY Resistive Ribbon Sensor](http://www.ooooo.be/devices/ribbon4/ribbon4.htm)

- [Analog Input Instructables](https://www.instructables.com/Analog-Input/)

- [Mozzi Library](https://sensorium.github.io/Mozzi/examples/)

- [Paper Synth](https://www.instructables.com/PaperSynth-an-8-bit-Synthesizer-Made-Out-of-Paper-/) by Bryan Cera

### References for Later

[Adaptive Morse Code Detector](https://www.hackster.io/shjin/adaptive-led-morse-code-decoder-and-timer-interrupt-8d18a7)

[Pulse Counter](https://forum.arduino.cc/t/pulse-counter-and-time-measurement/904085/12)

[Photocell Reading](https://learn.adafruit.com/photocells/arduino-code)




