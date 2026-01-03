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






