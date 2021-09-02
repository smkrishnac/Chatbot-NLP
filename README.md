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


## Exploratory Data Analysis

### Univariate Analysis

**Affected Countries**

