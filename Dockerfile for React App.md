# ✅ Dockerfile (Production-ready)
Create a file named Dockerfile in  **~/prasanth-poultry**
```
vi Dockerfile
```
✅ IMPORTANT (Before Build)

Make sure **dist** exists (you already have it 👍)

### 🔹 Dockerfile content
```
# Step 1: Use Nginx official image
FROM nginx:alpine

# Step 2: Remove default Nginx website
RUN rm -rf /usr/share/nginx/html/*

# Step 3: Copy Vite build output to Nginx web root
COPY dist/ /usr/share/nginx/html/

# Step 4: Expose port 80
EXPOSE 80

# Step 5: Start Nginx
CMD ["nginx", "-g", "daemon off;"]
```
✅ Build Docker Image & Verify:
```
docker build -t prasanth-poultry .
docker images
```
✅ Run Docker Container & Check:
```
docker run -d -p 80:80 --name prasanth-poultry-app prasanth-poultry
docker ps
```
✅ Access Website
```
Open browser: http://<EC2_PUBLIC_IP>
```
🎉 Your React website is now live using Docker + Nginx

## 🔍 Common Issues & Fixes
❌ Only blank page?

Check inside container:
```
docker exec -it prasanth-poultry-app ls /usr/share/nginx/html
```
You should see:
```
index.html
assets/
```


