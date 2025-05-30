# MLOP
Respository for MLOps course

# Iris Decision Tree Classifier

This project builds and evaluates a Decision Tree classifier to classify Iris flower species using the classic Iris dataset. The trained model is saved for future use.

## Project Structure
.
├── data/
│   └── iris.csv           # Input dataset
├── models/
│   └── decision\_tree\_model.pkl  # Trained Decision Tree model (output)
├── train.py               # Main script to train and save the model
└── README.md              # Project documentation


## Model Description

- **Algorithm**: Decision Tree Classifier (scikit-learn)
- **Max Depth**: 3
- **Features**: `sepal_length`, `sepal_width`, `petal_length`, `petal_width`
- **Target**: `species`

## Getting Started

### Prerequisites

Make sure you have the following installed:

- Python 3.7+
- pip

### Installation

1. Clone the repository or download the files.
2. Install required dependencies:

```bash
pip install pandas numpy scikit-learn joblib
````

3. Ensure the `iris.csv` file is placed inside a `data/` directory.

### Running the Training Script

```bash
python train.py
```

* Trains a Decision Tree Classifier.
* Prints the model accuracy.
* Saves the trained model to `models/decision_tree_model.pkl`.

## Output

* Console prints the accuracy of the classifier on the test set.
* A serialized model file (`.pkl`) is saved under the `models/` directory.

## Testing

To validate the output, you can load the model and run predictions in a separate script or notebook.

python
import pickle
model = pickle.load(open("models/decision_tree_model.pkl", "rb"))
# model.predict(...) on new data
