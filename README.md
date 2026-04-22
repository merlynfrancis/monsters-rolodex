<div align="center">

# 👹 Monsters Rolodex

### _A flip-book of friendly monsters, summoned from thin air._

A playful React app that conjures an army of quirky monster avatars out of a public API,
sticks them on trading cards, and lets you hunt through the horde with live search.
Small project, big vibes — a classic for learning React fundamentals the fun way.

[![Live Demo](https://img.shields.io/badge/👾_See_the_Monsters-monstersrolodex.netlify.app-00C853?style=for-the-badge)](https://monstersrolodex.netlify.app/)
[![React](https://img.shields.io/badge/React-16-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://react.dev/)
[![JavaScript](https://img.shields.io/badge/JavaScript-ES6-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Netlify](https://img.shields.io/badge/Deployed_on-Netlify-00C7B7?style=for-the-badge&logo=netlify&logoColor=white)](https://www.netlify.com/)

</div>

---

## 🧟 What is this?

**Monsters Rolodex** takes a boring list of fake users (from [JSONPlaceholder](https://jsonplaceholder.typicode.com/)) and transforms each one into a **one-of-a-kind monster card** using [Robohash](https://robohash.org/) avatars. Then it hands you a search box and says: _go find your favorite monster._

Built as a fundamentals-first React project, it's small on scope but rich on concepts:

- 🧠 **Class components** with state & lifecycle (`componentDidMount`)
- 🔎 **Controlled inputs** for real-time filtering
- 🧩 **Component composition** — `App` → `SearchBox` + `CardList` → `Card`
- 🌐 **External API consumption** via `fetch`
- 🎨 **Pure CSS** styling with Grid for that rolodex feel

---

## ✨ Features

| | |
|---|---|
| 👹 **Instant Monster Generation** | Every user gets a unique Robohash avatar — no two are alike |
| 🔍 **Live Search** | Filter the rolodex as you type — no submit button needed |
| 💳 **Card-based UI** | Clean, uniform monster "trading cards" with name and email |
| 📱 **Responsive Grid** | Cards reflow nicely across screen sizes |
| ⚡ **Zero Config** | Just `npm start` and you're in |

---

## 🛠️ Built With

<div align="center">

| Category | Stack |
|---|---|
| **Library** | React 16 (class components) |
| **Tooling** | Create React App (react-scripts) |
| **Styling** | Vanilla CSS + CSS Grid |
| **Data Source** | [JSONPlaceholder](https://jsonplaceholder.typicode.com/users) |
| **Avatars** | [Robohash](https://robohash.org/) (set2 — "monsters") |
| **Deployment** | Netlify |

</div>

---

## 📁 Project Structure

```
monsters-rolodex/
├── public/                         Static shell — index.html, favicon, manifest
└── src/
    ├── components/
    │   ├── card/
    │   │   ├── card.component.jsx      Single monster card (avatar + name + email)
    │   │   └── card.styles.css
    │   ├── card-list/
    │   │   ├── card-list.component.jsx Grid of all monster cards
    │   │   └── card-list.styles.css
    │   └── search-box/
    │       ├── search-box.component.jsx Controlled search input
    │       └── search-box.styles.css
    ├── App.js                      Root component — fetches data & holds state
    ├── App.css                     App-level layout
    ├── index.js                    React entry point
    └── index.css                   Global resets
```

---

## 🔬 How it Works

```txt
1. App mounts
       ↓
2. componentDidMount() fetches users from JSONPlaceholder
       ↓
3. State fills with monsters — each has id, name, email
       ↓
4. SearchBox updates `searchField` on every keystroke
       ↓
5. filteredMonsters recomputes on every render
       ↓
6. CardList maps the filtered array into Card components
       ↓
7. Each Card pulls its avatar from:
      https://robohash.org/<id>?set=set2&size=180x180
```

No Redux. No hooks. No backend. Just React, doing React things. 🧘

---

## 🚀 Running Locally

**Prerequisites:** Node.js 14+ (older is fine for React 16) and npm or yarn

```bash
# 1. Clone the repo
git clone https://github.com/merlynfrancis/monsters-rolodex.git
cd monsters-rolodex

# 2. Install dependencies
npm install

# 3. Start the dev server
npm start
```

Your browser should pop open at [http://localhost:3000](http://localhost:3000) — and the monsters will be waiting. 👁️

### Other commands

```bash
npm run build     # Production build into /build
npm test          # Run test suite
npm run deploy    # Deploy to GitHub Pages (uses gh-pages)
```

---

## 🌐 Deployment

Live version is hosted on **Netlify** at [monstersrolodex.netlify.app](https://monstersrolodex.netlify.app/).

To deploy your own:

- **Netlify:** Connect the repo → build command `npm run build` → publish directory `build/`
- **GitHub Pages:** `npm run deploy` (already wired up via `gh-pages`)
- **Vercel:** Import the repo and leave defaults — it just works

---

## 📚 Credits

Inspired by the [ZTM React Complete Guide](https://www.zerotomastery.io/) course — a great starter project for anyone getting into React.

Huge thanks to the free APIs that power this:
- 🤖 [Robohash](https://robohash.org/) — for giving every monster a face
- 📦 [JSONPlaceholder](https://jsonplaceholder.typicode.com/) — for the endless supply of fake users

---

<div align="center">

### Crafted with 💚 by [@merlynfrancis](https://github.com/merlynfrancis)

_If you made it this far, you probably like monsters. Drop a ⭐ on the repo and make one very happy._

</div>
