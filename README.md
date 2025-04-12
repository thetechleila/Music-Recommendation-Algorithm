# Music Recommendation Algorithm 
___

## Project Overview
___

This project contains the process of creating a song recommendation algorithm trained on the [Music Dataset: Lyrics and Metadata from 1950 to 2019](https://data.mendeley.com/datasets/3t9vbwxgr5/3) (created in 2020) using an unsupervised machine learning method called [KMeans Clustering](https://www.ibm.com/think/topics/k-means-clustering). 

The overall goal is to successfully develop a machine learning pipeline that clusters songs based on features like genre, release date, artist and more in order to provide personalized recommendations.

The project will be broken down into 5 stages, each housed in its own Jupyter notebook:

#### *Stage 1*
* **Initial Exploratory Data Analysis (EDA):** Implementation of univariate, bivariate, and multivariate exploratory analyses and creation of relevant visualizations/graphs that inspect possible relationships between the several predictor features.

####  *Stage 2*
* **Data Cleaning, Data Wrangling/Pre-Processing, and Dimensionality Reduction:** Techniques utilized include, but are not limited to:
    * Removing columns with strong colinearity 
    * Dropping null values
    * Removing unnecessary columns
    * Potentially fixing incorrectly formatted data
    * Removing outliers

The new processed dataframes will be saved as new csv files.

#### *Stage 3*
* **Data Model Creation, Hyperparameter Search, and Model Evaluation:**
    * Implementation of a **KMeans Clustering** algorithm on the training data set.
    * Evaluation of initial training results to determine the optimal number of clusters using the classificiation method
    * Saving the cluster labels as a new column attached to a processed and cleaned dataframe, then saving the newly updated dataframe for future analysis

#### *Stage 4*
* **New Sample Prediction:**
    * Application of the trained machine learning algorithm on a pre-exisiting test data set in order to generate cluster labels for each new sample.

    * After the generation of these clusters, these labels will be saved as a new column in my test dataset then will be saved this subsequent dataframe for further analysis.

    * **Please Note that Stages 3 & 4 are both stored in the model_and_sampleprediction.ipynb Jupyter Notebook in the code folder.**

#### *Stage 5*
* **Report:**
    * Detailed insights found during the exploratory data analysus (EDA)
    * Explanation of why certain features were dropped or kept during the data wrangling phase and whether these actions informed by the EDA.
    * Listing of the optimal number of clusters in the cluster model and an explanation of how this value was determined
    * Description of clusters in *human terms* using the columns from the dataset as reference
    * Sample song recommendations for a test user based on the clusters the algorithm assigned to the test samples

___

## Data Overview

___
### *Numeric Features*

* **age:** A score from 0 to 1 expressing how “old” a song is from our perspective. 1 being the oldest, and 0 being the newest.

* **communication:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with communication (either in romantic terms or otherwise).

* **dating:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with dating.

* **family/gospel:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with family-oriented content or the gospel.

* **family/spiritual:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the importance of family or spirituality.

* **feelings:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with emotions, either positive or negative.

* **len:**  The number of words in the lyrics of this song

* **light/visual perceptions:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the sun or other physical weather-related patterns.

* **movement/places:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with movement or various locations.

* **music:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with music (music about music, basically).

* **night/time:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do night-life or time.

* **obscene:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with obscene content (money, rockstar-lifestyle, etc).

* **release_date:** When this song was released

* **romantic:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with romantic feeling.

* **sadness:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the importance of family or spirituality.

* **shake the audience:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with provocative feeling.

* **violence:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with violence.

* **world/life:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the world or life in general terms.

>>

### *Categorical Features*

* **artist_name:** The name of the artist

* **genre:** The categorical genre of this song

* **lyrics:** The pre-tokenized lyrics of this song. *Disclaimer: note that as this is real-world data, lyrical content is often obscene.* 

* **topic:** The categorical label of lyrical content

* **track_name:** The name of the song

___

## Tools 
___
* Python
* NumPy for mathmatical & statistical operations
* Pandas for data manipulation
* Matplotlib & Seaborn for data visualization
* Scikit-learn for machine learning and data processing
* Statsmodels for statistical data exploration
* Jupyter Notebooks