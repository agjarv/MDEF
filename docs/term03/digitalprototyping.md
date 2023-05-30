# Digital Prototyping for Design: Interfaces

## Wildcard - Robots

For this class we got to learn how to control a robotic arm with Grasshopper and simulate the movements in Rhino. Josep demonstrated on how to install the library for the robotic arm and how to use a Grasshopper example sketch to get the robot to "write letters". I was able to install it on my computer and try out the simulation. It was pretty easy to install and get started moving the robot arm in the Rhino/Grasshopper simulation. I made a simulation in Grasshopper of the robotic arm saying "Hi Robot". 

![](../images/term-03/prototypingdesign/robot_arm.gif)  

In the lab Josep attached an LED to the robot so the robot could do "light writing". Using a timelapse camera we were able to capture the LED light tracing based on the robot's movements to get some cool light art. This was really fun and I was surprised how easy it was to control this robot even though it looks very complicated.  

![](../images/term-03/prototypingdesign/robot_write1.png)  

![](../images/term-03/prototypingdesign/robot_write2.png)  

## Advanced Design tools - Blender

## Live Coding as a Human Interface

## Blender as Interface

## Final Micro-challenge: Intellectual property  

For this final challenge Seher and I continued working on the project we had been working on in previous microchallenges. Our project, Andaaza, was created to encode audio messages onto the surface of everyday objects -- a ceramic cup is what we have started with. Andaaza was created as a storytelling tool to carry our messages through time and to explore alternative ideas of measurement from a post-scientific perspective. In the past two challenges we successfully built a machine that takes audio input in real time, processes it, and embosses it onto a ceramic cup, similar to how sound can be recorded onto a vinyl record.

Check out the full project on our [GitHub](https://github.com/SeherKrishna02/Andaaza)

### Audio Generated Visuals  


To incorporate what we learned this term in our digital prototyping courses we decided to add a digital component to accompany the project. We planned to create a collection of digital assets based off the sound recordings that will be taken at the time of creating the cups. These digital twins will accompany each ceramic cup and stay on a digital archive online to represent the messages engraved in each cup.  The sound waves will be recorded in both the cups and into an audio file.

#### Processing  

We started working on making generative images from the sound recordings in Processing. We generated some still images based off the sound waves that we thought matched the aesthetics and feeling of the project. These images were generated with the audio recordings in Processing using the minm library based on this paper by [Manuel Kretzer](http://responsivedesign.de/wp-content/uploads/2016/05/tutorial-06_processing-soundmapping2.pdf). 

![](../images/term-03/prototypingdesign/processing_lines00.png)  

![](../images/term-03/prototypingdesign/processing_lines01.png)  


#### p5.js   

After creating these images we realized that we would like the media to be more interactive and decided to try out the sound recordings in a more interactive format with p5.js. p5.js will allow us to make interactive graphics that can be embedded as javascript on a webpage.  Here are the sample visualizations made in p5.js to accompany the sound recordings.


[Mother's Kitchen](https://editor.p5js.org/agjarv/full/4PX7xMz5z)  
[Grandmother's Kitchen](https://editor.p5js.org/agjarv/full/qOPdnXOsH)  
[My Kitchen](https://editor.p5js.org/agjarv/full/o7EYgK_W5R) 


[Edit Code](https://editor.p5js.org/agjarv/sketches/o7EYgK_W5R)

![](../images/term-03/prototypingdesign/tree_trial_00.png)  
![](../images/term-03/prototypingdesign/tree_trial_01.png)  
![](../images/term-03/prototypingdesign/tree_trial_03.png)  

### Online Archive

We decided to create a webpage to host our archive of interactive media. The website can be found here: https://seherkrishna02.github.io/Andaaza/

Going further we would like to make a version of the p5.js sketch we created so that visitors to our webpage can interact and add to the archive. We got this feedback in our final presentation and we would like to incorporate it. This sketch will allow visitors to respond to the question "What message would you like to pass on to future generations?" They will be able to record and save audio and then modify select parameters of the sketch to customize the visual appearance of the animation. This sketch will be embedded in our archival webpage so that people can contribute to the archive even if they can't participate in the live intervention. 