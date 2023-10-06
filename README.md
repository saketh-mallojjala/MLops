# Machine Learning Model Deployment

This project demonstrates the process of training a machine learning model, containerizing it with Docker, and setting up a continuous integration (CI) pipeline using Travis CI.

## Files

### 1. `train_model.py`

The `train_model.py` file contains the Python script responsible for training a machine learning model using the Iris dataset. Here's a brief overview of its functionality:

- Loads the Iris dataset from scikit-learn's built-in datasets.
- Splits the dataset into training and testing sets.
- Trains a Random Forest Classifier on the training data.
- Makes predictions on the test data.
- Calculates and prints the accuracy of the model.

### 2. `Dockerfile`

The `Dockerfile` is used to create a Docker image of the machine learning model. Here's what it does:

- Uses an official Python 3.9 image as the base image.
- Sets the working directory to `/app` within the container.
- Copies the project files, including `train_model.py`, into the container.
- Installs the required dependencies specified in `requirements.txt`.
- Defines the command to run when the container starts, which is `python train_model.py`.

### 3. `.travis.yml`

The `.travis.yml` file configures Travis CI, a continuous integration service, to automatically run tests whenever changes are pushed to the repository. Here's what it does:

- Specifies the programming language and version (Python 3.9).
- Sets up the environment by installing project dependencies from `requirements.txt`.
- Defines the command to run unit tests, which is `python -m unittest discover -s tests`.

### 4. `unittest.py`

The `unittest.py` file contains unit tests for the machine learning code in `train_model.py`. These tests ensure the correctness of the code by comparing expected and actual outcomes. For example, it includes a test for model accuracy.

## Getting Started

To use this project, follow these steps:

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/your-github-username/your-repo.git
# Machine Learning Model Deployment

This project demonstrates the process of training a machine learning model, containerizing it with Docker, and setting up a continuous integration (CI) pipeline using Travis CI.

## Files

### 1. `train_model.py`

The `train_model.py` file contains the Python script responsible for training a machine learning model using the Iris dataset. Here's a brief overview of its functionality:

- Loads the Iris dataset from scikit-learn's built-in datasets.
- Splits the dataset into training and testing sets.
- Trains a Random Forest Classifier on the training data.
- Makes predictions on the test data.
- Calculates and prints the accuracy of the model.

### 2. `Dockerfile`

The `Dockerfile` is used to create a Docker image of the machine learning model. Here's what it does:

- Uses an official Python 3.9 image as the base image.
- Sets the working directory to `/app` within the container.
- Copies the project files, including `train_model.py`, into the container.
- Installs the required dependencies specified in `requirements.txt`.
- Defines the command to run when the container starts, which is `python train_model.py`.

### 3. `.travis.yml`

The `.travis.yml` file configures Travis CI, a continuous integration service, to automatically run tests whenever changes are pushed to the repository. Here's what it does:

- Specifies the programming language and version (Python 3.9).
- Sets up the environment by installing project dependencies from `requirements.txt`.
- Defines the command to run unit tests, which is `python -m unittest discover -s tests`.

### 4. `unittest.py`

The `unittest.py` file contains unit tests for the machine learning code in `train_model.py`. These tests ensure the correctness of the code by comparing expected and actual outcomes. For example, it includes a test for model accuracy.

## Getting Started

To use this project, follow these steps:

1. Clone the repository to your local machine:

   ```bash
   git clone https://github.com/saketh-mallojjala/MLops.git
   cd your-repo

docker build -t ml-model .
docker run ml-model

