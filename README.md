# House Price Prediction using MLOps

## Project Overview
This project is a Machine Learning-based House Price Prediction web application. It uses a trained machine learning model to predict house prices based on user-provided input features. The application is built using Flask and Scikit-learn, containerized with Docker, and deployed on AWS EC2.

## Technologies Used
- **Python** — Programming language
- **Scikit-learn** — Machine learning model
- **Flask** — Web application framework
- **Pandas & NumPy** — Data processing
- **Docker** — Application containerization
- **AWS EC2** — Cloud deployment
- **GitHub** — Version control and project hosting

## Project Structure

```text
mlops-house-price/
├── app.py
├── requirements.txt
├── Dockerfile
├── models/
│   └── model.pkl
└── templates/
    └── index.html
```

## Features
- Predicts house prices through a web interface
- Uses a trained Random Forest Regression model
- Displays prediction results to the user
- Supports Docker-based deployment
- Hosted on an AWS EC2 instance

## Run Locally

### 1. Clone the repository
```bash
git clone https://github.com/YOUR-USERNAME/mlops-house-price.git
cd mlops-house-price
```

Replace `YOUR-USERNAME` with your GitHub username.

### 2. Create and activate a virtual environment
```bash
python -m venv venv
```

Windows PowerShell:
```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Run the application
```bash
python app.py
```

Open your browser at `http://127.0.0.1:5000`.

## Run with Docker

Build the Docker image:
```bash
docker build -t house-price-app .
```

Run the container:
```bash
docker run -d --name house-price-container -p 80:5000 house-price-app
```

Open `http://localhost` in your browser.

## AWS Deployment
The application is deployed on an AWS EC2 Ubuntu instance using Docker. The EC2 security group must allow inbound HTTP traffic on port 80 to access the web application.

## Machine Learning Model
The project uses a Random Forest Regression model trained on the California Housing dataset to generate house price predictions.
