# C-Sharp-Generic-API

Task-1A - Finding API <br>
Task-1B - Get API Key <br>
Task-2  - Create Request <br>
Task-3A - Recieve Request <br>
Task-3B - Parse Data <br>
# Table of Contents
1. [Business Context](#business-context)
2. [Project Definition](#project-definition)
3. [Stakeholders](#stakeholders)
4. [SWOT Analysis](#swot-analysis)
5. [Functional & Non-Functional Requirements](#functional--non-functional-requirements)
6. [Decomposition](#decomposition)
7. [KPI’s & User Acceptance](#kpis--user-acceptance)
8. [Proposed Solution](#proposed-solution)
9. [Research](#research)
10. [Emerging Technologies](#emerging-technologies)
11. [Meet the Client and User Needs](#meet-the-client-and-user-needs)
12. [Wider Issues](#wider-issues)
    - [Legal Considerations](#legal-considerations)
    - [Ethical Considerations](#ethical-considerations)
    - [Social Considerations](#social-considerations)
    - [Software Considerations](#software-considerations)
13. [Risks](#risks)
14. [Overall Justification of System](#overall-justification-of-system)
15. [Appendix](#appendix)

## Business Context

## Project Definition

## Stakeholders
The project for the client will contain stakeholders such as the actual client, the users of the solution, and the developers. As the solution develops further, stakeholders in the project could be introduced such as the investors who fund the solution to be made.

## SWOT Analysis

### Strength
Due to the fact that the Health Advice Group already has an existing infrastructure for environmental health, such as dealing with extreme temperatures or health conditions/allergies, this will help the new solution. They will be able to use some of their existing data in the new solution, making the solution more feature-backed and ready to compete with other solutions.

### Weakness
With the application wanting to get real-time data for weather forecasting, the device will need to connect to the internet, which may not be viable for certain customers who might use the device. For example, mountain climbers in the wilderness or walkers in the countryside may not have existing infrastructure to connect to the global internet/cloud, which will limit the usability of the solution.

### Opportunities
While the feature set of the new solution, combined with some of the old data, will be feature-packed, there is still room for improvement. The solution could incorporate recent technologies and features such as measuring the UV Index or the humidity of the air. These new features will further improve the image of Health Advice Group.

### Threats
Although the idea is good and will provide data for the user, there are existing devices with large backing that can compete with this product. One such device is the Apple iWatch. With its parent company being a multinational corporation with a large research & development team, they might be able to out-feature the product from the client.

## Functional & Non-Functional Requirements

### Functional Requirements

| Requirement ID | Requirement & Description | Mandatory / Desirable |
| -------------- | ------------------------- | --------------------- |
| 1              | The solution must utilize the local weather forecasting | Mandatory |
| 2              | The solution must show all the information used and the output in a central dashboard | Mandatory |
| 3              | The solution must have a section for advice dealing with health matters affected by weather and environment | Mandatory |
| 4              | The solution should have a section for all previous data used by the charity | Desirable |
| 5              | The solution should personalize the health based on location | Desirable |
| 6              | The solution should accommodate all users’ needs | Desirable |
| 7              | The solution should track the health for each user | Desirable |

### Non-Functional Requirements

| Requirement | Explanation |
| ----------- | ----------- |
| The solution will be secure | The solution should not be easily changeable. |
| The solution will be mobile-friendly | The solution should respond to device size. |
| The solution will have a friendly UI | The solution will be easy to navigate. |
| The solution will have accessibility settings | The solution will comply with standards. |
| The solution will be fast | The solution will be optimized. |

## KPI’s & User Acceptance

### KPI’s for the Non-Functional Requirements
- The solution should store any passwords used securely, not in human-readable formats (e.g., in binary files or a database).
- The solution will have scalable UI elements for each device size.
- The solution will not have any confusing names for buttons or text boxes.
- The solution will have alternate text for images and link names for links to other pages.
- The solution does not wait for more than 1 second executing 1 line of code.

### User Acceptance Criteria for the Functional Requirements
- The user can click on each button on the page.
- Each button works and can direct the user to a new page.
- Each page has a title for a friendly UI.
- Each page has a button for dark/light mode.
- There is a page for the charity's existing data and research.
- The solution should show over time how the air quality changes in certain places.
- The user can view their personalized advice.

## Decomposition
- To comply with requirement 1, the solution could use an API for getting the local weather in the device's location or could use built-in weather sensors.
- For requirement 2, the information will be stored in variables, then passed to a function to create the central dashboard.
- For requirement 3, the solution will have a bullet-point list for each issue and solution.
- For requirement 4, the “old” information will be in a separate section using the existing layout.
- For requirement 5, the solution will use data measured in the device instead of geographical area.
- Requirement 6: The solution will have color blindness filtering and text-to-speech.
- Requirement 7: The solution will save health data locally on the device for user tracking.

## Proposed Solution

## Research
In the health sector, there are ways that hospitals and GPs use technology in their everyday use. The details of which are outlined below.

### Hardware
Previously, doctors had no way of viewing the inside of a person’s body, but now that hospitals have modern scanning machines, such as X-Ray machines that doctors use to scan bones. An example is when a person goes to the hospital thinking one of their leg bones is broken, the hospital can order an X-ray where the patient goes under the ray, and the different thickness of the bone shows once the image is generated. This helps the doctor identify the fracture's location and severity. MRI (Magnetic Resonating Imaging) machines can also take pictures of the inside of the body, such as the heart, to check for blocked veins/arteries and prescribe treatment.

Another innovative technology in the health industry is the ECG (Electrocardiogram) machine, which can clip onto a patient's finger to show heart rate and rhythm. This is much more accurate than manually counting beats per minute from the pulse.

### Software
The way the NHS and other health organizations keep track of a patient's progress and diagnoses is through Electronic Health Record (EHR) software, which stores a patient's personal information and medical history. Additionally, medical imaging software is used to turn the results from CT or MRI scans into images that doctors and patients can analyze. The NHS app lets patients access their appointments, view test results, and check information from their EHR system.

## Emerging Technologies
- AI in the health industry can analyze CT scan images to help diagnose conditions like broken bones or more complex issues with greater accuracy. 
- Nanotech enables the use of small devices that can target specific areas in the body, such as cancer cells or tumors.
- 3D printing can create new organs or tissues, providing solutions when donor organs are unavailable, with potential life-saving applications.

## Meet the Client and User Needs

### Client
The client (Health Advice Group) needs the product to meet their requirements, which include weather forecasting to inform health decisions. The solution should offer specific instructions based on weather conditions like rain, flooding, or heatwaves that differ by location. The solution must also provide a central dashboard showing air quality data (e.g., carbon dioxide, carbon monoxide concentration), with details about wind speed and direction. It must also show health-related advice based on the environment.

### User
Users should easily access relevant information for their needs, such as preparation tips for extreme weather conditions. The dashboard should display air quality data in a clear format, with labels and descriptions for clarity. The solution must also integrate previous research data for reuse by the modern generation.

## Risks
The Health Advice Group must ensure that developers follow GDPR, Human Rights, and Care Act laws, and properly encrypt any sensitive data. If legal requirements are ignored, the company could face lawsuits, legal fines, and loss of public trust. To mitigate these risks, the company should train developers or hire legal professionals to review the app before launch.

## Wider Issues

### Legal Considerations
- **GDPR**: This regulation ensures data privacy and user consent for data collection. If the app stores sensitive user information on servers, GDPR compliance is critical.
- **Care Act**: The Care Act ensures the client meets care and support responsibilities.
- **Human Rights Act**: Protects users' rights, ensuring that the app provides truthful, non-discriminatory information.

### Ethical Considerations
- There may be concerns about personalized health advice, especially when some users feel the advice is biased.
- Environmental concerns could arise if development leads to destruction of nature, such as deforestation for infrastructure projects.

### Social Considerations
- The solution can help reduce health issues caused by environmental factors like asthma, respiratory problems, or heart disease. It can warn users of potential health risks such as landfill gas exposure, helping them stay safe.

### Software Considerations
- The decision on whether to use open-source or proprietary software will impact how the app is used, updated, and customized by developers. Open-source offers transparency and the potential for community contributions, while proprietary software is more secure but less customizable.

## Risks
The company must meet legal requirements to avoid legal troubles. Failing to meet system requirements may lead to poor adoption, negatively impacting trust and future use. To mitigate legal risks, the company should train developers in relevant laws and regulations or hire a legal team.

## Overall Justification of System

## Appendix

### Hardware
- Sensors, trackers, wearables, ECG, defibrillators, bedside monitors.

### Software
- Electronic Health Record (EHR) Software, Medical Imaging Software.

### Emerging Technologies
- AI, 3D printing, nano-medicine.

### Medical Devices
- Equipment such as MRI and CT scanners, patient monitoring systems, and portable diagnostic tools.
- Wearable devices for remote monitoring of patients' vital signs.

### Regulatory Frameworks
- **General Data Protection Regulation (GDPR)**: Protects personal data privacy.
- **Human Rights Act**: Ensures fair treatment in healthcare.
- **NHS Act**: Governs NHS operations and promotes transparency.
- **Care Act**: Outlines care responsibilities and emphasizes personalized care.
- **Inquiries Act**: Regulates public health inquiries and ensures accountability.
