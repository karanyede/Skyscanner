# 🛠️ Hoen Scanner - Rental Cars & Hotels Microservice

A lightweight Java microservice built with **Dropwizard** that serves combined search results of rental cars and hotels based on the user's city input.

---

## 📌 Table of Contents

- [🔍 About the Project](#-about-the-project)
- [📁 Project Structure](#-project-structure)
- [⚙️ Tech Stack](#-tech-stack)
- [🚀 Getting Started](#-getting-started)
- [📡 API Usage](#-api-usage)
- [🧪 Testing with Postman](#-testing-with-postman)
- [✅ Features](#-features)
- [📌 Status](#-status)
- [📎 Author](#-author)

---

## 🔍 About the Project

Hoen Scanner is a simple microservice that allows users to search for rental cars and hotels in different cities.

- Built using **Dropwizard**.
- Reads static data from `rental_cars.json` and `hotels.json`.
- Exposes a REST API to **POST** a city name and returns filtered search results.

---

## 📁 Project Structure

📦hoen-scanner ┣ 📂src ┃ ┗ 📂main ┃ ┃ ┣ 📂java/com/yourcompany/hoenscanner ┃ ┃ ┃ ┣ 📜HoenScannerApplication.java ┃ ┃ ┃ ┣ 📜Search.java ┃ ┃ ┃ ┣ 📜SearchResult.java ┃ ┃ ┃ ┗ 📜SearchResource.java ┃ ┃ ┗ 📂resources ┃ ┃ ┃ ┣ 📜rental_cars.json ┃ ┃ ┃ ┗ 📜hotels.json ┗ 📜pom.xml


---

## ⚙️ Tech Stack

- **Java 19**
- **Dropwizard**
- **Jackson** (for JSON serialization/deserialization)
- **Maven**
- **Postman** (for testing)

---

## 🚀 Getting Started

### Prerequisites

- Java JDK 19
- IntelliJ IDEA (recommended)
- Maven
- Postman

---

### Setup Instructions

```bash``'
# Clone the repository
git clone https://github.com/yourusername/hoen-scanner.git
cd hoen-scanner

Open the project in IntelliJ IDEA.

Load the Maven project when prompted.

Ensure JDK 19 is configured.

Run HoenScannerApplication.java.

If you see Welcome to Hoen Scanner! in the logs, you’re good to go 🚀

📡 API Usage
POST /search
Search for available rental cars and hotels in a specific city.

🔸 Request Headers
pgsql
Copy
Edit
Content-Type: application/json
🔸 Request Body
json
Copy
Edit
{
  "city": "petalborough"
}
🔸 Example Response
json
Copy
Edit
[
  {
    "city": "petalborough",
    "kind": "rental",
    "title": "Swift Rentals"
  },
  {
    "city": "petalborough",
    "kind": "hotel",
    "title": "Hotel Petal Palace"
  }
]
# 🧠 Note: City names are case-insensitive (e.g., Petalborough, petalborough, or PETALBOROUGH will all work).

### 🧪 Testing with Postman
Open Postman.

Create a new POST request:

bash
Copy
Edit
http://localhost:8080/search
Under the Body tab:

Choose raw

Select JSON format

Paste:

json
Copy
Edit
{
  "city": "shaleport"
}
Hit Send and receive filtered results.

✅ Features
 Load hotel and rental car data from JSON

 Use Jackson for JSON parsing

 Implement Dropwizard RESTful API

 Filter data based on city input

 Test with Postman

📌 Status
🎉 Fully functional microservice complete and tested.

📎 Author
Made with 💖 by Karan
