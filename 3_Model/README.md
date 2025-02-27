# Model Definition and Evaluation

## Neural Network Model: Definition and Evaluation

### Implementation Overview
The Jupyter Notebook **neuronales_netz.ipynb** implements a multi-layer neural network using modern optimization methods to improve predictive accuracy.

### Model Selection
The selection of models was based on problem complexity:
- A **baseline model** was chosen for its simplicity and interpretability. It served as a starting point to assess the predictive performance of more complex models.
- The **neural network** was selected due to its ability to capture complex, nonlinear relationships in the data and improve prediction accuracy.

### Feature Engineering and Function Development
- The models utilize specially developed functions that extract the most relevant features from the preprocessed data.
- The neural network incorporates various activation functions (e.g., ReLU) and optimization algorithms (e.g., Adam).
- Additional feature engineering was performed to enhance feature diversity and improve model performance.

### Hyperparameter Tuning
- Optimization of hyperparameters included tuning the number of layers, the number of neurons per layer, the learning rate, and batch size.
- Techniques such as **Grid Search** and **Random Search** were used to identify the best hyperparameter combinations.
- The models were validated using **cross-validation** to prevent overfitting and improve generalizability.

### Model Training and Execution
- The models were trained using the preprocessed training dataset and then evaluated on a separate test dataset.
- Multiple training cycles were conducted to ensure model convergence.
- Key metrics were documented during each iteration to track model performance.

### Evaluation Metrics
To assess model performance, the following evaluation metrics were used:
- **Mean Squared Error (MSE):** Measures the average squared deviations between predictions and actual values.
- **R²-Score:** Indicates how well the model explains the variance in the target variable. A value close to 1 suggests high explanatory power.
- **Mean Absolute Error (MAE):** Evaluates the average absolute deviation of predictions from actual values.

## Summary
The neural network demonstrated superior predictive accuracy compared to the baseline model. By optimizing hyperparameters and using feature engineering, the model successfully captured complex patterns within the data. This documentation provides a structured approach for implementing and evaluating neural networks in real-world applications.

