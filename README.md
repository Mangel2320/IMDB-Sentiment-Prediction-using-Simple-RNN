# IMDB-Sentiment-Prediction-using-Simple-RNN 

## Overview
This project is a web application for sentiment analysis of IMDB movie reviews using a deep learning model built with TensorFlow and Keras. The app allows users to input a movie review and predicts whether the review is positive or negative.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Model](#model)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [License](#license)

## Features
- User-friendly web interface to input movie reviews.
- Real-time sentiment analysis using a pre-trained RNN model.
- Displays sentiment prediction and the corresponding confidence score.

## Installation
### Prerequisites
- Python 3.x
- TensorFlow
- Keras
- scikit-learn
- Streamlit
- ngrok

### Setting Up the Environment
1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/imdb-sentiment-analysis.git
    cd imdb-sentiment-analysis
    ```

2. Create and activate a virtual environment:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
### Running the Application
1. Ensure your model file (`simple_rnn_imdb.h5`) is in the correct path.
2. Start the Streamlit app with ngrok:
    ```bash
    streamlit run app.py
    ```
3. Open a new terminal and start ngrok:
    ```bash
    ngrok http 8501
    ```
4. Access the application via the provided ngrok URL.

## Model
The model is a simple RNN trained on the IMDB dataset. For details on training the model, refer to the `model_training.ipynb` notebook in the repository.

## Deployment
To deploy the app on a public server or cloud platform, follow these steps:

1. **Docker (Optional):** Use the provided Dockerfile to containerize the application.
    ```bash
    docker build -t imdb-sentiment-analysis .
    docker run -p 8501:8501 imdb-sentiment-analysis
    ```

2. **Heroku (Optional):** Deploy to Heroku by following their deployment guides, using the `Procfile` and `requirements.txt` provided.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.
