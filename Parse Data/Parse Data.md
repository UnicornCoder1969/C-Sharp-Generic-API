# Table of Contents
1. [Prototype Effectiveness](#prototype-effectiveness)
   1.1. [Assets](#assets)  
   1.2. [Sources](#sources)  
   1.3. [Legal and Ethical Implications](#legal-and-ethical-implications)  
2. [Requirements](#requirements)
   2.1. [Functional Requirements](#functional-requirements)
   2.2. [User Acceptance Criteria](#user-acceptance-criteria)
   2.3. [Non-Functional Requirements](#non-functional-requirements)
3. [Key Performance Indicators](#key-performance-indicators)
4. [Future Development](#future-development)
   4.1. [Areas of Improvement](#areas-of-improvement)
   4.2. [Additional Features](#additional-features)

---

## Prototype Effectiveness

### Assets
The prototype has many different backgrounds for each page. These are sourced from the internet during development time. Sources of these were from different website backgrounds, but unfortunately, I didn’t get the chance to write down exactly where the assets came from. The main login background is a still image of a field of grass. I thought this would suit the login screen as it can be defined as a metaphor for not only logging into the application but logging into health and the outside world. The main program background is a picture of a woodland with a walkway covered in leaves. This suits the purpose of the main background as you have already logged into nature and are now on the path of becoming healthy.

### Sources
Whilst developing the prototype I needed placeholder assets; these were gathered from numerous sources. The most common source was Flaticon. Flaticon provides thousands of free assets for use in many projects if the developer credits the source of these assets. These sources should have been kept in an asset log file.

### Legal and Ethical Implications
Because I used icons from websites that I can’t remember, if I were to send the prototype off, I would either have to change the background to an image that is copyright-free or find the original source and make sure that I can use the images commercially. If I do not do this, then Health Advice Group and the developers could land in legal troubles over copyright infringement.

During the development of the prototype, ethical dilemmas regarding where to store data arose. Some users are privacy advocates and would not like their data stored on one central database. To avoid this, the program will use a local database stored on the device. However, features such as health advice will need to be stored on a central server.

---

## Requirements

### Functional Requirements
The first functional requirement outlined in Task 1 was that the program must use localized weather forecasting. I do believe that this was fully implemented, given that the user inputted the correct coordinates. If the user entered the correct coordinates, then the API would return the correct weather response for that location. If they didn’t use the correct coordinates, they wouldn’t get the weather response for their area. For this reason, I believe that it was implemented successfully on the development part.

The second requirement was that the program must show all information on a central dashboard. This was fully implemented as there is only the 1 ‘page’ of the program that can be used. Both the weather forecast and air quality data are displayed on the central display for easy access.

The program was also required to provide a section for advice dealing with health matters affected by the weather and environment. Unfortunately, this was not implemented at all due to time constraints and a switch in programming languages from Python to C#.

The first desirable requirement was that there must be a section for all the previous data used by the charity. This was again not met due to the refactoring of the program in C#. However, due to the design of the database, the existing information could be easily implemented in the future.

The requirement for the program to personalize health advice based on the user's location was partially completed. I managed to get the weather forecast running on local GPS coordinates. Once the advice page is created, it will integrate seamlessly with the local weather forecasting.

Despite a few requirements not being met, the program does accommodate for all users’ needs. In feedback forms, all users who labeled themselves as having a disability gave the prototype an overall accessibility rating of 5.1 out of 10.

The last requirement, tracking the health of each user, was not met. This could, however, be easily implemented in the next iteration of the program due to the way the backend database works.

### User Acceptance Criteria
Many of the user requirements were based on how navigable the prototype was. Feedback from users gave an overall 8/10 on the navigation question for the prototype. This aligns well with the UAC, as the first two criteria were that the user can click on every button and be taken to a new page. The third criteria were that the app should display a title, which was met as the Health Advice Group logo and title appear on the login screen.

The prototype does not have a light/dark mode toggle switch. The reason for this is that I intentionally used colors that would stand out to both light and dark mode users. This aligns well with survey responses, with more people saying they liked the color scheme than not.

The next criteria could not be met because the page for existing data was not created by the time the prototype was finished. The program does, however, show that the air quality changes in certain places viewable on the panel on the right-hand side of the main menu. Users cannot yet view their personal advice, but they will be able to once the feature has been implemented.

### Non-Functional Requirements
The first non-functional requirement was that the program should be secure, meaning that users could not break it by inputting invalid information. I believe this was met by the error handling processes inside the prototype, where the user is prompted if they give invalid coordinates.

The second requirement was that the prototype should be mobile-friendly. Due to the nature of C#, I cannot compile the prototype for mobile applications. However, I determined if this was met by testing the prototype on different computers with various screen sizes and resolutions. The prototype scales well with alternate screen sizes.

The friendly UI requirement was met according to survey responses, where most users liked how the prototype looked, except for a few places where the colored text on different backgrounds made it hard to read.

The program also meets the requirement of being fast. Even API responses and data parsing take less than 1 second.

---

## Key Performance Indicators
The first KPI was that the program should not store any passwords in plain text. While the password is stored in plain text during testing, there is a function in the program for hashing the password before it is saved to the database. This feature is disabled for testing but can easily be reconnected to ensure secure password storage.

The program meets the KPI for having scalable UI elements due to the testing on various screen sizes and resolutions, including 4K and 1080p displays.

---

## Future Development

### Areas of Improvement
If I were to further develop the prototype into a fully developed application, I would improve on meeting the functional requirements, such as ensuring that the application shows the previous data collected by the Health Advice Group. I would also improve the forecasting system to not require the user to input latitude and longitude. Instead, I would allow users to enter a country and city for travel purposes and have the option for GPS location to be retrieved automatically.

Additionally, I would enhance the air quality information. Feedback from users suggested adding a dedicated page for more detailed air quality information, explaining why a high level of something is bad and what users can do to reduce their risk of health issues.

A few survey responses also indicated that users would like to change the background images, as the text was difficult to read. This can be done by either changing the image or adding customization features so that users can select their background.

### Additional Features
After implementing the above changes, I would like to work on having separate pages in addition to the main dashboard. This could include a dedicated forecast page where users can view the forecast hourly instead of just daily. The current API can facilitate hourly forecasts, but I have it disabled to keep the dashboard focused on daily forecasts.

Finally, I would like to implement a feature that allows users to track their health using metrics such as weight. This could be achieved by creating a separate table in the database to store the user’s health data locally on the device. This would help ease user concerns about privacy. The dashboard could also display changes in user statistics, such as how much weight they have lost.
