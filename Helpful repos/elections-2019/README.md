To run the program

Prior to running of the program , extract the following zip files inside electionsentiment folder
a. old-data.zip, b. publicsentiments.zip, c. train.zip


1. Crawl tweets :

cd  electionsentiment/analysis/twittercrawler

python crawlTweet.py


2. Merge tweeets crawled weekly [ electionsentiment/old-data contains tweets crawled in past weeks, that will be merged]

python mergeTweets.py

The above command will generate the merged files corresponding to Bjp, Congress, both parties , other parties at

electionsentiment/train/raw/LokShobaElc2019... .csv


3. Clean Tweets, process hashtags, url, emojis, retweet_counts and generate train and test datasets

cd   electionsentiment/analysis/tweetprocessor

python preprocessTweets.py


4. Run Analytics for party wise comparison charts and polarized tweet classification

cd electionsentiment/algorithms

python sentimentPlots.py

python polarizedTweetPlots.py


5. Run mood prediction algorithms

a.  cd electionsentiment/algorithms

b. python fasttextClassify.py

c. python nltkClassify.py

d. python bagging.py

e. python boosting.py

f. python stacking.py

g. python  classifygloveattlstm.py [Deep learning models based on Word2Vec Embeddings]

10 python classifyw2veclstm.py  [Deep learning LSTM based models]

11 python classifyw2veccnn.py  [Deep learning CNN based models]


Links of blogs published in Analytics Vidhya

1.https://techairesearch.com/sentiment-analysis-using-deep-learning-techniques-with-india-elections-2019-a-case-study/
2.https://techairesearch.com/elections-2019-mood-classification-with-text-based-classifiers-ii/
3.https://techairesearch.com/sentiment-classification-for-2019-elections-using-text-based-classifiers-i/
4.https://techairesearch.com/twitter-sentiment-analysis-for-the-2019-election/
5.https://techairesearch.com/boosting-bagging-and-stacking-a-comparative-analysis-2019-india-elections-case-study/
