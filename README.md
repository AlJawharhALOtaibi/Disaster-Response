# Disaster Response with AI: Message Classification for Effective Relief
![1*WbxjI5poZm3OjVuw9WNFqQ](https://github.com/AlJawharhALOtaibi/Disaster-Response/assets/87391133/e4c2e6f7-a4ae-4a01-8a52-a6ed6005677a)

## Project Overview

This project focuses on the development of a real-time message classification system using machine learning to enhance the efficiency of disaster relief efforts. The primary objectives include accurately categorizing disaster messages, enabling targeted outreach to relevant relief agencies, and creating a user-friendly web app for emergency workers. The adaptable framework of this project holds the potential for broader applications, such as identifying urgent needs and tracking resource distribution.

## Key Components

### 1. Data Analysis

Explore real-world disaster message datasets to uncover patterns and key features crucial for effective message classification.

### 2. Machine Learning Pipeline

Construct a multi-stage pipeline for data handling, feature engineering, and model training, utilizing advanced Natural Language Processing (NLP) techniques.

### 3. Model Development

Train a highly accurate model capable of classifying disaster messages into distinct categories, with a primary focus on precision and recall.

### 4. API Creation

Develop a versatile API for real-time classification of new messages, facilitating seamless integration into web and mobile applications.

### 5. User-Friendly Web App

Design an intuitive web app for emergency workers, empowering them to input messages swiftly and receive immediate and clear classification results.

## Project Structure

### ETL Pipeline:

- Perform data cleaning and preparation within `process_data.py`.
- Merge messages and categories datasets.
- Store clean data in the SQLite database (`DisasterResponse.db`).

### ML Pipeline:

- Load data from the SQLite database within `train_classifier.py`.
- Split data into training and testing sets.
- Build a robust text processing and machine learning pipeline.
- Train and fine-tune the model using `GridSearchCV`.
- Output results on the test set.
- Export the final model as a pickle file (`classifier.pkl`).

### Flask Web App:

- Allow users to input disaster-related messages.
- Display real-time classification results for targeted relief efforts.

## Running the Project

### Data Cleaning:

```bash
python3 process_data.py disaster_messages.csv disaster_categories.csv DisasterResponse.db
```

### Training Classifier:

```bash
python3 train_classifier.py DisasterResponse.db classifier.pkl
```

### Starting Web App:

```bash
python3 run.py
```

## Conclusion

This Disaster Response with AI project provides a robust framework for real-time message classification, enabling emergency workers to streamline their efforts efficiently. By combining advanced machine learning techniques with user-friendly interfaces, the project aims to contribute significantly to enhancing disaster response capabilities. For further details, refer to the documentation and feel free to reach out to the project team for additional information or assistance.
