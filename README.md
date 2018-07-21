# 100 Days of ML Code challenge

## Day 0: Friday, July 6, 2018
**Progress**: Studied search in non-deterministic environments from the [Artificial Intelligence: A Modern Approach](http://aima.cs.berkeley.edu/) Book

**Thoughts**: I have been following this book for a while. I first started by reading chapter 22 which covers NLP but then I started from the beginning and now I'm chapter 4. Searching algorithms in deterministic and nondeterministic environments are helping me understand AI more and in knowing how to approach open-ended problems. I'm hoping to finish this book and start implementing those algorithms one by one.

## Day 1: Saturday, July 7, 2018
**Progress**: Started the day looking into building a chatbot in the Kurdish Language. I had the preprocessing pipeline ready so I built a sequential Keras model. The data I used where recorded phone conversations. I kept having the loss getting stuck at certain values so to study the dataset further I started turning the data into a Neo4j graph to understand the language better. I will publish my work as soon as I reach interesting results. This is part of my [Applications of NLP on the Kurdish Language project](https://github.com/ammarasmro/Kurdish-Language)

**Thoughts**: Today just confirmed my belief that just because we have all the tools and fancy algorithms doesn't mean that we can just throw data at it without understanding what's happening. I think that those experiences are much more valuable than any lesson or any course.

## Day 2: Sunday, July 8, 2018
**Progress**: As another step in the Kurdish Language NLP applications. I tried to build a word embedding. I got my data from the [Kurdish Wikipedia](ku.wikipedia.com) and finished processing it into a useful format for such a task. I started training the embedding and will continue refining my network and verifying the results by asking a native Kurdish person to check the word similarity.

**Thoughts**: I have used embeddings many times but I had to brush up on my knowledge by following the tutorials on [TensorFlow](www.tensorflow.org) website and [Google ML crash course](https://developers.google.com/machine-learning/crash-course/ml-intro). My knowledge allowed me to get up to speed in less than a day but it also means that I need to keep practicing those skills so that I don't forget them.

Today's work: https://github.com/ammarasmro/Kurdish-Language/tree/master/utils


## Day 3: Monday, July 9, 2018
**Progress**: Today was a busy day so I tried to make up by reading the [Artificial Intelligence: A Modern Approach](http://aima.cs.berkeley.edu/). I studied section 4.4.1 Searching with no observation and explored how belief states can be utilized to replace sensors.

**Thoughts**: I was surprised to know that there are problems that can be completely solved without any input from sensors. It's true sensors do give valuable input but they are a very expensive component. However this method, if not designed properly, can introduce exponential complexity to the solution.

## Day 4: Monday, July 10, 2018
**Progress**: Today was good for both learning and coding. I started the day with an hour on the Deep Reinforcement Learning Nanodegree on Udacity. Next, to do some coding I started a new open-source project aimed to help me practice building chatbots and to also be a learning path for someone just entering the field.

**Thoughts**: I'm very excited for the Deep RL course and I can't wait to learn how to incorporate it within my projects. I have been looking for such a resource for a long time. The beauty of Udacity courses is that they are very well structured and they gather the right resources from so many places. My favourite part is always the suggested readings.
As for the chatbots project, I think that it's necessary to take a step back and go to the basics before relying on fancy algorithms to do the job and I think that journey will help me grow in the Natural Language Processing field.

Today's work: https://github.com/ammarasmro/chatbots-zero-to-hero


## Days 5, 6, 7: July 10 to 12, 2018
**Progress**: During the last few days I was working on gathering and cleaning data for a Kurdish word embedding. Having word embeddings helps in many applications as it adds semantic knowledge to our model by representing data in a way that reflects its true meaning in a way that is useful for our model. One cool thing about embeddings is the ability to visualize them and see which words are clustered together. I chose to do this mini project for several reasons:

* I can barely speak the language and the data is in different dialects
* I haven't seen any efforts to do this task for the Kurdish language
* I like challenges

The scope of this project needed to be specific to fit into the challenges requirements and to be finished quickly. So, I narrowed it down into the Sorani dialect and got the data as an xml dump from the [Sorani Kurdish Wikipedia](ckb.wikipedia.com).

Next, came the data preparation part. I looked at how TensorFlow documentation does this and they used a dataset of concatenated words called text8. I used a pipeline that I built on Day 2 of the challenge, plus the WikiExtractor tool, to extract data from the dump and prepare it for training. I have also included this dataset on my GitHub for anyone to download and use. It does need a bit of cleansing but it will do for my current applications.

[**Sorani text8**](https://github.com/ammarasmro/Kurdish-Language/blob/master/utils/text8.txt)

[**Kurmanji text8**](https://github.com/ammarasmro/Kurdish-Language/blob/master/utils/text8ku.txt)

For the training part, I followed the embeddings tutorials on the TensorFlow documentation and even with 28 MB of text the results are impressive. Here are few of the results that caught my eye:

Query | Nearby words | English category
--- | --- | ---
شوباتی | نیسانی, حوزەیرانی, ڕۆژی, ئازاری | Months
عێراق | ئێران, جەزائیری, ئەڵمانیا, ڕوسیای, تورکیا | Countries
عەرەبی | فارسی, کوردی, ئینگلیزی | Languages

The last day was spent on getting the data representation to work on a static website so that I can share it. Finally found the widget that does just that. You can find the visualization here. I will try to train better models and upload them soon but the current one isn't so bad.

To start just go to [The project's website](https://ammarasmaro.com/Kurdish-Language/)

Here is a peek at what to expect and how to navigate it.
To start

![Starting](https://github.com/ammarasmro/Kurdish-Language/blob/master/visualizations/start.gif)

To query for a word

![Query](https://github.com/ammarasmro/Kurdish-Language/blob/master/visualizations/query.gif)

To switch to t-SNE

![t-SNE](https://github.com/ammarasmro/Kurdish-Language/blob/master/visualizations/tsne.gif)



**Thoughts**: I'm glad I did this mini project. It gave me confidence to pursue further similar projects and it will sure be beneficial to include in the next projects.


## Days 8 & 9: July 14 & 15, 2018
**Progress**:
* Covered the policy and state-value and action-value functions of the Reinforcement Learning ND on Udacity. As part of that I also read chapter 3 of the [Reinforcement Learning: An Introduction](http://incompleteideas.net/book/bookdraft2017nov5.pdf) which covered the same concepts.
* Explored the talkthewalk dataset published by Facebook few days ago and read the pre-write of their paper. This dataset aims to be the basis of a new approach to teaching computers how to communicate in natural language. In the next few days I will try to tackle this problem from different angles and see if I can add value to what they found.
* Started working on a prototype for the Kurdish NLP website.

**Thoughts**: Those two days were spent mostly learning but they paved the way towards several days of experiments and research.

## Days 10: July 16, 2018
**Progress**:
* Implemented several Dynamic Programming algorithms as part of the Deep Reinforcement Learning ND on Udacity. The algorithms were:
  * Iterative policy evaluation
  * Estimation of Action Values
  * Policy Improvement
  * Policy Iteration
  * Truncated Policy Iteration
  * Value Iteration

* Improved the Progressive Graph Builder API (ProGBA) on a private repo and will start open-sourcing parts of it soon.
[Demo web app](http://ammarasmaro.com/progba-web-app/)


**Thoughts**: Even though dynamic programming algorithms were so simple yet they proved very effective. However, they are limited by the fact that they require full knowledge of the Markov Decision Process (MDP), which isn't feasible in real world environments.
As for the ProGBA project. It seems to be getting to the end result but I believe that it's time to demo it to decide how to move forward.

## Days 11 and 12: July 17 and 18, 2018
**Progress**:
* Trained an end-to-end Automatic Speech Recognition (ASR) model to turn Kurdish, language, speech into text. It uses a deep neural network with
 1. One convolutional layer
 2. Two bidirectional RNN's
 3. A time distributed dense layer

 This model was trained using phone conversations in the Kurmanji dialect with their hand annotated scripts.

**Thoughts**: The use of the convolutional layer proved very useful in recognizing patterns for this task. Especially that phone conversations can be particularly harder than usual audio datasets of people reading books. Audio conversations contain many uniquely spoken words, alot of noise, and alot of silence. The dataset was also small, so I didn't expect much from it. However, it seems to work well for words that occur more often than others, such as numbers. Another part that caught my attention was that in Kurdish, there are letters that are very similar and the model was often able to detect that difference.

Further development could include adding a language model at the end to enhance the quality of the resulted words. Dropout layers could also be added to avoid the overfitting too.

Today's work: https://github.com/ammarasmro/Kurdish-Language/tree/master/speech-recognition

## Day 13: July 19, 2018
**Progress**:
Today I decided to go back to the basics and start from the most naive algorithms, Naive Bayes. I used it on a FIFA worldcup dataset on Kaggle to predict if a member of the playing team got the "Man of the Match" title in a match.

**Thoughts**: With some processing and improvement I got 69.7 % accuracy. It's not state of the art but with a dataset as small as this one, with 128 rows only, those results are a good start.

Today's work
https://www.kaggle.com/ammarasmaro/naive-approach/notebook
