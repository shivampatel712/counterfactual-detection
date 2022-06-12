# counterfactual-prediction

Our take on the counterfactual recognition task provided by SemEval 2020 Task 5.

## Subtask 1

The code for our approach for Subtask 1 is organized as:

- **notebooks/1_data_exploration_sp_v1.ipynb** : SVM baseline for the task as well as code for data loading, class imbalance exploration, and GloVe embedding coverage for the train data.
- **notebooks/2_data_preprocessing_sp_v1.ipynb** : basic preprocessing of the data for transformers - lower casing, punctuation handling, etc.
- **notebooks/3_counterfactual_transformers_sp_v1.ipynb** - training and testing transformers on our data (using huggingface)
- **notebooks/3_counterfactual_transformers_sp_v2.ipynb** - weighted cross-entropy loss and false positive/negative visualization.
- **notebooks/4_neurosymbolic_data_and_testing_sp_v1.ipynb** - data splitting for our neurosymbolic approach as well as code for testing our ensemble. training can be done using transformer training code.

The detailed explanations of these approaches is given in our report located at **reports/report.pdf**.

## Project Organization

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io

---

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
