## Objective

To build a chatbot employing ML/DL techniques that can determine the accident level &
potential level involved in any accident based on the text description.



## Problem Statement & Abstract

With the advancement of technology, manual labour requirement in industries has reduced
considerably. However, it’s still a long way before industries achieve 100% automation.
Since human activity is involved, accidents & injuries are common despite all the safety
measures and precautions put in place. Such injuries can also prove fatal. Industrial
accidents can turn depending on the type of industry. For example, a mere spark in a
firecracker factory can burn the whole plant leading to loss of lives and property.
Workplace injuries are a big concern for both workers and management. It is imperative to
classify industrial incidents into different categories and determine whether the event was
merely an accident, due to negligence or by incompetence. This avoids reoccurrences,
reduce frequency of occurrence & severity and minimize the effects.
To achieve this we employ exploratory data analysis on a dataset from one of the biggest
Brazilian industries and find out the top reasons for industrial accidents, nature of accidents,
type of employees being injured and so on. We also aim to develop a chatbot application
using natural language processing to classify the accident into various critical risks by looking
at the description of the accident.


## Domain

Industrial Safety/NLP Chatbot


## Dataset 
[Link](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/data.csv)


The dataset is from one of the biggest industries in Brazil, having 12 different plants in 3
different nations. Each observation in the dataset corresponds to one accident. Data attributes are as below:


**Data:** Timestamp or time/date information

**Countries:** Country where the accident occurred (anonymised)

**Local:** City where the manufacturing plant is located (anonymised)

**Industry sector:** Sector which the plant belongs to

**Accident level:** I to VI, it registers how severe the accident was (I means not severe but VI
means very severe)

**Potential Accident Level:** Depending on the Accident Level, the database also registers how
severe the accident could have been (due to other factors involved in the accident)

**Genre:** If the person is male or female

**Employee or Third Party:** If the injured person is an employee or a third party

**Critical Risk:** Some description of the risk involved in the accident

**Description:** Detailed description of how the accident happened.


## Observations of EDA

Some highlights of Exploratory Data Analysis are as noted below:
- "Country_01" has maximum percentage of accidents (59.06%)
- Mining sector has maximum accidents with 241 incidents (56.71%)
- Maximum no of accidents belong to "Accident Level I" at 74.35%
- Top contributing factor for accidents is classified as "Others" 

## Data Preprocessing

Before using NLP model, the below text preprocessing steps were employed:
- **Word Tokenization** to tokenize text into words
- **Lemmatization** was preferred over Stemming to remove inflectional endings and return base form of dictionary words
- **Removing Stopwords** to allow the model to focus on contextual text
- Changing text case to lower
- Removing tokens which are not alphanumeric
- Removing punctuations


## Observations after Data Preprocessing


![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/distribution_characters_sentences.png)

Distribution of characters of all sentences

![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/words_in_description.png)

Distribution of words appearing in all descriptions

![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/average_word_length.png)

Average Word Length

![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/bigram_analysis.png)

Bigram analysis

![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/trigram_analysis.png)

Trigram analysis

![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/4gram_analysis.png)

Four gram analysis


## Modelling

For modelling both machine learning and deep learing algorithms have been used, compared performances of all the models and chosen the model with highest score. Objective is predict both ‘Accident Level’ & ‘Potential Accident Level’ labels, models for both these variables are generated and model giving best accuracy scores for both these variables are chosen.

**Machine Learning Models**
- Support Vector Classification
- Random Forest
- Gradient Boost
- XG Boost


**Deep Learning** 
Long Short Term Memory(LSTM) architecture with Word2Vec

**Text Preprocessing Techniques**  
- CountVectorizer
- TF-IDF


## Model Scores

### Machine Learning 

### 1. Accident Level
  - **Count Vectorizer**

| Score-Model | SVC | Random Forest | Gradient Boost | XG Boost |
 | :---: | :---: | :---: | :---: | :---: |
 | Training Score | 99.45% | 99.45% | 99.45% | 91.97% |
 | Test Score | 78.12% | 78.12% | 73.44% | 73.44% |
 
 
  - **TF-IDF**
 
 | Score-Model | SVC | Random Forest | Gradient Boost | XG Boost |
 | :---: | :---: | :---: | :---: | :---: |
 | Training Score | 99.17% | 99.45% | 99.45% | 95.57% |
 | Test Score | 78.12% | 78.12% | 73.44% | 76.56% |
 
 
 
### 2. Potential Accident Level
  - **Count Vectorizer**
  
 | Score-Model | SVC | Random Forest | Gradient Boost | XG Boost |
 | :---: | :---: | :---: | :---: | :---: |
 | Training Score | 99.72% | 99.72% | 99.72% | 19.94% |
 | Test Score | 39.06% | 37.50% | 42.19% | 40.62% |


  - **TF-IDF**

 | Score-Model | SVC | Random Forest | Gradient Boost | XG Boost |
 | :---: | :---: | :---: | :---: | :---: |
 | Training Score | 99.72% | 99.72% | 99.72% | 90.86% |
 | Test Score | 43.75% | 35.94% | 43.75% | 39.06% |



### LSTM with Word2Vec

| Accident Level | Potential Accident Level |
| :---: | :---: |
| 78% | 30% |


## Score Comparision

**Accident Level**

![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/score_accident_level.png)


**Potential Accident Level**

![alt text](https://github.com/MarurSrikanta/Chatbot-NLP/blob/main/Images/score_potential_accident_level.png)

## Result

From the tables and graphical representations seen above, SVC model using TF-IDF text preprocessing yields best results for both accident level and potential accident level variables, 78.12% and 43.75% respectively. This model is chosen.


                                          



