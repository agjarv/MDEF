# Almost Useful Ghost Machine

<iframe src="https://docs.google.com/presentation/d/e/2PACX-1vRXRer_4LkwNSSRSiP6Ro8_FdwRp9BHXNzIQmxz3BfKbHeDDZMHWxm6gaH_CFEr-JNS2SFxAeDB-icy/embed?start=false&loop=false&delayms=3000" frameborder="0" width="960" height="569" allowfullscreen="true" mozallowfullscreen="true" webkitallowfullscreen="true"></iframe>

## Code
```
/* The code reads analog input from the LDR sensor determines if the amount of light changes. 
If the ambient light sensed is below the threshold it will turn off the lights 
and make the sounds from the “ghost” passing over. 
 

 This is using the example Arduino smoothing code. 
 http://www.arduino.cc/en/Tutorial/Smoothing
  **
  Reads repeatedly from an analog input, calculating a running average and
  printing it to the computer. Keeps ten readings in an array and continually
  averages them.
  **

  created 16 Nov 2022
  by Amanda Jarvis  <https://github.com/agjarv>
  
  
*/

// Define the number of samples to keep track of. The higher the number, the
// more the readings will be smoothed, but the slower the output will respond to
// the input. Using a constant rather than a normal variable lets us use this
// value to determine the size of the readings array.
const int numReadings = 50;

int readings[numReadings];      // the readings from the analog input
int readIndex = 0;              // the index of the current reading
int total = 0;                  // the running total
int average = 0;                // the average

int LDRsensor = A0;       // define analog pin A0. (input/sensor)
int led0 = 12; // define pin 12 for led (output)
int led1 = 11;
int led2 = 10;
int led3 = 9;
int led4 = A1;
int led5 = A2;
int piezoPin = 3;

void setup() {
  // initialize serial communication with computer:
  Serial.begin(9600);
  pinMode(LDRsensor,INPUT); // sets analog pin A0 as input.
  pinMode(led0,OUTPUT); //sets pin 13 as output.
  pinMode(led1,OUTPUT); 
  pinMode(led2,OUTPUT);
  pinMode(led3,OUTPUT); 
  pinMode(led4,OUTPUT); 
  pinMode(led5,OUTPUT);
  // initialize all the readings to 0:
  for (int thisReading = 0; thisReading < numReadings; thisReading++) {
    readings[thisReading] = 0;
  }
}

void loop() {
  // subtract the last reading:
  total = total - readings[readIndex];
  // read from the sensor:
  readings[readIndex] = analogRead(LDRsensor);
  // add the reading to the total:
  total = total + readings[readIndex];
  // advance to the next position in the array:
  readIndex = readIndex + 1;

  // if we're at the end of the array...
  if (readIndex >= numReadings) {
    // ...wrap around to the beginning:
    readIndex = 0;
  }

  // calculate the average:
  average = total / numReadings;
  //long brightness = map(average, -650, -400, 0, 255);
  if(average > 420) //condition
  {
    analogWrite(led0,255); //turns LED on.
    analogWrite(led1,255); //turns LED on.
    analogWrite(led2,255); //turns LED on.
    analogWrite(led3,255); //turns LED on.
    analogWrite(led4,255); //turns LED on.
    analogWrite(led5,255); //turns LED on.
    noTone(piezoPin);
  }
  else
  {
    analogWrite(led0,0); //maps led to to brightness average
    analogWrite(led1,0);
    analogWrite(led2,0);
    analogWrite(led3,0);
    analogWrite(led4,0);
    analogWrite(led5,0);
    tone(piezoPin, average); //sets frequency of the tone to sensor average
  }
  // send it to the computer as ASCII digits
  Serial.println(average);
  delay(10);        // delay in between reads for stability
}
```
## Video
<div style="padding:75% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/773159561?h=aa561b4bad&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="ghost machine.mp4"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

