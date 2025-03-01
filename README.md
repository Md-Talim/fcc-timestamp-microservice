# Timestamp Microservice  

A simple **Node.js** and **Express.js** API that returns **Unix** and **UTC timestamps** for a given date. This project is part of freeCodeCamp's **Back End Development and APIs** certification.  

## 🚀 Features

- Returns the **current timestamp** when no date is provided.  
- Accepts both **Unix timestamps** and **date strings** as input.  
- Returns timestamps in **both Unix and UTC formats**.  
- Handles **invalid dates** gracefully.  
- CORS-enabled for remote testing.  

## 🛠️ Installation  

1. **Clone the repository**  
   ```bash
   git clone https://github.com/your-username/timestamp-microservice.git
   cd timestamp-microservice
   ```

2. **Install dependencies**  
   ```bash
   npm install
   ```

3. **Start the server**  
   ```bash
   npm start
   ```
   The server will run on **http://localhost:3000** by default.

## 📡 API Usage  

### **Get the current timestamp**  
**Request:**  
```http
GET /api
```
**Response:**  
```json
{
  "unix": 1672531199000,
  "utc": "Fri, 31 Dec 2022 23:59:59 GMT"
}
```

### **Get timestamp for a specific date**  
**Request:**  
```http
GET /api/2015-12-25
```
**Response:**  
```json
{
  "unix": 1451001600000,
  "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
}
```

### **Get timestamp for a Unix timestamp**  
**Request:**  
```http
GET /api/1451001600000
```
**Response:**  
```json
{
  "unix": 1451001600000,
  "utc": "Fri, 25 Dec 2015 00:00:00 GMT"
}
```

### **Handling invalid dates**  
**Request:**  
```http
GET /api/invalid-date
```
**Response:**  
```json
{
  "error": "Invalid Date"
}
```
