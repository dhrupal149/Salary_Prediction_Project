# Salary Prediction Project

This is a simple **salary prediction** project using Python, Flask, and Streamlit. The project uses a Linear Regression model to predict salary based on years of experience.

---

## Project Structure
Salary_prediction_project/
│
├── train_model.py # Script to train the Linear Regression model and save it as model.pkl
├── model.pkl # Trained model (created after running train_model.py)
├── app.py # Flask API to serve predictions
├── app_ui.py # Streamlit app for user-friendly interface
├── README.md # Project documentation


---

## Requirements

- Python 3.8+
- Libraries:

```bash
pip install pandas scikit-learn flask streamlit

Step 1: Train the Model

Run the train_model.py script to create the model.pkl file:
python train_model.py

This will train a Linear Regression model using sample experience and salary data and save it for later use.

Step 2: Run the Flask API

Start the API by running:

python app.py
API will be available at http://127.0.0.1:5000/
Endpoints:
GET / → Check if API is running
POST /predict → Predict salary

JSON payload example:

{
  "Experience": 5
}

Response:

{
  "salary": 100000
}
Step 3: Run the Streamlit App
Launch the Streamlit interface:

python -m streamlit run app_ui.py
Enter years of experience
Click Predict to see the predicted salary

Notes
The sample data is small and used for demonstration purposes. Replace it with a larger dataset for better accuracy.
Make sure model.pkl exists before running the API or Streamlit app.
If streamlit command is not recognized, run via Python:
python -m streamlit run app_ui.py
