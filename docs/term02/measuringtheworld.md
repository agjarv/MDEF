# Measuring the World

## Sense-Making Journal 


MDEF: Measuring the world / A world in data activity report.

Team:  
Amanda  
Claudia  
Ahmed  
Caglar  
Korbinian  


## From objectives to the hypothesis

### Brainstorming

![](https://i.imgur.com/uNfRo4e.jpg)


### **Project Goals**

**Objective** 

> **We want a better work-life balance**

A lot of **questions**
- Do I spend enough time in nature?
- Is my work fulfilling?
- Is my identity / life shaped mostly by my work?
- Are our salaries high enough?
- Do we get health care?
- Do we have recovery time at the end of a work day?
- Do we have time to connect with people in a meaningful way?
- Do we have time and energy to do what we love?
- Do we feel we are free to choose what we do?
- Do we have enough time for our mental health?

*Pick one question and make a statement out if it:*
Do we have time and energy to do what we love?

**Hypothesis**

> **People lack the time and energy to pursue their passions outside of work.**





### **From Hypothesis to Data**


#### Tools selection

Arduino
![](https://i.imgur.com/uvxVbbm.jpg)


#### **First Experiments**

We started gather data to understand the difference between natural and artificial light. We used a a resistor of 1K.
March the 9th, rainy and cloudy day in Poblenou, Barcelona - We still could spot significant differences from outdoor and indoor:

- Artificial light in MDEF class: 2000 K
- Artificial light in the hall of IaaC: 1000 K
- Natural light outdoor(cloudy): 4095 K (max)

![](https://i.imgur.com/oNrtDYk.jpg)


#### **Data Capturing Strategy**

We used two different strategies to capture data:
- with a sensor 
- from a data set (Twitter and Wi-fi).

#### **Materials Needed**

[Adafruit Feather ESP32](https://www.adafruit.com/product/3405)
LDR Sensor
Laptop
[ArduSpreadsheet](https://circuitjournal.com/arduino-serial-to-spreadsheet)
[IFTTT](https://ifttt.com/explore)
Orange3
Twitter account

#### **Detail Setup Instructions**

1. With Arduspreadsheets: sensor data from the serial collection to a .CSV file
2. Gather the data via Wi-fi connection
3. Generate more info through database - Orange3: Text (add-on) - Twitter and sentiment analysis



## **ORANGE3** ##

### First Trial: World Happiness Report

First trial we tried to upload data from the World Happiness Report 2022, the range was too wide, too many information and detaled classification. It is based on too many socio-economic aspects, that's why we decided not to base our research on it.

![](https://i.imgur.com/HFWVTnw.jpg)

### Second Trial: OECD.Stat

Then we decided to narrow down the research field and get the data drom OECD.Stat, a survey that gathers data about the percentage of adults who reported that over the last 12 months it has been difficult for them to fulfill their family responsibilities because of the amount of time they spent at work.

![](https://i.imgur.com/6aWKC2i.png)


### Third trial: Twitter 


![](https://i.imgur.com/HdMYhpO.png)



Collecting data from Twitter throughout Orange3 - SENTIMENT ANALYSIS
Query word list: over time; over working
Language: english
Tweets: 1000

![](https://i.imgur.com/g8YtIwV.png)

We created a word cloud out of it

![](https://i.imgur.com/ojn6Ce6.png)

And then analyized the emotions throughout a Box Plot

![](https://i.imgur.com/HYINkOM.png)


## **LDR Sensor Data** ##

To collect and log the LDR sensor data we employed a couple of strategies. First, we downloaded Arduspreadsheets and were able to log the LDR data in a .csv file. We took readings of the resistor value every 10 seconds and each reading was stored in a spreadsheet with a corresponding timestamp. 

After this we realized we wanted the device to be mobile so it could be carried with a person to monitor the light levels they encounter throughout the day. For this we first tried to connect via bluetooth to a cell phone to collect the data. We made the bluetooth connection and could see the data but couldn't find a good way to save the data. After this we went with the option of sending the data over WiFi to an online spreadsheet. To make this happen we used If This Then That (IFTTT) to connect to Webhooks to publish the data over Wifi. After this we were able to connect the ESP32 to a phone hotspot and the device was mobile! We tested out different light levels throughout the IAAC building and outsice in the sun. 


#### Tips

[Tutorial for publishing sensor readings to Google using IFTTT](https://randomnerdtutorials.com/esp32-esp8266-publish-sensor-readings-to-google-sheets/)

[Arduino Serial to Spreadsheet](https://circuitjournal.com/arduino-serial-to-spreadsheet)

Pick the right sensor/tool for the application. In the end we didn't find the light sensor readings as useful for supporting our research for the time we had. 

It will take WAY more time than you imagine to get everything working. Make extra allowances for time. 



## Data Capture

<div style="padding:75% 0 0 0;position:relative;"><iframe src="https://player.vimeo.com/video/806717353?h=e828de4e47&amp;badge=0&amp;autopause=0&amp;player_id=0&amp;app_id=58479" frameborder="0" allow="autoplay; fullscreen; picture-in-picture" allowfullscreen style="position:absolute;top:0;left:0;width:100%;height:100%;" title="data_collection_worklifebalance.mp4"></iframe></div><script src="https://player.vimeo.com/api/player.js"></script>

### Data Summary

#### From OECD Stats

|     | Below upper secondary education | Upper secondary and post-secondary non-tertiary education | Tertiary education | All levels of education |
| --- | ------------------------------- | --------------------------------------------------------- | -------- | -------- |
|Italy   | 56                 |  58                      |    48    |       55   |
|Spain   |      45              |               58          |      56    |     52     |
| Türkiye  |         88         |                 82        |     72     |     81     |
| United States |       58    | 47                      | 55     | 52     |

![](https://i.imgur.com/jvDeRCS.png)
https://stats.oecd.org/

| Data Summary         |                                                                                                      |
| -------------------- |:---------------------------------------------------------------------------------------------------- |
| Project Title        | LDR Webhooks Events                                                                                  |
| Capture Start        | 03-10-2023                                                                                           |
| Capture End          | 03-10-2023                                                                                           |
| Original Data Format | Light Sensor Readings                                                                                |
| Submitted format     | CSV file                                                                                             |
| Total Data Points    | 400+                                                                                                 |
| Number of datasets   | 1                                                                                                    |
| Data Repository      | https://docs.google.com/spreadsheets/d/1YFaE637PvN5C3pGN2pU6fEf1k1q3pGcjHVHkii8CwdA/edit?usp=sharing  |

| Data Summary             |                    |
|--------------------------|--------------------|
| Project Title            | LDR Readings Day 1         |
| Capture Start            | 03-9-2023         |
| Capture End              | 03-9-2023         |
| Original Data Format     | Light Sensor Readings    |
| Submitted format         | CSV file           |
| Total Data Points        | 71                |
| Number of datasets       | 1                  |
| Data Repository          | https://github.com/agjarv/mdef-a-world-in-data/blob/main/ldr_sensor_manual2.csv  |

## Data Insights

:::warning
A hypothesis may be testable, but even that isn’t enough for it to be a scientific hypothesis. In addition, it must be possible to show that the hypothesis is false if it really is false. Proving it's true it will require testing all possible combinations, that's hard, maybe impossible.
:::



### Reflections

- Our Arduino tests could have been more successful if we had more time to dedicate to locally  gather data around students. 
- It could have been better if we selected our hypotesis more specific, we started from a way too broad and wide range. We needed to be more focused since the beginning.
- When analazying data with Orange, is important to understand the range or data you're feeding to it. If it's too wide, you may loose tge focus easily and not get the results you're hoping for.
- Lower our expectations on finding amazing data.
- In the reseach, we should have designed a process and be more organized about the data gathering. We lost our main goal while we were checking the data. 
- Trying many different techniques in one day was at the same time interesting but confusing and brought a little bit of chaos in the process. 
- We found interesting data on world happiness based on socioeconomic indices that we didn't get to use as much. For going further it could be interesting to use a sensor to monitor how much sunlight a group of people get per day and compare it with the happiness index. 