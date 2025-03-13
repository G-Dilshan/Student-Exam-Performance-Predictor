# Student Exam Performance Predictor

This project is a regression model development for predicting students' math scores based on various features such as gender, race/ethnicity, parental education, lunch type, test preparation course, and other academic scores. The goal of this project is to evaluate multiple regression models, including Linear Regression, Random Forest, XGBoost, and others, to determine the best model for predicting math scores with high accuracy. The model also allows for a detailed comparison of the performance of different algorithms based on various evaluation metrics, including Root Mean Squared Error (RMSE), Mean Absolute Error (MAE), and R-squared (R²).

### Who It's For
* Educators & Researchers: Analyze factors influencing student performance.
* Data Scientists & ML Enthusiasts: Learn regression modeling and feature engineering.
* Education Policy Makers: Gain insights into student achievement trends.


## Deployment

1. Clone the repository:

```bash
  git clone https://github.com/your-username/Student-Exam-Performance-Predictor.git
```
2. Install dependencies:

```bash
  pip install -r requirements.txt
```
3. Run the application:

```bash
  python app.py
```
#### By default, the application will be hosted locally at http://127.0.0.1:5000/. You can access the web app in your browser by navigating to this URL.


## API Reference

#### Home Route

```http
    GET /
```
* Description: Returns the home page with a form for user input.

#### Predict Data Route

```http
    POST /predict_data
```

| Parameter | Type     | Description                       |
| :-------- | :------- | :-------------------------------- |
| `gender`      | `string` | Gender of the student (e.g., 'male', 'female') |
| `ethnicity `      | `string` | Ethnicity of the student |
| `parental_level_of_education `      | `string` | Highest level of education achieved by the student's parents |
| `lunch `      | `string` | Type of lunch the student receives (e.g., 'standard', 'free/reduced') |
| `test_preparation_course `      | `string` | Whether the student completed a test preparation course (e.g., 'none', 'completed') |
| `reading_score `      | `integer` | Student's reading score (range: 0-100) |
| `writing_score `      | `integer` | Student's writing score (range: 0-100) |

#### Response
* Renders the home.html template with the prediction results:
  * The predicted score for the student based on the input data.


## Appendix
### Project Structure

```plaintext
Student-Exam-Performance-Predictor/
│
├── app.py                          # Main application file to run the Flask server
├── requirements.txt                # Lists the required Python packages for the project
├── setup.py                        # Script to install the package and its dependencies
├── src/                            # Source code for the project
│   ├── pipeline/                   # Contains the code related to data processing and prediction pipeline
│   │   ├── predict_pipeline.py     # Contains the logic for predicting exam scores
│   │   └── custom_data.py          # Defines how input data is processed
│   ├── __init__.py                 # Marks the directory as a Python package
│
├── templates/                      # HTML templates for the Flask application
│   ├── index.html                  # Home page template
│   └── home.html                   # Page to show prediction results
│
└── README.md                       # Project documentation file



