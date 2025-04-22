# Airline Booking Behavior Prediction

## Overview

This project predicts airline customer booking behavior using machine learning techniques.  It aims to identify key factors influencing whether a customer completes a booking, providing insights that can be valuable for airlines to optimize their services and marketing. The analysis utilizes exploratory data analysis (EDA) and predictive modeling.

## Key Features

* **Data Loading and Exploration:** The project begins with loading and exploring the customer booking dataset to understand its structure and characteristics.
* **Data Preprocessing:** Data cleaning and transformation are performed, including handling categorical features (using OneHotEncoding) and scaling numerical features (using StandardScaler).
* **Feature Engineering:** Categorical features like `sales_channel`, `trip_type`, `route`, and `booking_origin` are encoded to numerical representations suitable for machine learning models.
* **Predictive Modeling:**
    * Logistic Regression and Random Forest models are trained to predict the `booking_complete` status.
    * Models are evaluated using metrics like classification report, AUC-ROC score, and confusion matrix.
* **Feature Importance:** For the Random Forest model, feature importance is calculated to identify the most influential factors in predicting booking completion.

## Technologies Used

* Python
* Pandas
* Scikit-learn (for modeling and preprocessing)
* Matplotlib, Seaborn (for visualization)

## Installation

1.  Clone the repository:

    ```bash
    git clone github.com/Afeez07/Airline_Booking_Behavior_Prediction
    ```

2.  Install the required libraries:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1.  Run the Jupyter Notebook:

    ```bash
    Jupyter Notebook Airline Booking Behavior Prediction.ipynb
    ```

    * This notebook contains the code for data loading, preprocessing, modeling, and evaluation.  Execute the cells in the notebook sequentially to reproduce the analysis.

## Data

* The notebook uses a dataset named `customer_booking.csv`.  
    * "The dataset contains customer booking information for flights, including details about the booking channel, trip type, lead time, duration of stay, flight schedule, and whether the booking was completed."
    * "The data includes both numerical features (e.g., `purchase_lead`, `flight_duration`) and categorical features (e.g., `sales_channel`, `booking_origin`)."
* **Preprocessing Notes:**
    * Categorical features were encoded using OneHotEncoding to convert them into a numerical format.
    * The `flight_day` column was mapped to numerical values (Mon: 1, Tue: 2, ..., Sun: 7).
    * Numerical features were scaled using StandardScaler to standardize their range.

## Results

* **Target Variable Distribution:** The dataset shows an imbalanced class distribution, with significantly more incomplete bookings than complete bookings.
* **Model Performance:**
    * **Logistic Regression:** Achieved an AUC-ROC score of 0.7846 on the test set. (AUC-ROC means: "This indicates the model's ability to distinguish between complete and incomplete bookings. A score closer to 1 is better.").
    * **Random Forest:** Achieved an AUC-ROC score of 0.7880 on the test set.
* **Feature Importance (Random Forest):**
    * The following are the top 10 features identified by the Random Forest model:
        1.  `purchase_lead`
        2.  `length_of_stay`
        3.  `flight_duration`
        4.  `sales_channel_Internet`
        5.  `sales_channel_...`
        6.  `trip_type_...`
        7.  `booking_origin_...`
        8.  `wants_extra_baggage`
        9.  `wants_preferred_seat`
        10. `wants_in_flight_meals`
    
## Contributing

 * "Contributions to this project are welcome.  Please feel free to submit pull requests for bug fixes, feature additions, or improvements to the analysis."

## Author

* Afeez Onabekun
