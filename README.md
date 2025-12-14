# 🚀 Cypress API Automation Framework (JWT Auth + CRUD)

A **production-grade Cypress API automation framework** built using **service-layer architecture**, **JWT authentication**, and **reusable request handlers**.
Designed to reflect **real-world QA/SDET practices** used in FAANG-level teams.

---

## 📌 Key Highlights

* ✅ JWT **Bearer Token authentication**
* ✅ **Service-based API abstraction** (no raw `cy.request()` in tests)
* ✅ Full **CRUD API coverage**
* ✅ Scalable & maintainable folder structure
* ✅ Clean separation of concerns (Tests vs APIs)
* ✅ Git-ready & CI-friendly

---

## 🧰 Tech Stack

| Tool             | Purpose        |
| ---------------- | -------------- |
| Cypress          | API Automation |
| JavaScript (ES6) | Test Logic     |
| Node.js          | Runtime        |
| REST APIs        | Backend        |
| JWT              | Authentication |

---

## 🏗️ Framework Architecture

```
cypress/
 ├── e2e/
 │   └── studentApi.cy.js      # Test scenarios
 ├── support/
 │   ├── api/
 │   │   └── studentApi.js     # API service layer
 │   └── commands.js
 ├── fixtures/
 └── cypress.config.js
```

**Why this matters (FAANG standard):**

* Tests focus only on **assertions**
* API logic stays **centralized**
* Easy to scale for 50+ endpoints

---

## 🔐 Authentication Strategy

* Login API generates JWT token
* Token stored once using:

```js
Cypress.env('token')
```

* Automatically injected into all secured APIs via:

```js
Authorization: Bearer <token>
```

This mimics **real enterprise security flows**.

---

## 🔁 Reusable Authorization Layer

```js
const authHeader = () => ({
  Authorization: `Bearer ${Cypress.env('token')}`,
  'Content-Type': 'application/json'
})
```

✔ Eliminates duplication
✔ Improves readability
✔ Simplifies maintenance

---

## 📡 API Test Coverage

| Method | Endpoint        | Description         |
| ------ | --------------- | ------------------- |
| POST   | `/students`     | Create student      |
| GET    | `/students`     | Fetch all students  |
| GET    | `/students/:id` | Fetch student by ID |
| PUT    | `/students/:id` | Full update         |
| PATCH  | `/students/:id` | Partial update      |
| DELETE | `/students/:id` | Delete student      |

---

## 🧪 Test Design Principles

* No hardcoded headers in tests
* Assertions only in spec files
* API contracts validated via response body & status
* Independent & reusable test flows

---

## ▶️ Execution

### Install dependencies

```
npm install
```

### Start backend

```
npm start
```

### Run Cypress

```
npx cypress open
```

or

```
npx cypress run
```

---

## 📈 Why This Framework Stands Out

* Mirrors **real FAANG QA frameworks**
* Ready for **CI/CD integration**
* Easy onboarding for new team members
* Ideal for **SDET / Automation Engineer roles**

---

## 📂 GitHub Repository

🔗 [https://github.com/vinodpanzade/API_auth_CRUD](https://github.com/vinodpanzade/API_auth_CRUD)

---

## 👨‍💻 Author

**Vinod Panzade**
QA Automation Engineer | Cypress | API Testing | SDET

---

## 🧠 Learning Outcomes

* API auto
