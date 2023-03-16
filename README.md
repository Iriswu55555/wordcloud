![alt text](https://github.com/Iriswu55555/wordcloud/blob/a791973b838cef4d1289e61746d08b8ec3b273e9/Data_Analyst_skills.png)


# Core skills for Data-related job

This research aims to analyze job description data in the field of STEM-related jobs and identify specific skills required for them. The study utilizes tools such as skills keywords analysis by wordcloud to identify the most common skills required for certain jobs.

The study draws conclusions based on the data visualizations and provides recommendations for students who are seeking for data-related job. 

The research suggests that students should demand a diverse range of skills, including proficiency in programming languages such as SQL, Python, and R, expertise in data analysis. These skills are crucial for students who seeking data-related roles, like Business analyst or Data Analytics roles.


# What is Word Cloud?

Word Cloud is a data visualization technique used for representing text data in which the size of each word indicates its frequency or importance. Significant textual data points can be highlighted using a word cloud. Word clouds are widely used for analyzing data from social network websites. 

For generating word cloud in Python, modules needed are – matplotlib, pandas and wordcloud. To install these packages, run the following commands :

## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install foobar.

```bash
pip install wordcloud
```

## Usage

```python
import pandas as pd 
import csv
from wordcloud import WordCloud, STOPWORDS
from os import path
from PIL import Image
from wordcloud import WordCloud, STOPWORDS, ImageColorGenerator

import matplotlib.pyplot as plt

df = pd.read_csv('/Users/dodo/Desktop/required_skills.csv')

#delete Na. and blank
df.isna().sum()
df.dropna(inplace = True)
df.replace('\s+','',regex=True,inplace=True)

count = df['required_skills'].str.split(',').explode().value_counts()
print(count)
count.to_csv('counting_reuired_skills_Tableau.csv')

```

## Example 
A sample output is :

![alt text](https://github.com/Iriswu55555/wordcloud/blob/9ec83c886ae4e0de9670b67fab0aff6f7ab250d8/Picture1.png)


## Contributing

Pull requests are welcome. For major changes, please open an issue first
to discuss what you would like to change.
Please make sure to update tests as appropriate.

## License

The wordcloud library is MIT licenced, but contains DroidSansMono.ttf, a true type font by Google, that is apache licensed. The font is by no means integral, and any other font can be used by setting the font_path variable when creating a WordCloud object.

