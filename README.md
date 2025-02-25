# Verilog-Depth-Prediction
Synthetic Verilog Depth Prediction

# 📌 Overview

This project focuses on predicting the logic depth of Verilog designs using synthetically generated Verilog files. It extracts key features from Verilog files, trains an XGBoost regression model, and evaluates its accuracy.

# 📂 Project Structure

![image](https://github.com/user-attachments/assets/814741aa-03ea-41c9-a2ea-4cdd9ac3f49c)


# ⚙️ Installation & Dependencies

Ensure you have Python 3.7+ installed, then install dependencies:

![image](https://github.com/user-attachments/assets/94796538-e263-4ded-8545-00c04532235e)


# 🔄 How to Run

# 1️⃣ Generate Synthetic Verilog Data

Run the script to generate 500 Verilog designs with varied complexity:

![image](https://github.com/user-attachments/assets/ef785b06-b8cb-497c-a571-719a3f2246c6)


# 2️⃣ Extract Circuit Features

Extract key metrics from Verilog files:

![image](https://github.com/user-attachments/assets/2697faa9-5683-4477-9299-e6abd718bb9e)


# 3️⃣ Train the Machine Learning Model

Train an XGBoost model to predict logic depth:

![image](https://github.com/user-attachments/assets/161d829e-449d-401b-a8bd-d90b8102f241)


# 4️⃣ Predict Logic Depth for New Designs

Predict depth for the full dataset and save results:

![image](https://github.com/user-attachments/assets/eea8c49a-fa8f-488f-828f-380d48d6110a)


# 📊 Features Extracted

1.Gate Count (AND, OR, XOR, NAND, NOR)

2.Number of Flip-Flops (Sequential elements)

3.Combinational Logic Conditions (If-else, case statements)

4.Number of Assignments & Registers

5.Module Count (Hierarchy Depth)

# 🎯 Model & Training Details

Model Used: XGBoost Regressor

Feature Scaling: StandardScaler for normalization

Regularization: L1 (reg_alpha=2.0), L2 (reg_lambda=2.0)

Cross-validation: 5-fold (cv=5)

# Evaluation Metrics:

1.Mean Absolute Error (MAE)

2.R² Score (Accuracy %)

3.Root Mean Squared Error (RMSE)

# 📈 Results & Performance

After training on 500 synthetic circuits, the model achieves:

1.98.0% R² Score (Accuracy)

2.MAE ~ Low Error Rate

3.Improved Generalization with regularization & cross-validation

# 🚀 Future Improvements

1.Support for Real Verilog Data

2.Integration with FPGA Toolchains

3.Automated Circuit Complexity Analysis

4.Fine-tune model hyperparameters for even better accuracy

5.Use deep learning (LSTMs, CNNs) for code-based predictions
