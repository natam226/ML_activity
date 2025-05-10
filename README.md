# ML_activity

## 🧹 Feature Selection

Following an exploratory data analysis (EDA), the following features were selected:

### 📊 Categorical Variables
- `listing_type_id`
- `buying_mode`
- `status`
- `shipping_mode`

> These were transformed using `OneHotEncoder`.

### ✅ Boolean Variables
- `automatic_relist`
- `local_pick_up`
- `free_shipping`

> These were converted to binary values (`0` or `1`).

### 🔢 Numerical Variables
- `price`
- `sold_quantity`
- `available_quantity`

> These were standardized using `StandardScaler`.

### 🎯 Target Variable
- `condition` → Binary classification: `new` (1) or `used` (0)

---

## ⚙️ Trained Models

The following classifiers were trained and evaluated:

- **Logistic Regression**
- **K-Nearest Neighbors (KNN)**
- **Decision Tree**
- **XGBoost Classifier**

---

## 📊 Evaluation Metrics

Models were compared using the following metrics:

- **Accuracy**
- **Precision**
- **Recall**
- **F1 Score**

---

## 🏆 Best Model Selection

After training and evaluating all models using cross-validation and final test set evaluation, the **XGBoost Classifier** was selected as the best-performing model.

XGBoost consistently outperformed other models across key metrics, including precision, recall, F1 score, and overall accuracy. Its ability to model complex relationships, handle both numerical and categorical features effectively, and manage class imbalance made it particularly well-suited to this classification task.

The selection was based on the model’s performance on the **test set**, ensuring that the model generalizes well to unseen data.

- **Class `0`** (`used`) was predicted with good precision (0.8111) and recall (0.8356).
- **Class `1`** (`new`) was also predicted very accurately, with a precision of 0.8538 and recall of 0.8315.
- The overall **accuracy of 83.34%** indicates that the model generalizes well to new data.
- The **macro and weighted averages** confirm that performance was consistent across both classes.