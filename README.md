## 📋 Description

Comprehensive API testing project for **Restful Booker API** - a hotel reservation system. Demonstrates professional API testing with 100+ automated test cases covering functional testing, negative scenarios, and full booking lifecycle workflows.

---

## 🎯 What Was Tested and Why

### Functional Testing
- **CRUD operations** - Create, Read, Update, Delete bookings
- **Authentication** - Token generation and Basic Auth
- **Filtering** - Search by name, date range
- **Multiple formats** - JSON, XML payloads

**Why:** Verify core API functionality works as documented

### Negative Testing
- Invalid data types, missing fields, malformed payloads
- Boundary values, unsupported formats
- Error handling validation

**Why:** Ensure API handles errors gracefully and prevents bad data

### Integration Testing
- Full booking lifecycle: Create → Verify → Update → Patch → Delete
- Data consistency across endpoints

**Why:** Validate realistic workflows and data integrity

---

<!--## 🤖 What Was Automated and Why

**Automated:**
- ✅ Status code validation (200, 201, 404, 400)
- ✅ Response schema validation
- ✅ Data integrity checks
- ✅ Dynamic variables (bookingId, tokens)
- ✅ Test data cleanup
- ✅ Response time monitoring

**Why:** Speed (100+ tests in seconds), consistency, regression testing, CI/CD ready, scalability

----->

## 🛠️ Tools Used and Why

| Tool | Purpose | Why |
|------|---------|-----|
| **Postman** | API testing | Industry standard, powerful scripting |
| **Newman** | CLI automation | CI/CD integration |
| **Newman HTML Extra** | Test reporting | Professional reports with metrics |
| **JavaScript** | Test scripting | Built-in Postman support |
| **Git/GitHub** | Version control | Portfolio demonstration |

---

## 🚀 How to Run Tests
<img width="2559" height="1334" alt="postman" src="https://github.com/user-attachments/assets/6edd5503-7c1b-4ed0-91d1-875ed6e0c017" />

### Prerequisites
```bash
npm install -g newman newman-reporter-htmlextra
```

### Method 1: Postman (Manual)
1. Import `collections/Restful_Booker_Test_Collection.postman_collection.json`
2. Import `environments/Restful_Booker_Environment.postman_environment.json`
3. Click `Run` → `Run Restful Booker Test Collection`

### Method 2: Newman CLI (Automated)

**Basic:**
```bash
newman run collections/Restful_Booker_Test_Collection.postman_collection.json
```

**With environment:**
```bash
newman run collections/Restful_Booker_Test_Collection.postman_collection.json \
  -e environments/Restful_Booker_Environment.postman_environment.json
```

**With HTML report:**
```bash
newman run collections/Restful_Booker_Test_Collection.postman_collection.json \
  -e environments/Restful_Booker_Environment.postman_environment.json \
  -r htmlextra \
  --reporter-htmlextra-export reports/test-report.html
```

**Windows:**
```powershell
newman run collections/Restful_Booker_Test_Collection.postman_collection.json -e environments/Restful_Booker_Environment.postman_environment.json -r htmlextra --reporter-htmlextra-export reports/report.html
```

---

## 📊 Test Results

- **Total Requests:** 45+
- **Total Assertions:** 100+
- **Execution Time:** 5-8 seconds
- **Coverage:** All endpoints + edge cases
<img width="2559" height="1163" alt="newman" src="https://github.com/user-attachments/assets/c780aa0e-37ba-4a74-a5fa-aa145c21b750" />
