# Create GitHub Actions Workflow
Create folders:
```
mkdir -p .github/workflows
nano .github/workflows/build.yml
```
## ✅ GitHub Actions CI (FINAL)

name: Build React App and Commit Dist
```
on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      # 1️⃣ Checkout code
      - name: Checkout repository
        uses: actions/checkout@v4
        with:
          persist-credentials: true

      # 2️⃣ Setup Node.js
      - name: Setup Node.js
        uses: actions/setup-node@v4
        with:
          node-version: 20

      # 3️⃣ Install dependencies
      - name: Install dependencies
        run: npm ci

      # 4️⃣ Build Vite project
      - name: Build project
        run: npm run build
```




