# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & NLP

### Overview

For project 3, we will be pulling and analyzing a group of posts from two subreddits:
- **ExplainLikeImFive (ELI5)** - Explain Like I'm Five is the best forum and archive on the internet for layperson-friendly explanations. Don't Panic!
- **AskScience** - Ask a science question, get a science answer.


---

We will be analyzing a random collection of posts from two subReddits, **ExplainLikeImFive** and **AskScience**, in order to build a model to predict if an individual posts belong to ELI5 or AskScience; we will be analyzing the Title and Body of the Post.

---

### Problem Statement
**What am I hoping to achieve with this?**
> If ELI5 is distinguishable from AskScience.

**Why?**
> To see if a subreddit focused on explaining things in a simple manner is that much different than a subreddit that wants to explain it any way they can.

---


### Datasets

The dataset we will be using are scraped using Pushift Reddit API. 10,000 posts or submissions are pulled from both of our two subreddits, filtering for posts that were removed by the original publisher (OP) or a Moderator (mod).

After a cleaning process, we removed posts that only contained text in the title with no text in the body, or selftext, section of the post. This is because we wanted to ensure the model was as accurate as possible, utilizing as much data as we could give it to classify individual posts.


---

### Analysis

The datasets were cleaned of erroneous data and explored to find the top words found in each subreddit, after accounting for filler or other words that did not provide value to our model; for example, 'www', 'com', 'wikipedia', and other words such as these. 

Our datasets were then combined and passed to three different models, using a combination of CountVectorizer, TfidfVectorizer, RandomForestClassifier, and KNeighborsClassifier. The performance of these models was analyzed and used to determine if there was distinguishable differences between ELI5 and AskScience.


---

### Conclusion and Recommendations

**We found that the models, while none of them were perfect, all pointed to the conclusion that these Subreddits are distinguishable.** 
>Therefore, if you want to ask a question about something scientific, but don't have a strong domain knowledge, ELI5 would be a good choice. If you believe you could understand some terminology and domain knowledge AskScience will give a more in depth answer.