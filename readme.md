🧠 Image Classification Web App (TensorFlow + Flask + Heroku)

A deep learning web application that classifies uploaded images into one of 10 categories using a Convolutional Neural Network (CNN) built with TensorFlow/Keras.
The model is deployed as a Flask web app and hosted on Heroku for real-time image prediction.

🚀 Live Demo

👉 https://your-app-name.herokuapp.com

📸 Features

🧩 Custom CNN architecture built from scratch using TensorFlow/Keras

🧠 92% test accuracy on a 10-class image dataset (e.g., CIFAR-10)

🔄 Data augmentation, dropout, and batch normalization for robustness

🌐 Flask web interface for uploading and classifying images

☁️ Deployed on Heroku for public access

🧾 Real-time predictions displayed in browser

🧠 Model Overview

The CNN model consists of:

Multiple Conv2D + MaxPooling2D layers for feature extraction

BatchNormalization for stable training

Dropout layers to reduce overfitting

Fully connected dense layers with softmax output for multi-class prediction

Example architecture:

model = Sequential([
    Conv2D(32, (3,3), activation='relu', input_shape=(32,32,3)),
    BatchNormalization(),
    MaxPooling2D(2,2),
    Dropout(0.25),
    
    Conv2D(64, (3,3), activation='relu'),
    BatchNormalization(),
    MaxPooling2D(2,2),
    Dropout(0.25),
    
    Flatten(),
    Dense(128, activation='relu'),
    Dropout(0.5),
    Dense(10, activation='softmax')
])

🧰 Technologies Used
Component	Technology
Deep Learning	TensorFlow, Keras
Web Framework	Flask
Frontend	HTML5, CSS3, Bootstrap
Deployment	Heroku
Tools	NumPy, OpenCV, Pillow
📂 Project Structure
📦 image-classification-flask
│
├── app.py                  # Flask web application
├── model.py                # CNN model training script
├── model.h5                # Trained model file
├── static/                 # CSS, JS, and image assets
├── templates/              # HTML templates (Flask frontend)
├── requirements.txt        # Dependencies
├── Procfile                # Heroku deployment file
└── README.md               # Project documentation

⚙️ Installation & Setup
1️⃣ Clone the repository
git clone https://github.com/<your-username>/image-classification-flask.git
cd image-classification-flask

2️⃣ Install dependencies
pip install -r requirements.txt

3️⃣ Run locally
python app.py


Now visit: http://127.0.0.1:5000

4️⃣ Deploy to Heroku
heroku create your-app-name
git add .
git commit -m "Initial deployment"
git push heroku main

🧪 Example Results
Input Image	Predicted Label
🐶 Dog	Dog
✈️ Airplane	Airplane
🚗 Car	Automobile
📈 Results
Metric	Value
Test Accuracy	92%
Loss	0.23
Epochs	25
Optimizer	Adam
📚 Future Improvements

🔍 Add Grad-CAM visualizations

📊 Add interactive charts for training metrics

🌈 Support custom user datasets

🚀 Deploy using Docker for scalability


🪪 License

This project is licensed under the MIT License
.
