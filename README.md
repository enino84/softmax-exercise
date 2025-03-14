# 🚀 Softmax Exercise

This repository contains a hands-on coding exercise where you will **implement a Softmax layer** in Python. This activation layer/function is a crucial component in neural networks for multi-class classification.

The exercise runs **entirely inside a Docker container**, ensuring a consistent execution environment.

---

## 📖 Overview

In this exercise, you will:

✔️ Implement the **softmax function** from scratch.  
✔️ Ensure **numerical stability** for large input values.  
✔️ Validate your implementation using **unit tests**.  
✔️ Run and test your function inside a **Jupyter Notebook**.  

---

## 🛠️ Running the Exercise with Docker

### **1️⃣ Clone the Repository**
```sh
git clone https://github.com/YOUR_USERNAME/softmax-exercise.git
cd softmax-exercise
```

### **2️⃣ Build the Docker Image**
```sh
docker build -t softmax-exercise .
```

### **3️⃣ Run the Docker Container**

Use the appropriate command based on your operating system:

#### **For Linux/macOS or Git Bash (Windows):**
```sh
docker run -p 8888:8888 -v $(pwd):/app softmax-exercise
```

#### **For Windows (PowerShell):**
```powershell
docker run -p 8888:8888 -v ${PWD}:/app softmax-exercise
```

#### **For Windows (CMD):**
```cmd
docker run -p 8888:8888 -v %cd%:/app softmax-exercise
```

This command starts the container and launches **Jupyter Notebook**.

### **4️⃣ Open the Jupyter Notebook**
Once the container is running, open your browser and go to:
```
http://localhost:8888
```
Then, open **`softmax_exercise.ipynb`** and follow the instructions.

---

## **📂 Repository Structure**
```
softmax-exercise/
│── Dockerfile             # Docker configuration
│── requirements.txt       # Dependencies for the project
│── softmax_exercise.ipynb # Jupyter Notebook with the exercise
│── README.md              # Instructions for running the project
```

---

## 🛠️ Dockerfile

For reference, this is the **Dockerfile** used in this project:

```dockerfile
# Use an official lightweight Python image
FROM python:3.9

# Set the working directory inside the container
WORKDIR /app

# Copy dependency file and install required packages
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy all project files into the container
COPY . .

# Expose the Jupyter Notebook port
EXPOSE 8888

# Run Jupyter Notebook and keep the container alive
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root", "--NotebookApp.token=''", "--NotebookApp.notebook_dir=/app"]
```

---

## 🎯 Next Steps
✅ Implement the **Softmax function** inside `softmax_exercise.ipynb`.  
✅ Run the provided **unit tests** to verify correctness.  

---

## 📜 License
This project is open-source under the **MIT License**.

---

### 🎉 You’re all set! Launch the container and start coding! 🚀

