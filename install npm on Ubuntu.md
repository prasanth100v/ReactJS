# Create a React project.
## ✅ Install Node.js + npm via NodeSource (Best & Latest)
> This installs Node.js and npm together (stable & up-to-date).
### 1️⃣ Update system
```
sudo apt update
sudo apt upgrade -y
```
### 2️⃣ Install required packages
```
sudo apt install -y curl
```
### 3️⃣ Add NodeSource repository (LTS version)
```
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
```
### 4️⃣ Install Node.js & npm
```
sudo apt install -y nodejs
```
### 5️⃣ Verify installation
```
node -v
npm -v
```
✔️ Output like:
```
v20.x.x
10.x.x
```
## ✅ Create React Project using Vite (Recommended ⭐)
🔹 Prerequisites
```
Make sure these are installed:
Node.js (v18+ recommended)
npm (comes with Node.js)
```
### 1️⃣ Create React project using Vite
```
npm create vite@latest prasanth-poultry -- --template react     #Creates a new folder called "prasanth-poultry"
```
You’ll see prompts:
```
✔ Select a framework: React
✔ Select a variant: JavaScript
```
### 🔹 After this, your folder looks like:
```
prasanth-poultry/
├── index.html
├── package.json
├── vite.config.js
├── src/
│   ├── App.jsx
│   ├── main.jsx
│   └── assets/
└── public/
```
### 2️⃣ Move into project folder
```
cd prasanth-poultry
```
👉 Now all next commands run inside your React project
### 3️⃣ Install dependencies
```
npm install
```
🔹 What happens : Downloads all required packages
> Creates: node_modules/ && package-lock.json

### 4️⃣ Start development server
```
npm run dev
```
🔹 Expected output
```
VITE vX.X.X  ready in XXX ms

➜  Local:   http://localhost:5173/
➜  Network: http://<your-ip>:5173/
```
### 5️⃣ Open in browser
```
http://localhost:5173
```
🎉 You should see ***Vite + React*** welcome page
> ✏️ Modify Your App (Test)

## Build for Production
```
npm run build
```
Output will be in:
```
dist/
├── index.html
├── assets/
```
You can deploy this using Nginx, Docker.



