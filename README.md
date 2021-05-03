# E-Motion

E-motion is an emotion analysis solution that empowers marketers to write more impactful subject lines by identifying the intensities of the emotions conveyed in order to maximize email open rates.


## Installation

Use the package manager [pip](https://pip.pypa.io/en/stable/) to install any necessary packages, for example:

```bash
pip install guidedLDA
pip install textblob
pip install panel
pip install param
pip install pyldavis


pn.extension('plotly')
```

## Problem
Failure to segment, lack of personalization, and emails not adding value are the top reasons why promotional emails often get ignored. Emotional marketing involves arousing emotions that cause the consumers to act. Based on the Russell modeling diagram and the mood maintenance hypothesis, we focus on 6 targeted marketing emotions - enthusiasm, trust, inclusivity, surprise, greed and urgency. Although companies fail to keep these measures in mind when writing emails to attract their users, E-motion solves this problem by helping marketing organizations - like Oracle - use emotion to effectively automate marketing strategy and prioritize their email marketing efforts. 

The team’s primary goal was to accurately and efficiently determine the varying levels of intensity for particular marketing emotions portrayed by promotional subject lines. Emails are still a main medium for advertising, especially in areas of company recruitment and grocery shopping. As such, understanding the emotions evoked by email subject lines is extremely important in predicting email open rate. This is because certain emotions like trust or greed make people more likely to act on impulse than reason which can lead to a higher chance of them opening the specific promotional email. In this effort, E-motion would be a comprehensive tool to allow marketers to fully understand the emotions being provoked to fully exploit email subject lines to increase email open rates. 

## Detailed Solution 
Unsupervised Learning: In order to derive emotional intensity scores, GuidedLDA was utilized to determine emotion clusters and the probability each email subject line belonged to each cluster. At a high level, the unsupervised portion contains sections of data pre-processing, creating globe vectors, implementing guidedLDA, visualization of results through pyldavis, and comparison of guidedLDA results against manually labeled results. All related code in this analysis may be found in the unsupervised_learning folder. Ensure that all packages are installed when running the file unsupervised_learning_model.ipynb.
Supervised Model: Utilizing the labels produced by the unsupervised learning, convolutional neural network (CNN) and long short-term memory (LSTM) models were implemented. Pearson correlation was utilized to determine the performance of the models. All related code in this analysis may be found in the supervised_learning folder. 
User Interface: This neat UI utilized object oriented programming to present a dashboard that allows users to compare multiple subject lines based on emotional intensities and aids them in strategic marketing decisions. Users are able to compare and contrast up to five subject lines in any combinations they choose and scroll over each bar in the chart in order to view emotion intensity. The pie chart visualization provides an overall display of emotions conveyed and their respective proportions. With the graphics and data displayed by E-motion, marketers are better able to understand how varying diction can lead to different intensity levels of the target marketing emotions. With such analysis, marketers can customize email subject lines to fit along certain campaigns whether they are focused on evoking a sense of enthusiasm or urgency. All related code in this analysis may be found in the UI folder. 

## Usage
Download GloVe vector list [here](https://www.kaggle.com/yutanakamura/glove42b300dtxt/) to run notebooks in the supervised_learning folder. Under Supervised Model, copy and paste model dashboard code to activate UI.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/) - see LICENSE.txt file for details.
