# 🍔 Foodie-WAYS

> **A Priority Queue (Max-Heap) Demonstration via a Food Ordering System**

![Next.js](https://img.shields.io/badge/Next.js-16-black?logo=next.js)
![React](https://img.shields.io/badge/React-19-61DAFB?logo=react)
![JavaScript](https://img.shields.io/badge/JavaScript-ES2022-F7DF1E?logo=javascript)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 📌 About The Project

**Foodie-WAYS** is an interactive full-stack web application built with **Next.js 16** and **React 19** that demonstrates the **Priority Queue (Max-Heap)** data structure in a real-world food ordering context.

The application simulates a restaurant dispatch system where orders are **prioritized by urgency score and VIP status**, showcasing core heap operations live in the browser — no installation required.

---

## 🧠 Core Concept — Max-Heap Priority Queue

The heart of this project is a **from-scratch Max-Heap** implemented in pure JavaScript (`src/lib/PriorityQueue.js`).

| Operation | Method | Complexity |
|-----------|--------|-----------|
| Add order to queue | `insert()` + `heapifyUp()` | **O(log N)** |
| Dispatch highest-priority order | `extractMax()` + `heapifyDown()` | **O(log N)** |
| View next order (no removal) | `peek()` | **O(1)** |
| Get full queue state | `getQueueState()` | **O(1)** |

### Priority Scoring
- **VIP Customer** → Base score **1000** + random(0–50) = `1000–1049`
- **Regular Customer** → Base score **0** + random(0–50) = `0–49`

VIP orders always bubble to the top of the heap, ensuring they are always dispatched first.

---

## 🖥️ Pages & Features

### 🏠 Landing Page (`/`)
- Dark, high-end food photography aesthetic
- Hero section: *"Hunger Meets Speed"*
- 3 feature cards highlighting O-notation benefits
- Team credits footer

### 📊 Admin Dashboard (`/dashboard`)
A live **3-column DSA demonstration**:

```
[ Incoming Orders ]  →  [ Priority Algorithm ]  →  [ Processing Engine ]
   OrderForm              QueueVisualizer             extractMax() + Kitchen
```

---

## 🔌 API Routes

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/queue` | `GET` | Fetch current heap state |
| `/api/queue` | `POST` | Add a new order (insert into heap) |
| `/api/process` | `POST` | Dispatch highest-priority order (extractMax) |

---

## 📁 Project Structure

```
src/
├── app/
│   ├── page.js                  ← Landing Page
│   ├── layout.js                ← Root layout
│   ├── globals.css
│   ├── landing.module.css
│   ├── dashboard/
│   │   ├── page.js              ← Admin Dashboard (main DSA demo)
│   │   └── page.module.css
│   └── api/
│       ├── queue/route.js       ← GET + POST orders
│       └── process/route.js     ← POST extractMax
├── components/
│   ├── OrderForm.js             ← Order input form
│   ├── OrderForm.module.css
│   ├── QueueVisualizer.js       ← Live heap visualizer
│   └── QueueVisualizer.module.css
└── lib/
    └── PriorityQueue.js         ← Max-Heap algorithm (core)
```

---

## 🚀 Getting Started

### Prerequisites
- Node.js v18+
- npm v9+

### Installation & Run

```bash
# Clone the repository
git clone https://github.com/duakshita/Foodie-WAYS.git
cd Foodie-WAYS

# Install dependencies
npm install

# Start development server
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Build for Production

```bash
npm run build
npm start
```

---

## 🛠️ Tech Stack

| Technology | Version | Role |
|-----------|---------|------|
| Next.js | ^16.2.3 | Full-stack framework (App Router + API routes) |
| React | ^19.2.5 | UI and state management |
| JavaScript | ES2022 | Algorithm + frontend logic |
| CSS Modules | Built-in | Component-scoped styling |
| Node.js crypto | Built-in | UUID generation for order IDs |

---

## 👥 Team

| Name | UID |
|------|-----|
| Pawni | 25BCS10187 |
| Akshita | 25BCS11560 |
| Aayushi | 25BCS10261 |

**Subject:** Advanced Data Structure (25CSH-202)  
**Submitted to:** Mr. MD Tauseef

---

## 📄 License

This project is for academic purposes under the Advanced Data Structure course.
