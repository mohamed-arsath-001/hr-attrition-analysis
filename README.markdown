# HR Employee Attrition Analysis and Prediction

## Project Overview

This project focuses on analyzing and predicting employee attrition using a dataset containing HR-related information. The goal is to identify key factors contributing to employee turnover and build a predictive model to classify whether an employee is likely to leave the organization. A Random Forest Classifier is employed to achieve high accuracy in predicting attrition, and exploratory data analysis (EDA) provides insights into the relationships between various features and attrition.

The project is implemented in Python using a Jupyter Notebook (`HR_Analysis_Classification.ipynb`) and leverages libraries such as Pandas, NumPy, Matplotlib, Seaborn, and Scikit-learn for data processing, visualization, and modeling.

## Table of Contents

- [Installation](#installation)
- [Dataset Description](#dataset-description)
- [Key Findings](#key-findings)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)

## Installation

To run this project locally, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/hr-attrition-analysis.git
   cd hr-attrition-analysis
   ```

2. **Set Up a Virtual Environment** (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Dependencies**:
   Install the required Python packages listed in `requirements.txt`:
   ```bash
   pip install -r requirements.txt
   ```

4. **Install Jupyter Notebook** (if not already installed):
   ```bash
   pip install jupyter
   ```

5. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   Open the `HR_Analysis_Classification.ipynb` file in the Jupyter interface.

## Dataset Description

The dataset is sourced from a ZIP file (`archive (1).zip`) containing two CSV files:
- **employee_survey_data.csv**: Contains employee survey responses, including:
  - `EmployeeID`: Unique identifier for each employee.
  - `EnvironmentSatisfaction`: Satisfaction with the work environment (1–4).
  - `JobSatisfaction`: Satisfaction with the job (1–4).
  - `WorkLifeBalance`: Work-life balance rating (1–4).
- **general_data.csv**: Contains general employee information, including:
  - `Age`: Employee's age.
  - `Attrition`: Whether the employee left the company (Yes/No).
  - `BusinessTravel`: Frequency of business travel.
  - `Department`: Employee's department.
  - `DistanceFromHome`: Distance from home to workplace.
  - `Education`: Education level.
  - `EducationField`: Field of education.
  - `EmployeeID`: Unique identifier (links to survey data).
  - And other features like `NumCompaniesWorked`, `TotalWorkingYears`, etc.

The dataset is preprocessed to handle missing values by imputing median values for columns such as `NumCompaniesWorked`, `TotalWorkingYears`, `EnvironmentSatisfaction`, `JobSatisfaction`, and `WorkLifeBalance`.

## Key Findings

- **Missing Values**: Handled by imputing median values for relevant columns.
- **Class Imbalance**: The `Attrition` variable shows a significant imbalance, with fewer employees having attrited compared to those who stayed.
- **Feature Insights**:
  - Lower levels of job satisfaction, environment satisfaction, and work-life balance are correlated with higher attrition rates.
  - Attrition varies across departments, education fields, and job roles.
- **Model Performance**: A Random Forest Classifier achieved:
  - **Accuracy**: 0.9955
  - **Precision**: 1.0000
  - **Recall**: 0.9718
  - **F1-Score**: 0.9857
- **Feature Importance**: Key features influencing attrition predictions were identified through feature importance analysis.

## Usage

1. **Prepare the Dataset**:
   - Ensure the `archive (1).zip` file is placed in the project directory.
   - The notebook automatically extracts and loads the CSV files into Pandas DataFrames.

2. **Run the Notebook**:
   - Open `HR_Analysis_Classification.ipynb` in Jupyter Notebook.
   - Execute the cells sequentially to perform data loading, preprocessing, EDA, and model training.

3. **Explore the Analysis**:
   - Review visualizations (e.g., plots created with Matplotlib and Seaborn) to understand feature relationships.
   - Check the model evaluation metrics and feature importance outputs.

4. **Modify and Extend**:
   - Adjust preprocessing steps or model parameters in the notebook to experiment with different approaches.
   - Add new visualizations or models as needed.

## Project Structure

```
hr-attrition-analysis/
├── HR_Analysis_Classification.ipynb  # Main Jupyter Notebook with analysis and modeling
├── archive (1).zip                   # Dataset ZIP file (not included in repo, user must provide)
├── requirements.txt                  # Python dependencies
├── .gitignore                        # Git ignore file
└── README.md                         # Project documentation
```

## Results

The Random Forest Classifier demonstrates excellent performance in predicting employee attrition, with near-perfect precision and high recall. The EDA reveals actionable insights, such as the importance of job satisfaction and work-life balance in reducing turnover. Feature importance analysis highlights the most influential factors, which can guide HR strategies to improve employee retention.

## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

Please ensure your code follows PEP 8 guidelines and includes appropriate documentation.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.