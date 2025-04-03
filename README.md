# Music Recommendation Algorithm 
>> ### created using *KMeans Clustering* - an Unsupervised Machine Learning Method
___

## Project Overview

___

Within this project, I will be examining a real dataset of songs from 1950 to 2011. 

This dataset contains a mix of lyrical and continuous variables pulled from a 2020 research paper titled [Music Dataset: Lyrics and Metadata from 1950 to 2019] (https://data.mendeley.com/datasets/3t9vbwxgr5/3). 

The project will be broken down into 5 stages, each housed in its own Jupyter notebook:

*Stage 1*
* **Initial Exploratory Data Analysis (EDA):** Implementation of univariate, bivariate, and multivariate exploratory analyses and creation of relevant visualizations/graphs that inspect possible relationships between the several predictor features.

*Stage 2*
* **Data cleaning, Pre-Processing, and Dimensionality Reduction:** Techniques utilized include, but are not limited to:
    * Removing columns with strong colinearity 
    * Dropping null values
    * Removing unnecessary columns
    * Potentially fixing incorrectly formatted data
    * Removing outliers

The new processed dataframes will be saved as new csv files.

*Stage 3*
* **Data Model Creation, Hyperparameter Search, and Model Evaluation:**
    * Implementation of a **KMeans Clustering** algorithm on the training data set.
    * Evaluation of initial training results to determine the optimal number of clusters using the classificiation method
    * Saving the cluster labels as a new column attached to a processed and cleaned dataframe, then saving the newly updated dataframe for future analysis

*Stage 4*
* **New Sample Prediction:**
    * Application of the trained machine learning algorithm on a pre-exisiting test data set in order to generate cluster labels for each new sample.

    * After the generation of these clusters, these labels will be saved as a new column in my test dataset then will be saved this subsequent dataframe for further analysis.

*Stage 5*
* **Report:**
    * Detail insights found during the exploratory data analysus (EDA)
    * Explanation of why certain features were dropped or kept during the data wrangling phase and whether these actions informed by the EDA.
    * List the optimal number of clusters in my cluster model and an explanation of how I determined this value
    * Description of clusters in *human terms* using the columns from the dataset as reference
    * Provide song recommendations to the user based based on the clusters my algorithm assigned to my test samples

___

## Tools and Libraries
___
* Python
* NumPy for mathmatical & statistical operations
* Pandas for data manipulation
* Matplotlib & Seaborn for data visualization
* Scikit-learn for machine learning and data processing
* Statsmodels for statistical data exploration

___

## Numeric Variables
___ 
* **age:** A score from 0 to 1 expressing how “old” a song is from our perspective. 1 being the oldest, and 0 being the newest.

* **communication:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with communication (either in romantic terms or otherwise).

* **dating:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with dating.

* **family/gospel:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with family-oriented content or the gospel.

* **family/spiritual:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the importance of family or spirituality.

* **feelings:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with emotions, either positive or negative.

* **light/visual perceptions:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the sun or other physical weather-related patterns.

* **movement/places:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with movement or various locations.

* **music:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with music (music about music, basically).

* **night/time:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do night-life or time.

* **obscene:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with obscene content (money, rockstar-lifestyle, etc).

* **romantic:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with romantic feeling.

* **sadness:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the importance of family or spirituality.

* **shake the audience:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with provocative feeling.

* **violence:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with violence.

* **world/life:** A score from 0 to 1 expressing how likely it is that this song’s lyrics have something to do with the world or life in general terms.

___

## Categorical Variables

___
* **artist_name:** The name of the artist

* **genre:** The categorical genre of this song

* **len:**  The number of words in the lyrics of this song

* **lyrics:** The pre-tokenized lyrics of this song. *Disclaimer: note that as this is real-world data, lyrical content is often obscene.* 

* **release_date:** When this song was released

* **topic:** The categorical label of lyrical content

* **track_name:** The name of the song

