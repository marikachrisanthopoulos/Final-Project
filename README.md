# Final-Project - Deliverable 4

## Presentation

### Selected Topic
Prevalent characteristics amongst dogs that are put up for adoption.

### Characteristics of Interest
- Age
- Sex
- Breed
- Time of Year (month) found
- Coat
- Size
- Liking people

### Reasoning
I am interested in determining whether certain types of dogs are more likely to be put up for adoption than others, based on the listed characteristics. I chose this topic because I am a lover of all animals, specifically dogs, and have had the wonderful pleasure of taking care of two different adopted dogs in my life so far. I believe that learning more about the dogs that are put up for adoption can help organizations and breeders prevent animals from being put up for adoption, while informing the general population of which kinds of dogs they can bring into their homes and provide better lives.

### Source of Data
- Original Data Source: [Adoptable-Dogs on Kaggle](https://www.kaggle.com/jmolitoris/adoptable-dogs?select=ShelterDogs.csv)
- Data Source Summary (Kaggle): "The data is a compilation of information on dogs who were available for adoption on December 12, 2019 in the Hungarian Database of Homeless Pets. In total, there were 2,937 dogs in the database. It contains information on dogs' names, breed, color, age, sex, the date they were found, and some characteristics of their personalities."
- File: [ShelterDogs.csv](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Original_Dataset/ShelterDogs.csv)
- Total Columns: 19
- Total Rows: 2938 (including headers)
- Analyzable Columns:
    - age (missing: 0/2937)
    - sex (missing: 0/2937)
    - breed (missing: 0/2937)
    - date_found (missing: 0/2937)
    - coat (missing: 0/2937)
    - size (missing: 0/2937)
    - likes_people (missing: 938/2937)
- Removable Columns:
    - ID (irrelevant - missing: 0/2937)
    - name (irrelevant - missing: 0/2937)
    - color (not easily described in the dataset - groupings are not specific, too many options - missing: 0/2937)
    - adoptable_from (using date_found data for time of year instead - missing: 0/2937)
    - posted (using date_found data for time of year instead - missing: 0/2937)
    - neutered (too much unknown data - missing: 1085/2937)
    - housebroken (too much unknown data - missing: 2477/2937)
    - likes_children (too much unknown data - missing: 1718/2937)
    - get_along_males (too much unknown data - missing: 1304/2937)
    - get_along_females (too much unknown data - missing: 1254/2937)
    - get_along_cats (too much unknown data - missing: 2506/2937)
    - keep_in (irrelevant - missing: 1021/2937)

### Questions
1. Are dogs of certain ages more likely to be put up for adoption?
2. Are male or female dogs more likely to be put up for adoption?
3. Are dogs of unknown breeds more likely to be put up for adoption than dogs whose breeds are known?
4. Are dogs put up for adoption at certain times of the year (winter, spring, summer, fall) in comparison to others?
5. Are dogs of certain coats (short, medium, long, wirehaired) more likely to be put up for adoption than others?
6. Are dogs of certain sizes (small, medium, large) more likely to be put up for adoption than others?
7. Are dogs who like or don't like people more likely to be put up for adoption?
8. Are different characteristics of these dogs grouped together in any ways? Are there any patterns between the most prevalent characteristics?

### Goals
1. Discover trends in individual characteristics of adoptable dogs by analyzing the dataset.
2. Discover related trends in characteristics of adoptable dogs by analyzing the dataset and determining whether there are significant relationships between certain attributes.

### Google Slides
Formal Presentation on Google Slides can be found [here](https://docs.google.com/presentation/d/1yfcbV4N6XhM7GA3Mrze-t3AU_v3_R3KXNWspXaav2y0/edit?usp=sharing).

## Data Analysis, Exploration, and Database Overviews

### Data Exploration - Preprocessing (Deliverable 1)

**Script:** [Preprocessing_Script](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Deliverable_1_Preprocessing.ipynb)

**Procedures**:
1. Viewing and learning about the data (columns, data types, null values)
2. Dropping unnecessary columns
3. Removing null values
4. Transforming string values to numerical outputs (all columns besides values for "age")
5. Exporting processed data into a .csv file for further analysis
6. Creating sample datasets: first 200 values of unprocessed (original) and processed data

### First Analysis (Deliverable 2)

**Script:** [First_Analysis.ipynb](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Deliverable_2_Analysis.ipynb)

**Model Type:** Unsupervised Machine Learning Model using Python/Pandas/Jupyter Notebook

**Explanation/Reasoning for Model Choice:**
- There are no paired inputs and outcomes: there are no specified outcomes from this dataset - just patterns/relationships between the characteristics.
- The model uses a whole dataset as input: all of the data in the columns specified in the "Analyzabe Columns" list above (after being preprocessed as necessary) will be analyzed to determine trends/patterns, as well as relationships, amongst the characteristics.

**Procedures:**
1. Uploading processed data into jupyter notebook
2. K-Means Algorithm and Clustering Method
- Benefits: easy, runs quickly, and can scale to larger datasets.
- Limitations: difficult to determine how many clusters should be used upfront.
3. Including PCA
- Benefits: PCA was integrated because I wanted to analyze many different characteristics/metrics, as opposed to just two, which makes analysis using this type of modeling difficult. Using PCA, I could statistically combine all traits into just two main metrics, for easier analysis.
- Limitations: it can be hard to understand what the two metrics mean/symbolize during this type of analysis by just looking at the generated numbers.
4. Hierarchical Clustering Method
- Benefits: easier to pick the number of clusters to use without making assumptions using the dendogram.
- Limitations: despite the dendogram being generated, it was still slightly difficult to come to the conclusion of how many clusters to use.

**Conclusion/Results:** 

The graphs/images generated by these modeling helped group adoptable dogs with similar characteristics together - please view the following files/images for results/graphs:
- [Testing_2_Clusters](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_2_Clusters.png)
- [Testing_2_Clusters_3D](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_2_Clusters_3D.png)
- [Testing_3_Clusters](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_3_Clusters.png)
- [Testing_3_Clusters_3D](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_3_Clusters_3D.png)
- [Testing_4_Clusters](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_4_Clusters.png)
- [Testing_4_Clusters_3D](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_4_Clusters_3D.png)
- [Testing_5_Clusters](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_5_Clusters.png)
- [Testing_5_Clusters_3D](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Test_5_Clusters_3D.png)
- [Elbow_Curve](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Elbow_Curve.png)
- [Dendogram](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/Dendogram.png)
- [PCA_data.csv](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Data/PCA_data.csv)

Overall, the clustering models do not showcase the relationships between the characteristics well - even with more clustering, distinct differences between the clusters are not well defined. I believe that using more quantitative methods of analysis would produce more accurate results that are easier to understand/interpret.

**Next Steps:**

In order to obtain more concrete/quantifiable results, statistical tests in R will be run.

### Second Analysis (Deliverable 3)

**Script:** [Second_Analysis](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Deliverable_3_Analysis.Rproj)

**Statistical Analyses:**
Chi-squared test using RStudio

**Explanation/Reasoning for Model Choice:**
- Chi-squared tests are used to compare the distribution of frequencies across two groups.
- These tests outline conclusions and interpret categorical data (which is the majority of the data used in this analysis).

**Procedures:**
1. Adding column "up_for_adoption" to processed_data.csv (all dogs received a "1" to indicate that they were put up for adoption).
2. Performing chi-squared tests on all categories to compare the distribution of frequencies across categories in comparison to being put up for adoption.

**Conclusion/Results:**

- Age vs. Being put up for Adoption: X-squared = 1323.7, df = 222, p-value < 2.2e-16
- Sex vs. Being put up for Adoption: X-squared = 47.148, df = 1, p-value = 6.582e-12
- Breed vs. Being put up for Adoption: X-squared = 0.42071, df = 1, p-value = 0.5166
- Liking People vs. Being put up for Adoption: X-squared = 1967.1, df = 1, p-value < 2.2e-16
- Coat Color/Pattern vs. Being put up for Adoption: X-squared = 2104.2, df = 3, p-value < 2.2e-16
- Size vs. Being put up for Adoption: X-squared = 884.12, df = 2, p-value < 2.2e-16
- Month Found vs. Being put up for Adoption: X-squared = 32.014, df = 11, p-value = 0.0007589

These results can be viewed in the following table [here](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Data/Chi_Squared_Results.xlsx).

**Interpretation:**

The results suggest we can reject the null hypothesis for most of the characteristics, based on the p-values being less than 0.05. The hypotheses for this analysis are:

- H0 : There is no difference in frequency distribution between both groups.
- Ha : There is a difference in frequency distribution between both groups

Therefore, we can conclude that the frequency of the outcomes of these variables are related to being put up for adoption.

### Database

Programs/Hosting Sites:
- [Amazon Web Services (AWS) Database](final-project.cwiwfogyf7o4.us-east-2.rds.amazonaws.com)
- pgAdmin 4

Datasets:
- [original_sample.csv](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Data/original_sample.csv): 200 rows of unprocessed (raw, original) data
- [processed_sample.csv](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Data/processed_sample.csv): 200 rows of processed data
- [processed_data.csv](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Data/processed_data.csv): all processed data
- [pca_data.csv](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Data/PCA_data.csv): results of completing PCA on processed data

Table Images:
- [original_sample_table; Image 1](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/original_sample_table_1.png)
- [original_sample_table; Image 2](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/original_sample_table_2.png)
- [processed_sample_table](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/processed_sample_table.png)
- [processed_data_table](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/processed_data_table.png)
- [pca_data_table](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/pca_data_table.png)

Entity Relationship Diagrams (ERD's):
- [ERD](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_4/Images/ERD_Deliverable_2.png)

### Dashboard
A blueprint for the Dashboard can be found in the [Google Slides Formal Presentation](https://docs.google.com/presentation/d/1yfcbV4N6XhM7GA3Mrze-t3AU_v3_R3KXNWspXaav2y0/edit?usp=sharing).

The completed dashboard can be found [here](https://public.tableau.com/app/profile/marika.chrisanthopoulos/viz/final_project_16272619899530/).

### Technologies/Tools, Languages, Algorithms

**Technologies/Tools**
- Microsoft Excel
- pgAdmin 4
- Amazon Web Services
- Jupyter Notebook
- RStudio
- Tableau Public
- Google Slides
- QuickDBD
- Github

**Languages**
- Python/Pandas
- R
- SQL

**Algorithms**
- K-means Algorithm
- Principal Component Analysis (PCA)
- Hierarchical Clustering

## Communication/Organizational Protocols
- Different branches for individual Deliverables to keep work for each segment organized.
- Staying on top of my own work and troubleshooting using the Google when necessary.
