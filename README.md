# Project 2 - To Be or Not To Be

### Scope

The dataset used in this project (linked below) contains all character/player lines from all of Shakespeare's plays. The purpose of this project is to use feature engineering to generate new information that can be used in a classification model to determine which player is speaking. In other words, provided a player line, ideally the model will be able to predict which player is speaking.

### Results

The features that I created were: number of words per player line, average sentence length (per player line), number of sentences per player line. The classification models I used were: Decision Tree and Random Forest. The results from the models were very inaccurate, which I believe to be a result of poor feature choice and lack of feature variety. 

Please see the Jupyter Notebook for more details and further discussion.

### Data
Datasets obtained from:
1. https://www.kaggle.com/kingburrito666/shakespeare-plays

### Variable descriptions (of raw data, from kaggle)
- The first column is the Data-Line, it just keeps track of all the rows there are.
- The second column is the play that the lines are from.
- The third column is the actual line being spoken at any given time.
- The fourth column is the Act-Scene-Line from which any given line is from.
- The fifth column is the player who is saying any given line.
- The sixth column is the line being spoken.

### Variable descriptions (of final data)
- Play: the Play that the lines are from.
- PlayerLinenumber: the character's/player's line number (ie 1=that player's first line in the play)
- Player: the player who is saying any given line.
- PlayerLine: the line being spoken (contains the entire quote: all consecutive player lines from the raw data were combined to form a quote)
- quoteLength: the length of the PlayerLine
- AvgSentLen: the average length of sentences from PlayerLine (sum of sentence lengths/number of sentences)
- NumSentPerLine: the total number of sentences per playerLine

### References
To implement the Random Forest and Decision Tree models, I used the below tutorials:
1. https://www.datacamp.com/community/tutorials/decision-tree-classification-python
2. https://www.datacamp.com/community/tutorials/random-forests-classifier-python#algorithm
