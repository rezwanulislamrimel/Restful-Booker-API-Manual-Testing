<div align="center">

<img src="https://img.shields.io/badge/API%20Testing-Restful%20Booker-0A3C5E?style=for-the-badge&logo=postman&logoColor=white" alt="Project Banner"/>

# 🏨 Restful Booker — API Testing Project

> A structured API testing suite built with **Postman** & **Newman** for the Restful Booker platform — covering full CRUD operations with automated HTML reporting.

<br/>

[![Postman](https://img.shields.io/badge/Postman-FF6C37?style=flat-square&logo=postman&logoColor=white)](https://www.postman.com/)
[![Newman](https://img.shields.io/badge/Newman-CLI%20Runner-6BA539?style=flat-square&logo=npm&logoColor=white)](https://www.npmjs.com/package/newman)
[![Node.js](https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=node.js&logoColor=white)](https://nodejs.org/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=flat-square)](LICENSE)
[![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)]()

</div>

---

## 📌 Overview

This project is created for **practicing real-world API testing** using industry-standard tools. It covers the complete booking lifecycle of the [Restful Booker API](https://restful-booker.herokuapp.com/apidoc/index.html) — from authentication to CRUD operations — with automated test execution and beautiful HTML reports.

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| 🟧 **Postman** | API request design & manual testing |
| ⚡ **Newman** | CLI-based automated test runner |
| 🟩 **Node.js** | Runtime environment for Newman |
| 📊 **HTMLExtra Reporter** | Rich visual test reports |

---

## 📁 Project Structure

```
Manual API Testing/
│
├── 📂 newman/                               # Auto-generated HTML reports
│   └── report.html
│
├── 📄 New Collection.postman_collection.json   # Postman test collection (v2.1)
└── 📄 README.md                             # Project documentation
```

---

## ✅ API Coverage

| # | Method | Endpoint | Description |
|---|--------|----------|-------------|
| 1 | `POST` | `/auth` | 🔐 Generate auth token |
| 2 | `POST` | `/booking` | ➕ Create new booking |
| 3 | `GET` | `/booking` | 📋 Get all bookings |
| 4 | `GET` | `/booking/{id}` | 🔍 Get booking by ID |
| 5 | `PUT` | `/booking/{id}` | 🔄 Full update booking |
| 6 | `PATCH` | `/booking/{id}` | ✏️ Partial update booking |
| 7 | `DELETE` | `/booking/{id}` | 🗑️ Delete booking |

---

## 🚀 How to Run Tests

### Step 1 — Install Newman

```bash
npm install -g newman
```

### Step 2 — Install HTMLExtra Reporter

```bash
npm install -g newman-reporter-htmlextra
```

### Step 3 — Run the Collection

```bash
newman run "New Collection.postman_collection.json" -r cli,htmlextra
```

> 💡 **Tip:** Run from the project folder where the `.json` file is located.

---

## 📊 View Test Report

After execution, the HTML report is saved inside:

```
newman/
└── New Collection-YYYY-MM-DD-HH-MM-SS-000-0.html
```

Open the `.html` file in any browser for a detailed visual report including:
- ✅ Pass / ❌ Fail summary
- Response time graphs
- Request/response details per test

---

## ⚠️ Important Notes

- Always export Postman collection in **v2.1 format**
- Keep the `.json` file in the **same directory** where you run Newman
- Use **quotes** around file names that contain spaces
- Verify the API is reachable before running tests: [https://restful-booker.herokuapp.com](https://restful-booker.herokuapp.com)

---

## 🐛 Common Issues & Fixes

| Error | Cause | Fix |
|-------|-------|-----|
| `ENOENT` | Collection file not found | Check file path & working directory |
| `Assertion failed` | Expected vs actual mismatch | Review test assertions in Postman |
| `401 Unauthorized` | Invalid or expired token | Re-run auth request to get fresh token |
| `newman: command not found` | Newman not installed globally | Run `npm install -g newman` |

---

## 👤 Author

<div align="center">

**Rezwanul Rimel**

*Built for learning & practicing real-world API testing workflows.*

---

⭐ *If this project helped you, consider giving it a star!* ⭐

</div>
