{:toc }
## Introduction
This program is meant to depict how one can set off the journey to NLP in R. The whole process of setting up a a twitter app from scratch so that one can access the credentials can be found [here](http://docs.inboundnow.com/guide/create-twitter-application/). Basically, one needs a twitter developer account where he/she can access the Consumer and Access tokens, secret and keys. 

  To reiterate what is inside the twitter-mining-101 notebook, there are a few requisites the one need to consider while setting up the workspace for NLP in R. It is important to consider either using R or R Studio, and incase one does not have access to this, there is a third option. You can alway consider using Google Colaboratory Notebooks that fully support R. [Check](https://colab.fan/r) here in order to set up one(my preference).  

## Data Cleaning
  Wisdom of the Crowds dictates that 80% of the time should be used for wrangling and cleansing while modelling takes only 20%. Thus the main objective here is to clean the unstructured dataset we acquired from twitter using the twitteR API. 

Remember, informal communication makes twitter data to be higly unstructured. Noise in the data is highly depicted eg the typos, poor grammar, Stopwords, emoji usage, and even sometimes URLs. 

For starters like I am, the following definitions give a hint of what we are going to do.
- Corpus - Refers to a list of text, ie the column named text in our june6th_df.
- Document - Refers to the separate text blocks in our corpus list. 
- Term - This refers to the individual wordings also known as unigrams. In laymans language, at every split after a whitespace do we find our term.

A bunch of packages will be required for this process.  Some important ones to be mention include `tm` for text mining and `corpus` that is used for vectorization. Other packages will need to be installed first.Remember that not at all times will the packages work. Especially in a localized sence where the tweets we need are not in english but a mixture of languages. This calls for regulare expression which have been used effectively especially to remove the emoticons. 

In this paper however, we will not discuss much on what `tm` library can do but you can check the documentation from [here](https://cran.r-project.org/web/packages/tm/tm.pdf) and likewise for [SnowballC](https://cran.r-project.org/web/packages/SnowballC/SnowballC.pdf). Just note that the use of `%>%` may not be neccessary but it beautifies our code.

Another definition comes. What do understand by **Term Document Matrix**? As it is accronymed tdm, it refers to a two dimensional matrix consisting of terms used in a corpus list/document in each cell. Mathematically, it is an $(i,j)$ representatio of the frequency of term $i$ in the document $j$.

## Visualizing Social Web Data.

A good instructor begins from the known to the unknow. For this article's sake, let us begin from visualizations using histograms first before we move on to a...

We can be able to build a wordle-esque word cloud. That's a heavy term that can make one's head burst yet easy after implementation.

## Conclusion. 

As depicted by the whole twitter analysis process, the #uhurudontliftlockdown  was the number one kenya's trending in twitter. The wordcloud and the bargraph show that nuhurudontliftlockdown was the most frequently used word. Many kenyans tweeted about the speech that was to be made by the President Uhuru Kenyatta on the 6th June concerning the lockdown. An assignment for you is to try and figure out why the words `time`, `address`, `today` and `wanjohi` were used more than 200 times. 


Now that we've started, let's keep going.
Stay tuned and be prepared for deeper twittr analytics using Machine learning methods such as Principal Component Analysis and Multidimensional Scaling. I believe that nothing in this world is difficult and in the same spirit we will walk through this.

Thank  you for reading this article. In case of any comments, compliments, and criticism you are welcome. Find me on twitter [@anon_rohi](https://twitter.com/anon_rohi), [rpubs](https://rpubs.com/RohiAnon) or on [linked in](https://www.linkedin.com/in/rohi-anon-38a026167/). You can also find [my github page](https://github.com/Rohianon).  All the best as continue coding
