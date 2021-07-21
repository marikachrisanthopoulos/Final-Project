# Final-Project - Deliverable 1

## Presentation

### Selected Topic and Reasoning

**Topic**: prevalent characteristics amongst dogs that are put up for adoption.

**Characteristics of Interest:**
- Age
- Sex
- Breed
- Time of Year found
- Color
- Coat
- Size

**Reasoning:**
I am interested in determining whether certain types of dogs are more likely to be put up for adoption than others, based on the listed characteristics. I chose this topic because I am a lover of all animals, specifically dogs, and have had the wonderful pleasure of taking care of two different adopted dogs in my life so far. I believe that learning more about the dogs that are put up for adoption can help organizations and breeders prevent animals from being put up for adoption, while informing the general population of which kinds of dogs they can bring into their homes and provide better lives.

### Source of Data
The dataset for this project was found on Kaggle.com - click [here](https://www.kaggle.com/jmolitoris/adoptable-dogs?select=ShelterDogs.csv) to view the original source. Below, you can find a summary of the dataset written by the owner (taken directly from Kaggle):

"The data is a compilation of information on dogs who were available for adoption on December 12, 2019 in the Hungarian Database of Homeless Pets. In total, there were 2,937 dogs in the database. It contains information on dogs' names, breed, color, age, sex, the date they were found, and some characteristics of their personalities."

**Data Summary:**
- File: [ShelterDogs.csv](https://github.com/marikachrisanthopoulos/Final-Project/blob/Deliverable_1/Original_Dataset/ShelterDogs.csv)
- Total Columns: 19
- Total Rows: 2938 (including headers)
- Analyzable Columns:
    - Age (missing: 0/2938)
- Removable Columns:
    - ID (irrelevant)
    - Name (irrelevant)
    - Neutered (missing: 1085/2938)
    - Housebroken (missing: 2477/2938)
    - likes_people (missing: 938/2938)
    - likes_children (missing: 1718/2938)
    - get_along_males (missing: 1304/2938)
    - get_along_females (missing: 1254/2938)
    - get_along_cats (missing: 2506/2938)
    - keep_in (missing: 1021/2938)

The data listed above under "Analyzable Columns" will be analyzed to determine trends. None of the data for these characteristics are missing, which provides an excellent and complete dataset for this analysis. The data in the "Removable Columns" section is going to be removed from the analysis because the data is either irrelevant (ID, Name) or has a significant amount of data missing in comparison to the total number of dogs included in the dataset.

### Questions/Goals

**Questions**
1. Are dogs of certain ages more likely to be put up for adoption?
2. Are male or female dogs more likely to be put up for adoption?
3. Are dogs of unknown breeds more likely to be put up for adoption than dogs whose breeds are known?
4. Are dogs put up for adoption at certain times of the year (winter, spring, summer, fall) more likely to be put up for adoption than others?
5. Are dogs of certain colors more likely to be put up for adoption than others?
6. Are dogs of certain coats (short, medium, long, wirehaired) more likely to be put up for adoption than others?
7. Are dogs of certain sizes (small, medium, large) more likely to be put up for adoption than others?

**Goals**
1. Discover trends in individual characteristics of adoptable dogs by analyzing the dataset.
2. Discover related trends in characteristics of adoptable dogs by analyzing the dataset and determining whether there are significant relationships between certain attributes.

## Machine Learning Model

## Database
The database for this project was created using AWS (Amazon Web Services), in collaboration with pgAdmin4 and Google Colaboratory/PySpark. I used similar methods/procedures as those completed in Module 16 (Big Data) in order to create my database and connect it to pgAdmin.

AWS Database: final-project.cwiwfogyf7o4.us-east-2.rds.amazonaws.com


## GitHub

### Communication Protocols
In order to ensure all the work for each deliverable is completed correctly, different branches will be used for each deliverable (ex: all the work for this first deliverable will be in the branch "Deliverable_1." After completion of the entire project, all of the necessary materials from each deliverable will be merged.

Due to challenges and time constraints at my job (losing multiple staff members and being promoted during this exact transitional time, resulting in my having to take on the work of two positions at once), I am completing this project on my own. I have taken time off work (as we finally had a new employee start two weeks ago who can take on some of my responsibilities) to complete this project and any outstanding work for this class that I have fallen behind on. While I understand this was supposed to be a group project, I had situational factors impact my ability to work in a group with others, and will do my best to complete this project on my own by the end of the course.
