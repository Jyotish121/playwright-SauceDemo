# 🚀 Playwright SauceDemo Automation Framework

This project is an automated testing framework built using Playwright and JavaScript for testing the SauceDemo web application.  
It also includes GitHub Actions CI/CD integration for automatic test execution on every push and pull request.

---

# 📌 Features

✅ UI Automation using Playwright  
✅ Cross-browser testing support  
✅ Headed and Headless execution  
✅ HTML Test Reports  
✅ GitHub Actions CI/CD Integration  
✅ Easy project structure  
✅ Fast and reliable test execution  

---

# 🛠️ Tech Stack

- JavaScript
- Node.js
- Playwright
- GitHub Actions

---

# 📂 Project Structure

```text
playwright-SauceDemo
│
├── .github
│   └── workflows
│       └── playwright.yml
│
├── tests
│   ├── login.spec.js
│   ├── cart.spec.js
│   └── checkout.spec.js
│
├── playwright-report
├── test-results
├── node_modules
│
├── package.json
├── package-lock.json
├── playwright.config.js
└── README.md
```

---

# ⚙️ Installation & Setup

## 1️⃣ Clone Repository

```bash
git clone https://github.com/your-username/playwright-SauceDemo.git
```

---

## 2️⃣ Open Project Folder

```bash
cd playwright-SauceDemo
```

---

## 3️⃣ Install Dependencies

```bash
npm install
```

---

## 4️⃣ Install Playwright Browsers

```bash
npx playwright install
```

---

# ▶️ Running Tests

## Run All Tests

```bash
npx playwright test
```

---

## Run Tests in Headed Mode

```bash
npx playwright test --headed
```

---

## Run Specific Test File

```bash
npx playwright test tests/login.spec.js
```

---

## Run Tests in Specific Browser

### Chromium

```bash
npx playwright test --project=chromium
```

### Firefox

```bash
npx playwright test --project=firefox
```

### WebKit

```bash
npx playwright test --project=webkit
```

---

# 📊 HTML Report

## Generate and Open Report

```bash
npx playwright show-report
```

---

# 🔄 GitHub Actions CI/CD

This project uses GitHub Actions for Continuous Integration and Continuous Deployment (CI/CD).

The workflow automatically runs:
- On every push to `main` branch
- On every pull request

---

# 📍 Workflow File Location

```text
.github/workflows/playwright.yml
```

---

# 📄 Sample GitHub Actions Workflow

```yaml
name: Playwright Tests

on:
  push:
    branches:
      - main

  pull_request:
    branches:
      - main

jobs:
  test:
    runs-on: ubuntu-latest

    steps:
      - name: Checkout Repository
        uses: actions/checkout@v4

      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 20

      - name: Install Dependencies
        run: npm install

      - name: Install Playwright Browsers
        run: npx playwright install --with-deps

      - name: Run Playwright Tests
        run: npx playwright test

      - name: Upload HTML Report
        uses: actions/upload-artifact@v4
        if: always()
        with:
          name: playwright-report
          path: playwright-report/
```

---

# 🧪 Test Scenarios Covered

- Login Functionality
- Add to Cart
- Remove from Cart
- Product Validation
- Checkout Flow
- Form Validation
- UI Validation

---

# 📸 Reports & Results

After GitHub Actions execution:
1. Open GitHub Repository
2. Click on `Actions`
3. Open latest workflow run
4. Download HTML Report from Artifacts section

---

# 👨‍💻 Author

## Shruti Yedke
