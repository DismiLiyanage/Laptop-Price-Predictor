🧠 Laptop Price Predictor

A Machine Learning–powered web application built using Flask that predicts laptop prices based on specifications such as RAM, weight, CPU, GPU, operating system, and brand.
The app uses a trained ML model (predictor.pickle) and provides a clean, easy-to-use web interface.

🚀 Features

✔ Predict laptop prices based on hardware specs
✔ Flask-based backend
✔ Scikit-Learn ML model
✔ One-hot encoding for categorical inputs
✔ Responsive HTML/CSS UI
✔ Ready for deployment (Heroku/Render)

📸 Web App Preview

(Add screenshots if needed)

📂 Project Structure
Laptop Price Predictor/
│
├── app.py                  # Flask backend
├── templates/
│   └── index.html          # Frontend UI
├── static/
│   └── style.css           # Styling
├── model/
│   └── predictor.pickle    # Trained ML model
├── requirements.txt        # Project dependencies
└── README.md               # Project documentation

🛠 Technologies Used
Backend / ML

Python
Flask
Scikit-Learn
NumPy
Pickle
Frontend
HTML
CSS
Deployment
Gunicorn
Heroku / Render supported

📦 Installation Guide
1. Clone the repository
git clone <your-repo-link>
cd laptop-price-predictor

2. Create a virtual environment
python -m venv env
env\Scripts\activate        # Windows
# OR
source env/bin/activate     # macOS/Linux

3. Install dependencies
pip install -r requirements.txt

4. Run the application
python app.py


Visit the app at:
http://127.0.0.1:5000/

🧠 How the Model Works

The trained ML model predicts a base price using the following:
Numerical Features:
RAM (GB)
Weight (Kg)
Touchscreen (0/1)
IPS (0/1)
Categorical Features (One-Hot Encoded):
Company
TypeName
Operating System
CPU
GPU

The final prediction is scaled:

predicted_price = model_prediction * 354
And then rounded using NumPy.

📝 Input Fields (Frontend)
Feature	Type	Example
RAM	Number	8 GB
Weight	Float	1.5 Kg
Company	Dropdown	Dell, HP, Apple
Type Name	Dropdown	Notebook, Gaming
Operating System	Dropdown	Windows, Mac
CPU	Dropdown	Intel i5, AMD
GPU	Dropdown	Nvidia, Intel
Touchscreen	Checkbox	Yes/No
IPS Panel	Checkbox	Yes/No
🌐 Deployment Guide
Heroku Deployment

Make sure you have a Procfile:

web: gunicorn app:app

Then:
heroku login
heroku create <app-name>
git push heroku master

🤝 Contributing

Contributions, issues, and feature requests are welcome!

📜 License

This project is open-source. You may add MIT or another license if desired.
