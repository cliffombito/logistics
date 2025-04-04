How to run the program 

1. Install vs code and python 3.13
2. copy code from github or clone the repo
3. enable script execution by typing (Set-ExecutionPolicy Unrestricted -Scope CurrentUser)
4. open the folder of the project in cmd and run the following commands
       1. create a virtual environment for running the code
            a) python -m venv env (click enter)
            b) env\Scripts\activate (click enter)
            c) env\Scripts\Activate.ps1 (click enter)
5. after you arae done with no errors install dependencies by running 
  "pip install numpy pandas matplotlib seaborn scikit-learn xgboost joblib"
6. when everything is installed without errors run the program model 
 "python mainfile.py"

 this should run the mainfile as one using generated sample data fed into the program.
 It does the following  
 (
     Return Prediction
Objective: Predict whether a product will be returned.

Features:

Product details (category, price, discount)

Order context (shipping method, customer segment)

Historical data (previous orders/returns)

Model: XGBClassifier with hyperparameter tuning via grid search.

Output: Probability of return and high-risk order identification.

2. Disposition Decision
Objective: Classify returned items into optimal disposition paths:

Resell

Repair/Remanufacture

Recycle

Dispose

Features:

Product condition (score, age)

Financial metrics (repair cost, resale value)

Sustainability factors (recyclable components)

Model: RandomForestClassifier with feature importance analysis.

Output: Disposition label and probabilities for each option.

3. Processing Time Prediction
Objective: Estimate time to process returns at facilities.

Features:

Warehouse status (capacity, backlog)

Product/return attributes (condition, reason)

Model: GradientBoostingRegressor with RMSE evaluation.

Output: Predicted processing time (minutes).

4. Transportation Optimization
Objective: Predict cost/time for transportation options and recommend optimal routes.

Features:

Logistics details (distance, transport mode)

Costs (fuel, labor)

Sustainability targets (carbon footprint)

Models:

Cost: GradientBoostingRegressor

Time: RandomForestRegressor

Output: Predicted costs, times, and weighted scores for route optimization.

5. Warehouse Allocation
Objective: Assign returns to warehouses based on capacity and processing efficiency.

Logic: Prioritizes items with longer predicted processing times for warehouses with higher capacity.

Output: Allocation plan balancing workload across facilities.

6. End-to-End Workflow Optimization
Integration: Combines all models into a unified pipeline:

Predict returns.

Decide disposition for returned items.

Estimate processing times.

Optimize warehouse allocation.

Plan cost/time-efficient transportation.

Sustainability Metrics: Tracks carbon footprint, waste reduction, and resource recovery.

Additional Features
Data Preprocessing: Custom pipelines for each task, handling categorical/numerical features.

Model Evaluation: Generates classification reports, confusion matrices, and regression plots.

Model Persistence: Saves/loads trained models using joblib.

Customizable Weighting: Balances cost vs. time/sustainability in transportation decisions.
 )
