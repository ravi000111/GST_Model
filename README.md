# GST Model Prediction using Machine Learning

## Project Description
This project involves building a machine learning model to predict GST outcomes using a combination of Random Forest and XGBoost classifiers...


The purpose of this project is to assist businesses and organizations in automating their GST-related predictions based on key features from historical data.

Directory Structure
/GST_Model
|-- /data
|   |-- finalexported.csv              # Training dataset
|   |-- finalexport_test.csv           # Test dataset
|   |-- Y_Train_Data_Target.csv        # Training target dataset
|   |-- Y_Test_Data_Target.csv         # Test target dataset
|-- /notebooks
|   |-- EDA.ipynb                      # Jupyter notebook for Exploratory Data Analysis
|   |-- ModelTraining.ipynb            # Jupyter notebook for model training
|-- /scripts
|   |-- train_model.py                 # Script to train the model
|   |-- deploy_streamlit.py            # Script to run the Streamlit app
|-- README.md                          # Project readme file
|-- requirements.txt                   # Python dependencies file
|-- model.joblib                       # Saved model file

Prerequisites
Python 3.8 or higher
Jupyter Notebook
Git
Basic knowledge of machine learning and Streamlit

Installation and Setup
Clone the repository:
git clone [https://github.com/your-username/GST_Model.git](https://github.com/ravi000111/GST_Model.git)
cd GSTModel

Create a virtual environment:
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate

Install the dependencies:
pip install -r requirements.txt

Usage
Run the exploratory data analysis: Open and run the Jupyter notebook located at /notebooks/EDA.ipynb to visualize and understand the data distribution, handle missing values, and analyze feature importance.

Train the model: Run the notebook /notebooks/ModelTraining.ipynb to train the machine learning models (Random Forest and XGBoost). You can also use the script /scripts/train_model.py for a script-based approach.

Deploy the model using Streamlit:
streamlit run /scripts/deploy_streamlit.py

This will start a local web server where you can interact with the model by inputting relevant features to get GST predictions.

Model Description
Key Steps:
Data Cleaning and Preprocessing: Handled NaN values using the KNN method and removed unnecessary columns like 'ID.'
Feature Scaling: Applied Standard Scaling to normalize features.
Model Selection: Tried both Random Forest and XGBoost classifiers to find the optimal model.
Hyperparameter Tuning: Used GridSearchCV to optimize model parameters.
Threshold Selection: Tested different thresholds and settled on the best-performing value of 0.50.
Performance Metrics:
Accuracy: 97.7854%
Precision for Class 0: 0.9895
Recall for Class 0: 0.9860
Precision for Class 1: 0.8700
Recall for Class 1: 0.8995
Confusion Matrix:
[[233718,  3316]
 [  2480, 22198]]

 Evaluation
The model was evaluated using various metrics, including accuracy, precision, recall, F1 score, and AUC-ROC. For more details, please refer to the /notebooks/ModelTraining.ipynb notebook.

Deployment
The project is deployed using a Streamlit app, which provides an intuitive web-based interface for making predictions based on the model. The app loads the trained model using Joblib and offers input fields for relevant features to obtain the GST predictions.

Results and Insights
The GST model shows high accuracy and good recall for both classes, making it reliable for predicting outcomes based on historical data.

How to Contribute
If you'd like to contribute to this project, please follow these steps:

Fork the repository
Create a new branch (git checkout -b feature/your-feature-name)
Commit your changes (git commit -am 'Add your feature description')
Push to the branch (git push origin feature/your-feature-name)
Create a Pull Request

## Contact
For any questions, suggestions, or collaboration opportunities, feel free to reach out to me:

- **LinkedIn**: [Ravi Singh](https://www.linkedin.com/in/ravi-singh-316028253/)
- **Email**: [ravis4312e@gmail.com](mailto:ravis4312e@gmail.com)


Feel free to customize the README.md to fit your project's specifics. This template covers all essential sections and offers a clear structure to guide users through your project.
