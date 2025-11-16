🎯 API Testing with Postman – Booking API

A complete Postman-based API testing project demonstrating real-world CRUD testing, environment handling, scripts, and token-based authentication.

✨ Key Highlights

🚀 Fully functional Booking API test suite

🔄 Complete CRUD workflow (Create, Read, Update, Delete)

🔐 Automated Token generation & cookie-based authentication

📁 Dynamic Postman Environment (baseurl, id, token)

🧪 Built-in test scripts for data extraction

👨‍💻 Beginner-friendly yet industry-standard setup

📂 Project Files
📦 API Testing with Environment
 ┣ 📄 Basic.postman_collection.json
 ┗ 📄 Batch 24.postman_environment.json

📘 Postman Collection

Contains all API requests with scripts to capture variables.
File: Basic.postman_collection.json

🌍 Postman Environment

Stores dynamic variables (baseurl, id, token).
File: Batch 24.postman_environment.json

🔧 Setup Guide
1️⃣ Import Files into Postman

Go to File → Import

Select both JSON files

Choose the environment Batch 24

2️⃣ Set Base URL

Open environment and set:

baseurl = https://restful-booker.herokuapp.com


Or your custom API server.

🧪 API Workflow
1️⃣ Create Booking

➡ POST {{baseurl}}/booking/
✔ Saves bookingid to {{id}}

2️⃣ Get Booking

➡ GET {{baseurl}}/booking/{{id}}
✔ Fetches booking info

3️⃣ Generate Access Token

➡ POST {{baseurl}}/auth
✔ Saves token to {{token}}

4️⃣ Update Booking

➡ PUT {{baseurl}}/booking/{{id}}
Requires Header:

Cookie: token={{token}}

5️⃣ Delete Booking

➡ DELETE {{baseurl}}/booking/{{id}}
Requires Header:

Cookie: token={{token}}

📜 Example: Create Booking Body
{
  "firstname": "Asif",
  "lastname": "Rahman",
  "totalprice": 111,
  "depositpaid": true,
  "bookingdates": {
    "checkin": "2025-01-01",
    "checkout": "2025-02-01"
  },
  "additionalneeds": "Breakfast"
}

🛠 Tech Stack
Tool	Purpose
Postman	API Testing
JavaScript (Postman Scripts)	Test & Pre-request scripts
REST API	Booking API
JSON	Request/Response handling


