# **Live User Search — API‑Powered Filtering UI**

A simple, responsive, real‑time search interface that loads user data from the JSONPlaceholder API and filters results instantly as the user types. This project demonstrates practical use of `fetch()`, DOM manipulation, event handling, and dynamic UI updates.

---

## 🚀 **Features**

- Fetches user data from **JSONPlaceholder** on page load  
- Displays users as clean, readable cards  
- Live filtering by:
  - **Name**
  - **Email**
  - **Company**
- Case‑insensitive search  
- Real‑time result count:  
  **“Showing X of 10 users”**
- Loading state while fetching  
- Error handling for failed requests  
- “No users found” message when filters match zero users  

---

## 📸 **Preview**

The interface includes:

- A loading message  
- Three search inputs  
- A dynamic result count  
- User cards showing:
  - Name  
  - Email  
  - Company  

Search updates instantly as you type.

---

## 🧠 **How It Works**

### 1. **Fetch Users**
On page load, the script fetches all users from:

```
https://jsonplaceholder.typicode.com/users
```

The data is stored in `allUsers` so filtering happens locally without re-fetching.

### 2. **Render Cards**
A `renderUsers()` function clears the container and rebuilds user cards from a given array.

### 3. **Live Filtering**
Each search input listens for the `input` event.  
On every keystroke:

- The script reads all three search fields  
- Normalizes them with `.trim().toLowerCase()`  
- Filters `allUsers` using `.includes()`  
- Re-renders only the matching users  
- Updates the result count  
- Shows “No users found” when appropriate  

### 4. **Loading & Error States**
- “Loading users…” appears before the fetch completes  
- “Users loaded!” appears on success  
- “Error loading users.” appears if the request fails  

---

## 🛠️ **Tech Stack**

- **HTML** — structure  
- **CSS** — basic styling  
- **JavaScript** — fetch, filtering, DOM updates  
- **JSONPlaceholder API** — mock user data  

---

## 📂 **Project Structure**

```
live_search.html
└── Contains all HTML, CSS, and JavaScript in one file
```

---

## 📘 **Requirements Satisfied**

✔ Fetch users on load  
✔ Display name, email, company  
✔ Live search (name, email, company)  
✔ Case-insensitive filtering  
✔ Result count  
✔ Loading state  
✔ Error handling  
✔ “No users found” message  

---

## 📄 **Usage**

Simply open `live_search.html` in any modern browser.  
No build tools or dependencies required.

