# Open-Weather-Map-API-DIKA
This repository contains API automation tests for OpenWeatherMap API using Katalon Studio. It covers:

✅ 5-Day Weather Forecast for Jakarta Selatan
✅ Current Air Pollution Data for Jakarta Selatan

All test scenarios are implemented following best practices with JSON schema validation and assertions to ensure correctness.

📌 Project Structure
pgsql
Copy
Edit
Open-Weather-Map-API
│── .gitignore
│── README.md
│── Test Cases/
│   ├── API/
│   │   ├── TC_Get_Weather_Forecast
│   │   ├── TC_Get_Air_Pollution
│── Object Repository/
│   ├── API/
│   │   ├── Get_Weather_Forecast
│   │   ├── Get_Air_Pollution
│── Data Files/
│   ├── JSONSchemas/
│   │   ├── Weather_Forecast_Schema.json
│   │   ├── Air_Pollution_Schema.json
│── Test Suites/
│   ├── API_Test_Suite
│── GlobalVariable/
│   ├── GlobalVariables
│── Reports/ (Generated after running tests)
📂 Explanation of Key Files
Test Cases/API/TC_Get_Weather_Forecast → Test case to fetch 5-day weather forecast.
Test Cases/API/TC_Get_Air_Pollution → Test case to fetch air pollution data.
Object Repository/API/ → API requests are stored here.
Data Files/JSONSchemas/ → JSON schemas for response validation.
Test Suites/API_Test_Suite → Collection of test cases to run as a suite.
GlobalVariable/GlobalVariables → Stores API Base URL & API Key.
📥 Prerequisites
✅ Install Katalon Studio → Download Here
✅ Create an OpenWeatherMap API Key → Get API Key
✅ Ensure Git is Installed → Check using git --version

🚀 Steps to Run the Test
1️⃣ Clone the Repository
bash
Copy
Edit
git clone https://github.com/Teguh-Ardama/Open-Weather-Map-API-DIKA.git
cd Open-Weather-Map-API-DIKA
2️⃣ Open the Project in Katalon Studio
Launch Katalon Studio
Click File → Open Project
Select the cloned Open-Weather-Map-API-DIKA folder
3️⃣ Set Up Global Variables
Open Profiles > Default
Set the values for:
BASE_URL → https://api.openweathermap.org/data/2.5/
API_KEY → Your API Key from OpenWeatherMap
4️⃣ Run Individual Test Cases
Open Test Cases/API/TC_Get_Weather_Forecast
Click Run (Choose API/Web Service)
OR

Open Test Cases/API/TC_Get_Air_Pollution
Click Run (Choose API/Web Service)
5️⃣ Run the Full API Test Suite
Open Test Suites/API_Test_Suite
Click Run
📊 How to Get the Report?
Generate Report in Katalon
After running a test, go to Reports folder
Reports are automatically saved as HTML, JUnit, or PDF
To view reports:
Click "Reports" on the left panel
Select a test run and view the results
Export Report to PDF or HTML
Click "Reports" in Katalon Studio
Right-click a test result → Select "Export as PDF"
🔍 Key Features in the Test Cases
✅ Validates HTTP Status Code (200 OK)
✅ Asserts JSON Schema for API Responses
✅ Checks Essential Response Data (e.g., temperature, humidity, air quality)
✅ Handles API Rate Limits by using Best Practices
