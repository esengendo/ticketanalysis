# Predictive Analysis of IT Helpdesk Ticket Resolution Time

## Project Overview
"This project develops a machine learning model to predict the resolution time of IT helpdesk tickets. Employing advanced NLP techniques for text summarization and sentiment analysis, we extract meaningful features from ticket descriptions to enrich our predictive modeling. By analyzing historical data along with these dynamically generated NLP features, we aim to improve resource allocation, customer satisfaction, and operational efficiency. The project represents a practical application of data science, coupled with NLP, to enhance IT helpdesk operations, driven by insights from Kaggle's comprehensive dataset."

## Data Source
The data used in this project is sourced from the IT Helpdesk Dataset available on Kaggle, which contains a rich history of IT helpdesk tickets.

## Steps Involved

### Data Preprocessing
- **Data Cleaning**: Tackle missing values, outliers, and anomalies.
- **Feature Engineering**: Create features like 'ResolutionDurationMins', 'DayOfWeekOpened', and 'TimeOfDayOpened'.
- **Categorical Encoding**: Process categorical columns for the model.

### Exploratory Data Analysis (EDA)
- Use Plotly for visual analytics.
- Conduct a correlation study between features and resolution times.

## Insights from Data Visualization

- **Ticket Volume Over Time**: There are peak periods of ticket volume indicating potential systemic issues or specific events driving support needs.
- **Resolution Duration by Help Topic**: Some help topics take longer to resolve, indicating areas where process improvement may be needed.
- **Help Topic Distribution**: A small number of help topics make up the majority of tickets, which may guide resource allocation.
- **Ticket Resolution by Day of the Week**: The start of the workweek has the highest number of resolved tickets, suggesting a need for more staff during these days.
- **Source of Tickets**: Email is the primary source of tickets, indicating a possible focus area for optimizing support channels.
- **Ticket Opening Time of Day Analysis**: Tickets are most frequently opened at specific times, which could inform staffing patterns.

## Charts

Below are links to the charts generated from the dataset:

![Ticket Volume Over Time](https://github.com/esengendo/ticketanalysis/blob/main/Images/newplot.png)
![Resolution Duration by Help Topic](https://github.com/esengendo/ticketanalysis/blob/main/Images/newplot2.png)
![Help Topic Distribution](https://github.com/esengendo/ticketanalysis/blob/main/Images/newplot3.png)
![Ticket Resolution by Day of the Week](https://github.com/esengendo/ticketanalysis/blob/main/Images/newplot4.png)
![Source of Tickets](https://github.com/esengendo/ticketanalysis/blob/main/Images/newplot5.png)
![Ticket Opening Time of Day Analysis](https://github.com/esengendo/ticketanalysis/blob/main/Images/newplot6.png)


### Feature Selection
- Select significant features based on their correlation with the target variable.

### Model Development
- Experiment with various algorithms such as Linear Regression, Random Forest, and Gradient Boosting.

### Model Evaluation
- Use metrics like RMSE, MSE, MAE, and R² to evaluate model performance.

### Hyperparameter Tuning
- Fine-tune the Gradient Boosting Regressor with GridSearchCV.

### Final Model Training and Prediction
- Train the final model with the best parameters.
- Predict and evaluate the performance on the test set.

### Deployment Strategy
- Integrate the model into the existing IT system.
- Provide an interface for the helpdesk team.

### Monitoring and Maintenance
- Keep track of model performance.
- Regularly update the model with new data.

### Documentation and Reporting
- Maintain thorough documentation of methods, code, and outcomes.
- Prepare detailed reports and presentations.

## Key Considerations
- **Data Privacy**: Comply with data protection regulations.
- **Model Explainability**: Ensure the model's decisions can be understood.
- **Real-Time Prediction**: Prioritize efficiency for real-time predictions.

## Model Insights

- **R² Score**: The model shows a strong capability in predicting resolution times, as indicated by the R² score.
- **MSE and MAE**: The high values of MSE and MAE suggest the presence of large errors in certain predictions, potentially caused by outliers or violations of the model's assumptions.

### Recommendations

- **Reviewing Outliers**: It's essential to revisit outliers within the dataset since they significantly affect the MSE. We should consider implementing strategies to handle outliers or refine our feature engineering techniques.
- **Feature Importance**: Analysis reveals that 'TimeOfDayOpened' is a critical predictor, heavily influencing resolution times. In contrast, 'KYC' seems to have a negligible effect. This finding encourages us to scrutinize the data collection and feature engineering processes, particularly around the timing of issue reporting.

### Conclusions

The performance of the model is commendable with regard to the R² score; however, we acknowledge the necessity for improvement in reducing prediction errors, as shown by MSE and MAE. Addressing the issues surrounding outliers and focusing on significant features can potentially lead to a more refined and accurate model.


## References:

- Data Source: [IT Helpdesk Dataset](https://www.kaggle.com/datasets/utsav15/it-helpdesk)
- Text Summarization & Sentiment Analysis: [Hugging Face Models](https://huggingface.co/models?filter=text2text-generation)

