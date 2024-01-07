# Disaster Response with AI: Classifying Messages for Effective Relief

## Project Highlights 

- **Real-time message categorization:** Accurately classifying disaster messages using a robust machine learning model.
- **Targeted outreach:** Enabling efficient contact with relevant relief agencies based on message content.
- **User-friendly web app:** Empowering emergency workers to swiftly input new messages and receive immediate classification results.
- **Potential for broader impact:** Adaptable framework for various disaster-related tasks, such as identifying urgent needs or tracking resource distribution.

## Key Components

1. **Data Analysis:** Deep exploration of real-world disaster message dataset to uncover patterns and key features for effective classification.
2. **Machine Learning Pipeline:** Construction of a multi-stage pipeline for data handling, feature engineering, and model training, utilizing NLP techniques.
3. **Model Development:** Training a highly accurate model capable of classifying disaster messages into distinct categories, prioritizing precision and recall.
4. **API Creation:** Development of a versatile API to facilitate real-time classification of new messages, enabling integration into web and mobile applications.
5. **User-Friendly Web App:** Design of an intuitive web app specifically for emergency workers, enabling seamless message input and clear presentation of classification results.

## Project Structure

**ETL Pipeline:**
- Data cleaning and preparation within `process_data.py`.
- Merging of messages and categories datasets.
- Storage of clean data in SQLite database (`DisasterResponse.db`).

**ML Pipeline:**
- Loading data from SQLite database within `train_classifier.py`.
- Splitting data into training and testing sets.
- Building text processing and machine learning pipeline.
- Model training and tuning using GridSearchCV.
- Outputting results on the test set.
- Exporting the final model as a pickle file (`classifier.pkl`).

**Flask Web App:**
- Enabling users to input disaster-related messages.
- Displaying real-time classification results for targeted relief efforts.

## Running the Project

1. **Data Cleaning:**
   ```bash
   python3 process_data.py disaster_messages.csv disaster_categories.csv DisasterResponse.db
   ```
2. **Training Classifier:**
   ```bash
   python3 train_classifier.py DisasterResponse.db classifier.pkl
   ```
3. **Starting Web App:**
   ```bash
   python3 run.py
   ```
