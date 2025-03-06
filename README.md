🌤 OpenWeatherMap API Automation Testing
📌 Overview
OpenWeatherMap API Automation Testing adalah proyek otomatisasi pengujian berbasis Katalon Studio yang digunakan untuk menguji API dari OpenWeatherMap.
Proyek ini mencakup pengujian untuk skenario berikut:

✅ Get 5-Day Weather Forecast for Jakarta Selatan
✅ Get Current Air Pollution Data for Jakarta Selatan

Pengujian ini mencakup validasi:

Response Body
JSON Schema Validation
Status Code
Response Time
📂 Project Structure
javascript
Copy
Edit
OpenWeatherMap-API-Testing/
│── Profiles/
│   ├── default
│── Test Cases/
│   ├── API/
│   │   ├── TC_Get_Air_Pollution
│   │   ├── TC_Get_Weather_Forecast
│   │   ├── TC_Validate_JSON_Schema
│── Object Repository/
│   ├── Weather/
│   │   ├── GET_Get_Air_Pollution
│   │   ├── GET_Get_Weather_Forecast
│── Test Suites/
│   ├── TS_OpenWeather
│── Data Files/
│── Checkpoints/
│── Keywords/
│── Test Listeners/
│── Reports/
│── TestOps/
│── Include/
│── Plugins/
│── .gitignore
│── build.gradle
│── console.properties
│── README.md
🔧 Prerequisites
Pastikan Anda telah menginstal berikut sebelum menjalankan pengujian:

Katalon Studio (Versi terbaru) – Download Katalon
Akun OpenWeatherMap untuk mendapatkan API Key – Daftar di OpenWeatherMap
Git (opsional) untuk versi kontrol dan kolaborasi
🚀 How to Run
1️⃣ Clone Repository
bash
Copy
Edit
git clone https://github.com/USERNAME/OpenWeatherMap-API-Testing.git
cd OpenWeatherMap-API-Testing
2️⃣ Buka Proyek di Katalon Studio
File → Open Project
Pilih folder OpenWeatherMap-API-Testing
3️⃣ Set Up API Key dan Variabel
Buka Profiles → default
Tambahkan variabel berikut:
BASE_URL = https://api.openweathermap.org/data/2.5/
API_KEY = YOUR_OPENWEATHERMAP_API_KEY
LAT = -6.2615 (Latitude Jakarta Selatan)
LON = 106.8106 (Longitude Jakarta Selatan)
4️⃣ Jalankan Test Case Individu
Navigasi ke "Test Cases/API"
Klik kanan pada TC_Get_Air_Pollution atau TC_Get_Weather_Forecast
Pilih Run
5️⃣ Jalankan Test Suite
Buka Test Suites → TS_OpenWeather
Klik Run
📊 Generating Reports
Setelah pengujian selesai, laporan dapat diakses melalui:

Katalon Studio → Reports
Format yang tersedia:
JUnit Report
HTML Report
PDF Report
📜 API Testing Details
🟢 TC_Get_Weather_Forecast
🔹 Request:

Endpoint: /forecast
Method: GET
Query Params:
lat=${LAT}
lon=${LON}
appid=${API_KEY}
🔹 Assertions:
✅ Status Code = 200
✅ Response Time < 2s
✅ Validate JSON Schema
✅ Temperature, humidity, wind speed exist in response body

🟢 TC_Get_Air_Pollution
🔹 Request:

Endpoint: /air_pollution
Method: GET
Query Params:
lat=${LAT}
lon=${LON}
appid=${API_KEY}
🔹 Assertions:
✅ Status Code = 200
✅ Response Time < 2s
✅ Validate JSON Schema
✅ pm2_5, pm10, o3 exist in response body

🛠 Troubleshooting
Error: "Nothing to geocode"

Pastikan parameter lat dan lon valid
Error: "401 Unauthorized"

Pastikan API Key valid dan memiliki akses ke endpoint yang digunakan
📌 Contributors
👨‍💻 Your Name – QA Engineer

📜 License
This project is licensed under the MIT License – see the LICENSE file for details.
