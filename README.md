# Building-Machine-Learning-APIs-With-FastAPI

## Sepsis Prediction Using Machine Learning

### Overview
This project focuses on developing and deploying a machine learning model to predict sepsis in patients, a life-threatening condition that can lead to severe organ damage and increased mortality if not promptly treated. By leveraging a robust dataset of patient features, this project aims to revolutionize healthcare delivery through early detection, diagnosis, and management of sepsis.

The project follows the Cross Industry Standard Process for Data Mining (CRISP-DM) framework to ensure a structured approach. The trained machine learning model is deployed as an API using FastAPI, a modern Python web framework known for its efficiency and support for asynchronous capabilities. The API enables healthcare professionals to input patient data and receive real-time predictions on sepsis likelihood, empowering timely medical interventions.

### 1. Introduction
Sepsis is a critical condition triggered by the body's response to infection, leading to tissue and organ damage if not identified and treated promptly. This project utilizes machine learning techniques to predict sepsis by analyzing patient data, providing healthcare professionals with actionable insights for timely interventions.

### 2. Project Framework: CRISP-DM
The project is guided by the CRISP-DM framework, which includes the following phases:

Business Understanding: Understand the project's objectives, focusing on predicting sepsis onset in ICU patients using patient data.
Data Understanding: Explore and familiarize with the dataset, which includes 599 patient records across 11 columns such as vital signs, blood work results, BMI, age, and the target variable indicating sepsis status.
Data Preparation: Process the dataset for machine learning, including scaling, encoding, splitting into training/testing sets, and addressing class imbalance with SMOTE.
Modeling: Train and evaluate various machine learning models, including Logistic Regression, Random Forest, and Gradient Boosting.
Evaluation: Assess model performance using metrics like accuracy, precision, recall, F1-score, and ROC curve analysis.
Deployment: Deploy the trained model as an API using FastAPI and Docker for containerization.

### 3. Data Preparation
During this phase, the dataset was meticulously processed to optimize it for machine learning algorithms. Key steps included:

Scaling: Numerical features were scaled to ensure uniformity across the dataset.
Encoding: Categorical variables were encoded for model compatibility.
Splitting: The dataset was divided into training and testing sets to evaluate model performance.
Class Imbalance: The class imbalance was addressed using the Synthetic Minority Over-sampling Technique (SMOTE), generating synthetic samples to balance the dataset.

### 4. Modeling
The project involved training and evaluating multiple machine learning models to identify the most effective algorithm for sepsis prediction. The following classifiers were considered:

Logistic Regression: Known for its simplicity and interpretability.
Random Forest: An ensemble method that improves predictive accuracy and controls overfitting.
Gradient Boosting: An advanced ensemble technique that builds models sequentially, correcting errors made by previous models.
Model performance was assessed using accuracy, precision, recall, and F1-score, with Gradient Boosting emerging as the top performer, followed closely by Random Forest.

### 5. Evaluation
The selected models underwent rigorous evaluation to ensure their efficacy and generalizability. The Random Forest model consistently outperformed others based on the ROC curve, with a higher area under the curve (AUC), demonstrating its reliability in predicting sepsis onset.

### 6. Deployment Using FastAPI
The final phase involved deploying the trained model as an API using FastAPI, which offers efficient and asynchronous capabilities. Key features include:

Real-Time Predictions: Healthcare professionals can input patient data and receive instant predictions regarding sepsis likelihood.
Docker Containerization: The API and frontend were containerized using Docker, enabling easy scaling and updates.
By containerizing the application, we ensured that it runs consistently across different environments and can be easily scaled or updated as needed.

### 7. Conclusion
This project underscores the transformative impact of machine learning in healthcare, particularly in predicting and managing life-threatening conditions like sepsis. By deploying advanced predictive models through FastAPI, healthcare providers can proactively identify at-risk patients, intervene promptly, and improve patient outcomes.

### 8. Future Directions
Future iterations of this project could explore integrating additional data sources, such as genomic information or real-time physiological data streams, to enhance predictive accuracy and refine clinical decision-making. Continuous refinement and validation of the model with larger and more diverse datasets will be crucial to its ongoing effectiveness in real-world healthcare settings.

## Getting Started
### Prerequisites
Python 3.10.11
FastAPI
Docker

## Installation

Clone the repository: git clone https://github.com/michaelodumanye/sepsis-prediction.git
cd sepsis-prediction

Install dependencies: pip install -r requirements.txt

Run the FastAPI server: uvicorn api:app --reload

Build and run Docker container: docker build -t sepsis-prediction-api .
docker run -p 8000:8000 sepsis-prediction-api

### Usage
Access the API by navigating to http://localhost:8000/docs in your web browser. Use the provided endpoints to input patient data and receive sepsis predictions.

### Contributing
Contributions are welcome! Please submit a pull request or open an issue to discuss any changes.

### License
This project is licensed under the MIT License

