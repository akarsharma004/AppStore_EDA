# Apple App Store Analysis

## Project overview:
This project aims to empower the Apple App Store with data-driven insights to enhance user decision-making. By analyzing user engagement, reviews, and the factors influencing these metrics, we can identify areas for improvement and implement new features that cater to user needs.

## Data Sources and Tool use:

* **Apple App Store** dataset which contains information like app name, primary genre, content rating, average user rating, total number of reviews, etc.
* The analysis is primarily done in Python, with Pandas used for basic inspection, univariate and bivariate analysis of all numerical and categorical features. Matplotlib and Seaborn then visualize the findings.

## Data Cleaning/Preparation:

In the initial phase after the basic inspetion, follwing cleaning and preparation is done:

- There are 1,230,376 rows and 21 columns in the raw dataset.
- Some features have incorrect datatype, so we will convert them to the desired datatype.
- Columns such as App_Id, AppStore_Url, Developer_Url, and Developer_Website do not provide relevant information for our analysis, so we will remove them.
- **Missing Values:**
 Missing values have been identified in the Size_Bytes, Released, and Price columns.
  - We'll employ the mode to impute missing values in the Price column, the median for the Size_Bytes column, and remove rows with missing values in the Released column.
  - For rows with missing Price values that have been imputed using the mode (0), we'll update the corresponding values in the Free column to "yes" to accurately reflect their free status.

## Exploratary Data Analysis:

- An initial data exploration revealed potential redundancy (duplicate columns), right-skewed features with outliers, a growing trend in user ratings, and iOS version requirements primarily focused on iOS 9 and above.
- Beyond the obvious dominance of Games and Business genres, free apps with 4+ content ratings remain the norm, as the app ecosystem witnesses a growing chorus of releases and updates each year. Interestingly, this growth echoes within months and quarters, with app updates mysteriously clustering in the later half, particularly Q3 and Q4.
- While numerical feature correlations require further exploration, app size reveals interesting connections with ratings, content rating, and genre, with larger sizes corresponding to higher ratings for some genres and content levels.
- App release trends favor free apps with high content ratings, with popular genres like Games, Business, and Education fueling the surge, yet Developer Tools offer a unique landscape where paid options hold their own against the free majority.

## Results/Findings:
- App Store is dominated by free apps with 4+ content ratings, primarily spanning Games, Business, and Education genres.
- Apps with higher average ratings tend to be larger in size (up to 400MB) and belong to genres like Weather, Games, and Photos & Videos.
- Developer Tools apps generally have lower ratings and smaller sizes.
- App releases and updates have been increasing over time, particularly in the second half of the year.
Most apps require iOS versions 9 and beyond.

## Suggestion:
Focus on high-rating genres (Games, Weather, Photos & Videos) and potentially explore 9+ content ratings. Balance app size for user experience and consider paid models for unique value propositions. Time releases and updates strategically, prioritizing compatibility with latest iOS versions. Experiment with higher content ratings and prioritize continuous updates to drive engagement and success.
