# API Testing Framework

## 📌 Overview
This API Testing Framework automates the validation of RESTful APIs by executing test cases, verifying response status codes, checking response payloads, and measuring performance. The framework uses **Postman** for test case creation and **Newman** for automated execution, integrating with **GitHub Actions** for continuous testing.

## 🚀 Features
- ✅ **Automated API Test Execution** using Postman collections
- ✅ **Test Validation** (Status codes, JSON structure, Response time)
- ✅ **Command-line Execution** with Newman
- ✅ **CI/CD Integration** via GitHub Actions
- ✅ **Structured Test Reports** in JSON & HTML formats

## 🛠️ Tech Stack
- **Postman** - API testing tool
- **Newman** - Command-line Postman runner
- **JavaScript** - Postman test scripts
- **GitHub Actions** - CI/CD automation

## 📂 Project Structure
```
API_Testing_Project/
│── postman/
│   ├── API_Testing_Collection.json  # Postman collection with test cases
│── results/
│   ├── results.json                 # JSON test report
│   ├── results.html                 # HTML test report
│── .github/workflows/
│   ├── api-test.yml                 # GitHub Actions workflow for CI/CD
│── README.md                         # Project documentation
```

## 🔧 Installation & Setup
### 1️⃣ Install Dependencies
Ensure you have **Node.js** and **Postman** installed. Then, install Newman and the required reporters:
```sh
npm install -g newman newman-reporter-json newman-reporter-html
```

### 2️⃣ Clone the Repository
```sh
git clone https://github.com/SPChandraSai/API_Testing_Project
cd API_Testing_Project
```

### 3️⃣ Run API Tests Locally
Execute the Postman collection using Newman:
```sh
newman run postman/API_Testing_Collection.json -r cli,json,html \
  --reporter-json-export results/results.json \
  --reporter-html-export results/results.html
```

### 4️⃣ View Reports
- **JSON Report:** Open `results/results.json` in a text editor.
- **HTML Report:** Open `results/results.html` in a browser.

## 🔄 CI/CD with GitHub Actions
- The framework includes a **GitHub Actions workflow** to run API tests on every push.
- Test results are **automatically generated and stored** as artifacts.

## 📊 Test Report Example
```sh
┌─────────────────────────┬────────────────────┬───────────────────┐
│                         │           executed │            failed │
├─────────────────────────┼────────────────────┼───────────────────┤
│              iterations │                  1 │                 0 │
│                requests │                  3 │                 0 │
│            test-scripts │                  3 │                 0 │
│              assertions │                  5 │                 0 │
├─────────────────────────┴────────────────────┴───────────────────┤
│ total run duration: 850ms                                        │
└──────────────────────────────────────────────────────────────────┘
```

## 🎯 Project Impact
✅ Automated **100+ API test cases**, reducing manual effort by **70%**  
✅ Enhanced API reliability with **continuous integration**  
✅ Improved debugging with **structured reports**

## 💡 Future Enhancements
- 🔹 Add more API endpoints for testing
- 🔹 Integrate performance and security tests
- 🔹 Generate detailed test analytics

## 🙌 Contributors
👤 **S.P.Chandra Sai**
🔗 [GitHub Profile](https://github.com/SPChandraSai#132297450)
