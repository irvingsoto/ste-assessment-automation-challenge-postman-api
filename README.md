# ste-assessment-automation-challenge-postman-api

# Benefits Dashboard API – Postman Collection (Newman Runner)

This repository contains a **Postman collection** for testing the **Benefits Dashboard API**.  
The tests can be executed locally using [Newman](https://github.com/postmanlabs/newman) or in **GitHub Actions** for CI/CD automation.  

---

## 📦 Setup

### 1. Clone the repository
```
git clone <repo-url>
cd <repo-name>
```

2. Install Newman

Install Newman, the Postman CLI runner:

`npm install -g newman`


⸻

▶️ Running Tests Locally

The repository includes:
	•	benefits-dashboard-API.postman_collection.json → Postman collection of API tests
	•	dashboard-prod.postman_environment.json → Postman environment with variables

Run the collection:

`newman run benefits-dashboard-API.postman_collection.json -e dashboard-prod.postman_environment.json`

Optional: Generate an HTML report

Install the Newman HTML reporter:

`npm install -g newman-reporter-htmlextra`

The report will be saved in the newman/ folder.

⸻

⚡ Running Tests in GitHub Actions

This project includes a GitHub Actions workflow:
employee-api-tests.yml

You can run the tests directly in GitHub Actions:

```Steps:
	1.	Navigate to your repository’s Actions tab.
	2.	Select Employee API Tests workflow (employee-api-tests.yml).
	3.	Click Run workflow → select branch → click Run.
	4.	View results in the workflow summary. Reports (if enabled) will be available as artifacts.
```
⸻

📂 Project Structure

```
.
├── benefits-dashboard-API.postman_collection.json   # Postman test collection
├── dashboard-prod.postman_environment.json          # Postman environment (production)
├── employee-api-tests.yml                           # GitHub Actions workflow
└── README.md                                        # Documentation
```

