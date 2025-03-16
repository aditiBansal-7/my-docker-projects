# My-Docker-Projects
This repository serves as a **central hub** for all my **Docker, Kubernetes, and ML projects**. Each project is containerized, well-documented, and includes step-by-step deployment instructions.  

📌 **Technologies Used:**  
✅ Docker & Docker Compose 🐳  

✅ MySQL & PostgreSQL Databases 🗄️  

✅ Streamlit for UI 📊  

✅ ML Model Deployment & Monitoring 🤖  

✅ Kubernetes with Minikube & Kubectl ⚙️  


---

## 📂 Project List  

| 🔹 Project | 📌 Description | 🔗 Repo Link |
|------------|--------------|--------------|
| **1️⃣ Docker Basics** | Learn fundamental Docker commands and concepts | [https://github.com/aditiBansal-7/Docker-Basics] |
| **2️⃣ Docker ML Mushroom Classifier** | Deploy an ML model for mushroom classification using Docker | [https://github.com/aditiBansal-7/docker-ml-mushroom-classifier] |
| **3️⃣ MySQL using Docker** | Set up and run MySQL inside a Docker container | [https://github.com/aditiBansal-7/MySQL-using-Docker] |
| **4️⃣ Docker Volume Persistence** | Persist data across containers using Docker volumes | [https://github.com/aditiBansal-7/docker-volume-persistence-] |
| **5️⃣ Docker Container Communication** | Set up container-to-container communication in Docker | [https://github.com/aditiBansal-7/docker-container-communication] |
| **6️⃣ Streamlit & PostgreSQL in Docker** | Deploy a Streamlit app connected to PostgreSQL using Docker | [https://github.com/aditiBansal-7/Streamlit-PostgreSQL-in-docker] |
| **7️⃣ ML Monitoring Dashboard** | Monitor ML models using Streamlit and Evidently AI | [https://github.com/aditiBansal-7/ml-monitoring-dashboard] |
| **8️⃣ Minikube & Kubectl Lab** | Set up a local Kubernetes cluster and deploy apps | [https://github.com/aditiBansal-7/minikube-kubectl-lab] |
| **9️⃣ ML Model Deployment using Docker & EC2** | Deploy a Dockerized ML Model using Streamlit on AWS EC2 | https://github.com/aditiBansal-7/Docker_ec2.git |

---

## **1️⃣ Docker Basics 🐳 ** 
📌 **Goal:** Learn essential Docker concepts, commands, and best practices.  

🔹 **Topics Covered:**  
- What is Docker?
- Installing Docker  
- Running containers (`docker run`)  
- Managing images (`docker pull`, `docker build`)  
- Stopping & removing containers  

📜 **Commands:**  
```sh
docker run -it ubuntu bash
docker ps -a
docker images
docker stop container_id
docker rm container_id
```
🔗 Repository: [https://github.com/aditiBansal-7/Docker-Basics]

## **2️⃣ Docker ML Mushroom Classifier 🍄🤖**  

📌 Goal: Deploy an ML model that classifies mushrooms as edible or poisonous using Docker.

🔹 Project Steps:  

✅ Train the model using Scikit-Learn  

✅ Create a Flask API for inference  

✅ Containerize the model using Docker  


📜 Setup:

```sh
docker build -t mushroom-classifier .
docker run -p 5000:5000 mushroom-classifier
```
🔗 Repository:[https://github.com/aditiBansal-7/docker-ml-mushroom-classifier]

## **3️⃣ MySQL using Docker 🗄️**  

📌 Goal: Run a MySQL database inside a Docker container.  

📜 Setup Commands:

```sh
docker run --name mysql_container -e MYSQL_ROOT_PASSWORD=root -d mysql
docker exec -it mysql_container mysql -u root -p
```
🔗 Repository: [https://github.com/aditiBansal-7/MySQL-using-Docker]

## **4️⃣ Docker Volume Persistence 💾**  

📌 Goal: Learn how to persist data across Docker containers.

🔹 Key Concepts:  

✔ Bind Mounts (host-based persistence)  

✔ Docker Volumes (managed by Docker)

📜 Commands:

```sh
docker run -v /mydata:/container_data ubuntu touch /container_data/sample.txt
docker inspect container_id | grep Mounts
```
🔗 Repository: [https://github.com/aditiBansal-7/docker-volume-persistence-]

## **5️⃣ Docker Container Communication 🌐**  

📌 Goal: Enable communication between multiple Docker containers using networking.

🔹 Topics Covered:

Docker bridge networks  

Connecting multiple containers  

Inspecting network configurations  

📜 Commands:

```sh
docker network create my_network
docker network connect my_network container1
docker inspect my_network
```
🔗 Repository: [https://github.com/aditiBansal-7/docker-container-communication]

## **6️⃣ Streamlit & PostgreSQL in Docker 🎨📊**  

📌 Goal: Deploy a Streamlit app connected to a PostgreSQL database using Docker.

🔹 Project Setup:  

1️⃣ Run PostgreSQL inside Docker  

2️⃣ Create a database & table  

3️⃣ Connect Streamlit to PostgreSQL  

4️⃣ Deploy the app inside a container  


📜 Commands:

```sh
docker network create my_postgres_network
docker run --name my_postgres -e POSTGRES_USER=admin -e POSTGRES_DB=mydb -d postgres
docker build -t streamlit_app .
docker run --network my_postgres_network -p 8501:8501 -d streamlit_app
```
🔗 Repository: [https://github.com/aditiBansal-7/Streamlit-PostgreSQL-in-docker]

## **7️⃣ ML Monitoring Dashboard 📊🤖**  

📌 Goal: Monitor ML models in production using Streamlit & Evidently AI.  


🔹 Features:  

✔ Data drift detection (feature distribution changes)  

✔ Performance tracking (accuracy, precision, recall)  

✔ Live data monitoring  

✔ Statistical insights with visual reports  


📜 Setup & Execution:

```sh
git clone https://github.com/aditiBansal-7/ml-monitoring-dashboard.git
cd ml-monitoring-dashboard
python -m venv .venv
source .venv/bin/activate
pip install -r streamlit-app/requirements.txt
streamlit run streamlit-app/app.py
```
🔗 Repository: [https://github.com/aditiBansal-7/ml-monitoring-dashboard]

## **8️⃣ Minikube & Kubectl Lab 🏗️🔥**  

📌 Goal: Set up and manage a Kubernetes cluster locally using Minikube & Kubectl.  


🔹 Topics Covered:  

✔ Starting a Minikube cluster  

✔ Deploying applications on Kubernetes  

✔ Exposing services with NodePort  

✔ Scaling deployments  


📜 Setup Commands:  


```sh
minikube start
kubectl create deployment nginx --image=nginx
kubectl expose deployment nginx --type=NodePort --port=80
minikube service nginx --url
kubectl scale deployment nginx --replicas=3
kubectl delete service nginx
kubectl delete deployment nginx
```
🔗 Repository: [https://github.com/aditiBansal-7/minikube-kubectl-lab]

**9️⃣ ML Model Deployment Using Docker & EC2 🐳🌍**
📌 Goal: Deploy an ML model that classifies mushrooms as edible or poisonous using Docker and host it on AWS EC2.

🔹 Topics Covered:

✔ Setting up an AWS EC2 instance

✔ Installing Docker on EC2

✔ Deploying a Dockerized ML Model

✔ Running the Streamlit Web App

✔ Enabling automatic restart for the container

📜 Setup Commands:

# Step 1: Connect to EC2 via SSH
```
ssh -i /path/to/your-key.pem ec2-user@your-ec2-public-ip
```

# Step 2: Install Docker on EC2
```
sudo yum update -y
sudo yum install docker -y
sudo service docker start
sudo usermod -a -G docker ec2-user
exit  # Log out and log back in for changes to take effect
```

# Step 3: Clone the project and build the Docker image
```
git clone https://github.com/aditiBansal-7/Docker_ec2.git
cd ml-docker-app
docker build -t streamlit-app .
```

# Step 4: Run the Streamlit App in a Docker Container
```
docker run -d -p 8501:8501 --name my-streamlit-app streamlit-app
```

# Step 5: Ensure the app restarts automatically after reboot
```
sudo docker update --restart unless-stopped my-streamlit-app
```
📌 Access the Web App:
👉 Open your browser and visit http://your-ec2-public-ip:8501

🔗 Repository: [https://github.com/aditiBansal-7/Docker_ec2.git]


🔗 Summary  

✅ **Docker Basics** – Core Docker concepts  

✅ **ML Mushroom Classifier** – ML model deployment  

✅ **MySQL in Docker** – Database in a container  

✅ **Docker Volumes** – Data persistence  

✅ **Container Communication** – Networking in Docker  

✅ **Streamlit & PostgreSQL** – Web app with a database  

✅ **ML Monitoring Dashboard** – Model performance tracking  

✅ **Minikube & Kubectl** – Kubernetes setup & deployment  

✅ **ML Model Deployment Using Docker & EC2** – Deploying and hosting an ML model on Amazon EC2



 

