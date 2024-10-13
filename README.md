# Laravel-LSTM Project

This project integrates Laravel with an LSTM (Long Short-Term Memory) model. Laravel is used for managing web-based APIs, while the LSTM model is utilized for time series forecasting or natural language processing (NLP) on a specific dataset.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Technologies Used](#technologies-used)
- [Contributors](#contributors)
- [License](#license)

## Features
- Create RESTful API with Laravel.
- Time series forecasting or text analysis using an LSTM model.
- Upload training data for the model and retrieve predictions via API.
- Interface to control the training process of the LSTM model.

## Installation

### Requirements
- PHP >= 8.0
- Composer
- Python 3.x
- Laravel 9.x
- TensorFlow or PyTorch (Python Libraries)
- Virtual Environment (virtualenv) [Optional]

### Step 1: Laravel Project Setup
1. Clone the repository:
    ```bash
    git clone https://github.com/username/laravel-lstm-project.git
    cd laravel-lstm-project
    ```

2. Install Laravel dependencies:
    ```bash
    composer install
    ```

3. Set up the `.env` file:
    ```bash
    cp .env.example .env
    php artisan key:generate
    ```

4. Configure the database connection in the `.env` file and run migrations:
    ```bash
    php artisan migrate
    ```

### Step 2: LSTM Model Setup
1. Create and activate a virtual environment (optional):
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

2. Install Python dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Step 3: Start the Project
1. Run the Laravel development server:
    ```bash
    php artisan serve
    ```

2. Start the Python script for the LSTM model:
    ```bash
    python lstm_model.py
    ```

## Usage
1. Upload training data for the model via the API and retrieve prediction results.
2. Once the model training is complete, results are stored in the database.
3. Access LSTM model predictions through the API in JSON format.

### Example API Usage
- Upload Training Data:
    ```bash
    POST /api/train
    {
        "data": [dataset]
    }
    ```

- Get Prediction Results:
    ```bash
    GET /api/predict
    ```

## Technologies Used
- **Laravel**: Backend development and API creation.
- **Python**: Training and prediction using the LSTM model.
- **TensorFlow/PyTorch**: Development and utilization of the LSTM model.
- **MySQL/PostgreSQL**: Database management.

## Contributors
- [Mustafa Cihan İncir](https://github.com/Cihan9946)

## License
This project is licensed under the MIT License. See the `LICENSE` file for more details.
