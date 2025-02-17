# Table of Contents
1. [Algorithm Designs & Data Requirements](#algorithm-designs--data-requirements)
2. [Use Case Diagram](#use-case-diagram)
3. [Data Flow Diagrams](#data-flow-diagrams)
    - [Forecast Advice – Level 0](#forecast-advice--level-0)
    - [Forecast Advice – Level 1](#forecast-advice--level-1)
    - [Air Quality – Level 0](#air-quality--level-0)
    - [Air Quality – Level 1](#air-quality--level-1)
4. [Flowchart](#flowchart)
5. [Data Dictionary](#data-dictionary)
6. [Visual Interface Designs](#visual-interface-designs)
    - [Assets](#assets)
    - [Home Page](#home-page)
    - [Air Quality Page](#air-quality-page)
    - [Forecast Advice Page](#forecast-advice-page)
7. [Testing Strategy](#testing-strategy)

## Algorithm Designs & Data Requirements

### Use Case Diagram:
This use case diagram shows which users of the system will be able to view what parts of the system. I’ve shown that there will only be one user, so the product will be privacy-focused. The user will be able to access all parts of the front-facing system. Once the user logs into the system, they will be able to view all the tracking data for their account, view the local air quality, forecast, and information that will allow the system to make informed decisions based on the current forecast.

---

## Data Flow Diagrams
Below are all the different Data Flow Diagrams for the proposed system. All use case diagrams are separate from each other to minimize messiness and maintain readability. Separating the designs also allows the development team to work independently on each use case of the system.

### Forecast Advice – Level 0
Below is a level 0 Data Flow Diagram (DFD). This shows what will go in and out of the basic system. This design shows two entities that can input data into or take data out of the system. The user entity can provide the system with the current forecast, and the system will return advice made specifically for that user. The admin entity can also add new advice for conditions that haven’t been addressed yet (e.g., if it is a cloudy, rainy day, the user shouldn’t drive). The admin entity can add this new advice to the system.

### Forecast Advice – Level 1
Below is a level 1 DFD that shows the above level 0 system in more detail. It shows how the system deals with user requests and how the admin adds new advice. The user entity provides the forecast to the system, where the data is then parsed into the correct format for the system. Once parsed, it is checked against the advice database, which contains all the advice in the system. The admin inputs new advice to the system, and it is parsed and saved to the advice database for future use.

### Air Quality – Level 0
Below is the level 0 DFD for the air quality use case for the system. This design shows the air quality measuring device inputting air quality data into the system, where it is transformed into a readable format for the user. This readable format could be presented in multiple ways, such as a graph showing the quality over time or a simple sentence.

### Air Quality – Level 1
Below is the level 1 DFD for the air quality system. This diagram shows that the air quality data will be collected from the device, saved to the database, and then retrieved upon the user's request. The data is formatted into a human-readable format and displayed to the user.

---

## Flowchart
Below is the flowchart for this system design. It shows the flow of control between the system. The flowchart indicates that once the user starts the app, it checks if they are logged in. If they are not, they will go through the account creation process. If they are logged in, they continue to the user navigation, where they can choose which service they want to access.

---

## Data Dictionary
Below is the data dictionary for the proposed system. I have abbreviated the data types for the technical personnel who should understand what the abbreviations mean. I have also added useful comments to most variables to show their usage or any special details. The variable names follow camelCase for maintainability.

| Name             | Data Type | Max Size | Validation                                                      | Comments                                           |
| ---------------- | --------- | -------- | --------------------------------------------------------------- | ------------------------------------------------- |
| username         | str       | 16       | Must be unique                                                  | Used as a primary key                             |
| password         | str       | 16       | Must contain a special symbol and a number                       | Should be encrypted for security                 |
| airQualityFormat | str       | 512      | N/A                                                             | Formatted for user (may increase size)            |
| userForecast     | str       | 16       | Will be parsed by the system                                     | N/A                                               |
| forecastAdvice   | str       | 16       | N/A                                                             | Outputted from the system                         |
| selection        | int       | 1        | Must be between 1-5                                              | Will choose which system the program follows      |
| emailAddress     | str       | 20       | Must contain a '@' and '.' with space in between; must not end on '.' or '@' | Used to contact                                  |
| postcode         | str       | 10       | Must be a valid postcode                                         | Used for local weather tracking                   |
| CO2Concentration | float     | 4        | N/A                                                             | In ppm                                             |
| COConcentration  | float     | 4        | N/A                                                             | In ppm                                             |
| NO2Concentration | float     | 4        | N/A                                                             | In ppm                                             |

---

## Visual Interface Designs

### Assets

| Image | From | Purpose |
| ----- | ---- | ------- |
| ![Image](https://www.flaticon.com/) | Various images. | Navbar Icons, Weather Forecast Icons, Main Page Icon |
| ![Line Graph](https://www.linegraph.com/) | Line Graph | Data Visualization for Air Quality |
| ![Weather Image](https://www.weatherimage.com/) | It's raining harder in the U.S. | Background image related to weather conditions |
| ![Background Image](https://www.background.com/) | Environmental, health, and safety policies | Background image for context |
| ![Health Privacy Image](https://www.healthprivacy.com/) | How to stop health and fitness apps from using your private data | Background image |

### Home Page

- (Include a mock-up image or design)
- Describe Why it looks the way it does

### Air Quality Page

- (Include a mock-up image or design)
- Describe Why it looks the way it does

### Forecast Advice Page

- (Include a mock-up image or design)
- Describe Why it looks the way it does

---

## Testing Strategy

| Date of Test  | Component to be Tested | Type of Test | Prerequisites and Dependencies | Relationship |
| ------------- | ---------------------- | ------------ | ------------------------------ | ------------ |
| 12/12/24      | All Pages              | Functional – Navigation between pages | Pages exist and buttons on each of them | All pages will link to each other. Navbar will link all pages to the home and account page. |
| 13/12/24      | Weather                | Functional – Ensure that weather page moves with the date | Weather page and weather database set up | Weather page sends a request to a function which gets data from the database and formats it. |
| 14/12/24      | Air Quality            | Functional – Ensure data updates when new data is entered | Air quality page and air quality database set up | Air Quality page sends a request to a function which gets data from the database and formats it. |
| 15/12/24      | Account                | Functional – User can log in and create an account | Account database contains data | Page sends a request to the database to return a boolean for logging in or creating an account. |
| 15/12/24      | Account                | Stress – Server can handle multiple users logging in or creating accounts | Test users have accounts in the database | Login page sends multiple requests to the database to see if it can handle them without crashing. |
| 16/12/24      | Account                | Security – Prevent SQL Injection | Account database and login page set up | Login page sends a query to the database and tests if SQL is filtered. |
| 17/12/24      | Weather                | Stress – Can handle multiple queries from different users | Weather page and weather database set up | Weather page sends multiple requests to the database to see if it can manage them without crashing. |

The modules have been tested in this order to ensure that the development company can create and test the modules as they are made. Testing in this sequence ensures that all functional elements are completed before testing the modules interfacing with each other.
