# Final-Project - Deliverable 2

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
- File: [ShelterDogs.csv](LINK)
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

### Data Exploration - Preprocessing

Script: [Preprocessing_Script](LINK)

Procedure:
- Viewing and learning about the data (columns, data types, null values)
- Dropping unnecessary columns
- Removing null values
- Transforming string values to numerical outputs (all columns besides values for "age")
- Exporting processed data into a .csv file for further analysis
- Creating sample datasets: first 200 values of unprocessed (original) and processed data

### Data Analysis

Script:

Model Type: Unsupervised Machine Learning Model

Explanation/Reasoning for Model Choice:
- There are no paired inputs and outcomes: there are no specified outcomes from this dataset - just patterns/relationships between the characteristics.
- The model uses a whole dataset as input: all of the data in the columns specified in the "Analyzabe Columns" list above (after being preprocessed as necessary) will be analyzed to determine trends/patterns, as well as relationships, amongst the characteristics.

Procedure:
- Preliminary feature engineering and selection:
- Splitting into training/testing sets:
- Limitations:
- Benefits:

### Database

Programs/Hosting Sites:
- Amazon Web Services (AWS) Database: final-project.cwiwfogyf7o4.us-east-2.rds.amazonaws.com
- pgAdmin 4

Tables:
- [original_sample_table](LINK): 200 rows of unprocessed (raw, original) data
- [processed_sample_table](LINK): 200 rows of processed data

Table Images:
- [original_sample_table; Image 1](LINK)
- [original_sample_table; Image 2](LINK)
- [processed_sample_table](LINK)


## Communication/Organizational Protocols
- Different branches for individual Deliverables to keep work for each segment organized.
- Staying on top of my own work and troubleshooting using the Google when necessary.
