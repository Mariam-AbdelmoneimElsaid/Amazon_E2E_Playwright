# Amazon E2E Automation – Playwright

This project is an end-to-end (E2E) automation framework built using **Playwright Test**
to validate critical user flows on an Amazon-like e-commerce website.

The main test scenario focuses on searching for a product, sorting results by price,
navigating to product details, and validating product information.

---

## 🧪 Tech Stack
- Playwright Test
- TypeScript
- Node.js
- Docker & Docker Compose
- Page Object Model (POM) concepts

---

## 🎯 Test Scenario Overview
The automated test covers the following flow:

- Open Amazon website
- Search for **"Nikon"** using the search bar
- Sort search results by **Price: High to Low**
- Select the second product from the results list
- Verify that the product title contains **"Nikon D3X"**

Assertions are used to ensure that the expected product details are displayed correctly.

---

## 📂 Project Structure
.
├── tests/ # End-to-end test cases
├── playwright.config.ts # Playwright configuration
├── Dockerfile
├── docker-compose.yml
├── run-tests.sh
├── package.json
└── README.md

yaml
Copy code

---

## ⚙️ Configuration

### Base URL
The base URL is configurable and can be updated in:
- `playwright.config.ts`
  
Or overridden at runtime using an environment variable.

Example:
```bash
BASE_URL="https://www.amazon.co.uk/" npx playwright test
▶️ How to Run Locally
1️⃣ Install dependencies
bash
Copy code
npm install
npx playwright install --with-deps
2️⃣ Run tests (headed mode)
bash
Copy code
npx playwright test --headed
3️⃣ Run tests (headless mode – default)
bash
Copy code
npx playwright test
4️⃣ View HTML report
bash
Copy code
npx playwright show-report
🐳 Run Tests Using Docker
Make sure Docker is installed, then from the project root run:

bash
Copy code
docker compose up --build
The HTML test report will be available at:

arduino
Copy code
http://localhost:9323
The container will keep running until stopped manually.

🌍 Execution Environments
Local machine (headed or headless)

Docker container

CI-ready structure (can be integrated with GitHub Actions)

📝 Notes
Playwright auto-waiting is used instead of explicit waits.

The framework is designed to be easily extended with more test cases.

The project focuses on demonstrating real-world E2E automation practices.

🚀 Future Enhancements
Add more product-based test scenarios

Improve stability for CI execution

Integrate GitHub Actions for automated test runs

Enhance reporting and test annotations

👩‍💻 Author
Mariam Abd Elmoneim
Automation QA Engineer


