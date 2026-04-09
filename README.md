Mobile Price Classification Project
Overview
This project applies machine learning techniques to classify mobile phones into distinct price ranges based on their hardware specifications (such as RAM, battery power, and camera quality). The project includes exploratory data analysis (EDA), an ablation study, and the evaluation of multiple models including Logistic Regression, Support Vector Machines (SVM), and Random Forests.

Package Requirements
To run the Jupyter Notebook smoothly, ensure you have Python 3.8 or higher installed. The required libraries are listed below.

You can save the following list in a requirements.txt file:
pandas>=1.3.0
numpy>=1.21.0
scikit-learn>=1.0.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
Note: If you decided to keep kagglehub to download the dataset programmatically, you should add kagglehub to this list. Otherwise, ensure your downloaded train.csv and test.csv are in the project folder.

Run Instructions
Follow these steps to set up and execute the project locally:

1. Clone or Extract the Project
Ensure all project files, including the mobile_price_prediction.ipynb notebook and the dataset files (train.csv / test.csv), are located in the same directory.

2. Set Up a Virtual Environment (Recommended)
Open your terminal or command prompt, navigate to the project directory, and create a virtual environment to keep dependencies isolated:
python -m venv env

Activate the environment:

Windows: .\env\Scripts\activate

macOS/Linux: source env/bin/activate

3. Install Dependencies
Install the required packages using pip. If you created a requirements.txt file, run:
pip install -r requirements.txt

4. Launch the Jupyter Notebook
Start the Jupyter Notebook server by running:
jupyter notebook

5. Execute the Code

Your browser will open the Jupyter dashboard.
Click on mobile_price_prediction.ipynb to open it.
Navigate to the top menu and select Cell > Run All to execute the EDA, train the models, and view the final PCA and ablation study results.
