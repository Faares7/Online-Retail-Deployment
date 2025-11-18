# **🛒 Online Retail Predictor**

- A machine learning project that predicts total invoice value for an online retail dataset.
- The project includes a FastAPI backend, a simple HTML/CSS/JS frontend, and is containerized with Docker for easy deployment. 🚀

## **Table of Contents 📚**

- Project Overview

- Features

- Project Structure

- Installation

- Usage

- API Endpoints

- Docker Deployment

- Contributing

- License

## **Project Overview 📝**

This project trains a **Random Forest Regressor** on an online retail dataset and deploys it as an API using **FastAPI**.

A simple frontend allows users to input data and get predictions.💡

The workflow includes:

    1. Preprocessing the dataset (preprocess.py) 🔄

    2. Training the model (train.py) 🏋️‍♂️

    3. Saving the trained model (model.joblib) 💾

    4. Serving predictions through an API (app.py) 🌐

    5. Frontend interaction via HTML/CSS/JS (static/) 🖥️

## **Features ✨**

- Predict invoice total based on:

        1. Quantity 📦

        2. Unit Price 💲

        3. Invoice Month 📅

        4. Country 🌍

- FastAPI backend for serving predictions ⚡

- Simple frontend for user interaction 🖱️

- Fully containerized for deployment using Docker 🐳

## **Project Structure 📂**

a full detailed project structure can be viewed in the pipeline.txt file.

## **Installation** 🛠️

    1. Clone the repository

        git clone https://github.com/Faares7/Online-Retail-Deployment.git
        cd Online-Retail-Deployment

    2. Create a Python environment to install required dependecies
            
        pip install -r requirements.txt

    3. Usage 🚀

        1. Preprocess the dataset :

                python src/preprocess.py
                - This will create src/processed/retail_processed.csv. ✅

        2. Train the model

                python src/train.py
                - The trained model will be saved as src/model.joblib. 💾

        3. Run the FastAPI server

                cd src/api
                uvicorn app:app --reload --host 0.0.0.0 --port 8000
                - Open browser and go to: http://127.0.0.1:8000 🌐
                - Your API is now live.

        4. Open the frontend

                - Open src/static/index.html in a browser 🖥️
                - Enter input values and click Predict 🎯

## **API Endpoints**

**Root:**

GET /

Returns a welcome message. 👋

**Predict:**

POST /predict

    Request Body Example:

    {"Quantity": 5,"UnitPrice": 20.5,"InvoiceMonth": 6,"Country": 1}

    Response Example:

    {
    "prediction": 102.5
    }


## **License ⚖️**

This project is licensed under the Fares's License. 📝
