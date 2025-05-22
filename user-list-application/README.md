# Lists and Keys

- Lists
  - Preparing Data
  - Rendering lists
- Keys
  - Adding Unique Key
  - Key Attribute

To set up a **React** project using **Vite**, follow these steps:

---

### ✅ Prerequisites

Make sure you have the following installed:

- **Node.js** (v14.18+, v16+ recommended)
  You can check your version by running:

  ```bash
  node -v
  ```

---

### ⚙️ Step-by-Step Installation

1. **Create a new project with Vite:**

   ```bash
   npm create vite@latest my-react-app -- --template react
   ```

   > Replace `my-react-app` with your desired project name.

2. **Navigate to your project folder:**

   ```bash
   cd my-react-app
   ```

3. **Install dependencies:**

   ```bash
   npm install
   ```

4. **Start the development server:**

   ```bash
   npm run dev
   ```

   > You should see something like `Local: http://localhost:5173/`

---

### 📁 Project Structure

Here's a quick look at what you get:

```
my-react-app/
├─ public/
├─ src/
│  ├─ App.css
│  ├─ App.jsx
│  ├─ main.jsx
├─ index.html
├─ package.json
├─ vite.config.js
```

---

### 🚀 Production Build

When you're ready to build for production:

```bash
npm run build
```

This will generate a `dist` folder with optimized static assets.

---

Let me know if you want to add TypeScript, Tailwind CSS, or other tools!
