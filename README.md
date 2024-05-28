# Statistical-Modelling

**Data Loading and Initial Exploration**

The process begins by loading the music dataset using the pandas library. The initial few rows of the dataset are displayed to get a sense of its structure. Column information, including data types and non-null counts, is examined to understand the composition of the data. Summary statistics are also reviewed to get insights into the distribution and central tendencies of the numerical features.

**Data Cleaning**

An unnamed column, likely an index, is identified and removed from the dataset. Missing values in the Track Name, Artists, and Album Name columns are filled with a placeholder text "Unknown" to ensure completeness of the data.

**Distribution Analysis**

The distribution of the Popularity score is visualized using a histogram with a kernel density estimate (KDE). This helps to understand how the popularity scores are spread across the tracks. Most tracks in the dataset show moderate to high popularity scores, with peaks around the 50s and 60s.

**Correlation Analysis**

A correlation matrix is generated to explore the relationships between numerical features. A heatmap visualization provides a clear view of how different features are correlated with each other and with the Popularity score. Notably, Loudness and Energy show positive correlations with Popularity, while Acousticness shows a slight negative correlation.

**Feature Impact Visualization**

Scatter plots are created to visualize the relationships between several key features (Danceability, Energy, Loudness, Acousticness, Valence) and the Popularity score. These plots help to identify trends and patterns in how these features influence track popularity. For example, higher Danceability, Energy, and Loudness generally correlate with higher popularity, while higher Acousticness tends to correlate with lower popularity.

**Explicit Content Analysis**

The dataset is further segmented by explicit content to see if the relationships between features and popularity differ for explicit and non-explicit tracks. Scatter plots show that explicit tracks tend to cluster higher on the popularity scale at similar levels of danceability and energy compared to non-explicit tracks.

**Statistical Modelling**

A linear regression model is built to quantitatively assess the impact of various features on the popularity of music tracks. The Explicit column is converted from boolean to integer format for inclusion in the model. Features are standardized, and the dataset is split into training and testing sets. The linear regression model is then trained on the training set and evaluated on the test set.

**Model Evaluation**

The coefficients from the regression model indicate the direction and magnitude of the impact of each feature on track popularity. Positive coefficients (e.g., for Danceability, Loudness, Acousticness, Valence) suggest that increases in these features are associated with higher popularity. Negative coefficients (e.g., for Energy, Key, Mode, Tempo) suggest that increases in these features are associated with lower popularity. The coefficients for Explicit and Speechiness indicate a negligible impact on popularity.


This analysis provides a comprehensive understanding of the factors influencing the popularity of music tracks. The statistical modelling framework, combined with data visualization, helps to reveal how different musical features contribute to a track's popularity. The insights gained can be valuable for music producers, marketers, and data analysts in the music industry.
