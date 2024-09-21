🌍 Planet Habitability Predictor


A Machine Learning-Powered Website to Predict Exoplanet Habitability
Welcome to the Planet Habitability Predictor! This project combines machine learning with web development to assess whether an exoplanet could be habitable based on user-provided data such as temperature, gravity, and atmospheric composition.

Table of Contents
Project Overview
Features
Project Structure
Installation and Setup
Step-by-Step Guide
Technologies Used
How to Use
Future Improvements
Project Overview
The Planet Habitability Predictor allows users to input parameters of an exoplanet, and then the website uses a machine learning model to predict whether that planet could be habitable. This tool is aimed at promoting interest in astrobiology and space exploration through an engaging, interactive platform.

Features
Input form for entering planetary data such as temperature, mass, and atmospheric composition.
Real-time prediction using a machine learning model.
Visualization of prediction confidence (optional).
Simple and intuitive user interface.
Project Structure
bash
Copy code
├── ml_model/              # Contains the machine learning model
├── website/               # Flask web application
│   ├── templates/         # HTML templates for the front-end
│   ├── static/            # CSS, JS, and images
├── README.md              # This file
├── requirements.txt       # Required Python packages
└── app.py                 # Main Flask application file
Installation and Setup
Prerequisites
Make sure you have the following installed:

Python 3.x
Pip (Python package manager)
Flask
Scikit-learn
Pandas
Numpy
Step 1: Clone the Repository
bash
Copy code
git clone https://github.com/yourusername/planet-habitability-predictor.git
cd planet-habitability-predictor
Step 2: Install Required Libraries
Install the necessary Python packages by running the following command:

bash
Copy code
pip install -r requirements.txt
Step 3: Train or Load the ML Model
You can either:

Train the model: Use the provided train_model.py script to train a new model using your exoplanet dataset.
Use the pre-trained model: The ml_model/model.pkl file contains a pre-trained Random Forest model for predicting habitability.
If training, run the following command:

bash
Copy code
python train_model.py
Step 4: Run the Web Application
Start the Flask server to serve the website:

bash
Copy code
python app.py
Step 5: Access the Website
Open your browser and go to http://127.0.0.1:5000/ to access the Planet Habitability Predictor website.

Step-by-Step Guide
Step 1: Prepare Dataset and Train the ML Model
Gather or use a pre-existing dataset of exoplanets. The dataset should contain features like planet mass, surface temperature, atmospheric composition, etc.
Preprocess the data using Pandas and split it into training and testing sets.
Train a machine learning model (Random Forest, Logistic Regression, etc.) using Scikit-learn to predict habitability.
Save the trained model as a .pkl file to be used in the Flask application.
Step 2: Build the Flask Web Application
Set up Flask:
Create an app.py file and set up basic Flask routes for the homepage and result page.
Create the Input Form:
In the templates/ folder, create index.html, which includes an input form where users can enter planetary data (e.g., temperature, mass, gravity).
Display Prediction:
Upon form submission, the data is sent to the server where the ML model processes it and returns a prediction.
Display the result on a new page or within the same form.
Step 3: Style the Website
Use CSS to make the website visually appealing. You can store stylesheets in the static/ folder.
Optionally, add JavaScript to enhance interactivity.
Step 4: Integrate the ML Model
Load the pre-trained ML model (model.pkl) in app.py.
Process user input and make predictions using the model.
Send the prediction result back to the front end to display the habitability prediction.
Step 5: Test the Application
Test the website by entering various planetary data and ensuring the model predicts correctly.
Debug any issues with prediction accuracy or web functionality.
Technologies Used
Frontend: HTML5, CSS3, Bootstrap
Backend: Python, Flask
Machine Learning: Scikit-learn, Pandas, Numpy
Database: (Optional) SQLite for storing user input history or logs
How to Use
Run the web application and open the website.
Input exoplanet data such as mass, temperature, and gravity in the form.
Submit the data and view the habitability prediction (habitable or non-habitable).
(Optional) Check the confidence score or compare different planets.
Future Improvements
Add more planetary features to improve the prediction model's accuracy.
Implement a user authentication system to save past predictions.
Visualize prediction results using charts and graphs for better user understanding.
Integrate a real-time exoplanet data API for automatic predictions.
