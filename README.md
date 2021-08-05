# SVM-based-handwritten-number-identifier
Python demonstrates a supervised machine-learning model, specifically using Support Vector Machine to translate handwritten numbers into their corresponding digits. [Read more about SVM here](https://en.wikipedia.org/wiki/Support-vector_machine). These correspond to the first two findings.
I also used SVM and KNN to detrmine factors of online news popularity based on attributes such as:
 - length of the article
 - the number of images
 - day of the week the article was published
 - some variables related to the content of the article
This corresponds to the final two findings. The data for this section can be downloaded [here](https://archive.ics.uci.edu/ml/datasets/Online+News+Popularity)

## Libraries used:
- sklearn (for use of svm and training data)
- pandas (for use of dataframes)
- numpy (for additional processing)

## Findings:
1. The decision tree seemed to have the best accuracy for this dataset at slightly above 60% accuracy. 
2. Scaling X (the data) improved accuracy between both the training and the testing data. Another parameter that influenced accuracy was k for the KNN model. [Read more about KNN here.](https://en.wikipedia.org/wiki/K-nearest_neighbors_algorithm) It had the most accuracy when k was in the 90s and with diminishing returns computationally when it was above that threshold. 
3. Ease of interpretation is a rather subjective measure for online news popularity. In this case, the decision tree is most useful not only because of its accuracy compared to SVM or KNN, but also in terms of displaying what criteria are most important for being considered "popular". [Read more about decision trees here.](https://en.wikipedia.org/wiki/Decision_tree)
4. Based on the results from the decision tree, the most significant indicator of popularity is kw_avg_avg (<= -0.242). The next big deciding factor is if the news article was published on the weekend, it was less likely to be popular. Additionally, if it was flagged as "entertainment" it was more likely to be popular. Other categories such as LDA influenced popularity, if the aritcle contained references to other popular articles it was less likely to become popular, and also the minimum keywords based on average shares was another indicator.
