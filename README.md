Run this python code to get the data from kaggle
================================================
import os

def setup_data():
    if not os.path.exists('train.csv'):
        print("Data not found. Downloading from Kaggle...")
        # Note: Requires kaggle.json API token configured
        os.system("kaggle competitions download -c playground-series-s6e2")
        os.system("unzip playground-series-s6e2.zip")
    else:
        print("Dataset already present and ready for analysis.")

setup_data()
