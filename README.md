# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Which subreddit does the post belong?

### Description 

In this project, I try to estimate which subreddit does the post belong knowing the post body or the title. 

### Problem Definition

In reddit, there are subreddits that are dedicated for different topics. For this project, I picked the subreddits of the TV shows Black Mirror and Westworld. The reason is that they are both having similar topics which is the misuse of technology by humans. (And also both are my favourite TV shows). 

In subreddits, the posts might have:
- a title (must-have)
- a video
- an image
- a post body

Apart from those information there are also some additional data about the post identification, which might be the creation date or the author name, post score etc.

### Scraping

In order to get this content, I used the Reddit API to identify what to scrap. With the help of this function, I was able to download 500 posts with their full content with a single run. After looping this function with the breaks of 1 second, I successfully got more than 10000 posts for each subreddit.

### Preparing the Model

As it is for all the data science projects, cleaning took a significant amount of time in this project because the content from an online source is messy. When it is considered that these are user-entered information that didn't follow any template, the necessity of this part can be understood. 

### Model Evaluation

Since I am trying to build a model that predicts a binary outcome, I picked Random Forest and Logistic Regression to be applied. In total there are four models that I built. These were trying to predict Black Mirror or Westworld using:
- the post titles in a Logistic Regression Model
- the post bodies in a Logistic Regression Model
- the post titles in a Random Forest Model
- the post bodies in a Random Forest Model

### Ways to Improve

This project has a big potential to grow. Its applications are very promising not only in this specific case but also in other topics like estimating which class a certain Tweet belongs. 

Another way to improve is to deal with model's overfitting. Test data has slightly lower accuracy score than the training data. That might be solved with a better regularization method than the one used in the model. 
