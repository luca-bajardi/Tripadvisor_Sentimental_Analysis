# Tripadvisor Sentimental Analysis

In this project, I performed a sentiment analysis task, analyzing user’s textual reviews, to understand if a comment includes a positive or negative mood.
In practice, I built a robust classification model that is able to predict the sentiment contained in a text.

### The dataset

The dataset for this project has been specifically scraped from the [tripadvisor.it](https://tripadvisor.it) Italian web site. It contains 41077 textual reviews written in the Italian language.
The dataset is provided as textual files with multiple lines. Each line is composed of two fields: *text* and *class*. The *text* field contains the review written by the user, while the class field contains a label that can get the following values:
- *pos*: if the review shows a positive sentiment.
- *neg*: if the review shows a negative sentiment.

#### Dataset tree hierarchy
The data have been distributed in two separate collections. Each collection is in a different file.
The dataset archive is organized as follows:
- *development.csv* (Development set): a collection of reviews with the class column. This collection of data has to be used during the development of the classification model.
- *evaluation.csv* (Evaluation set): a collection of reviews without the class column. This collection of data has to be used to produce the submission file.
- *sample_submission.csv*: a sample submission file.

The dataset is located at:
[http://dbdmg.polito.it/wordpress/wp-content/uploads/2020/01/dataset_winter_2020.zip](http://dbdmg.polito.it/wordpress/wp-content/uploads/2020/01/dataset_winter_2020.zip)

### Task
You are required to build a classification pipeline to assign a label to each record in the Evaluation set.
The label specifies the sentiment of the review.

### Evaluation metric
Your submissions will be evaluated exploiting the [f1_score](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.f1_score.html) with the following configuration:

    from sklearn.metrics import f1_score
    f1_score(y_true, y_pred, average='weighted')


This project is a part of [Data Science Lab](https://dbdmg.polito.it/wordpress/teaching/data-science-lab-2019/) exam of [Polytechnic of Turin](http://www.polito.it).
