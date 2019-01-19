# :rocket: A Starter Guide to Chatbot Engineering

[![made-with-python](https://img.shields.io/badge/Made%20with-Python-1f425f.svg)](https://www.python.org/)
[![MIT license](https://img.shields.io/badge/License-MIT-blue.svg)](https://lbesson.mit-license.org/)
![tested-on-osx](https://img.shields.io/badge/Tested%20on-OSX-lightgrey.svg)

## Readings
* [Chatbot Fundamentals](https://apps.worldwritable.com/tutorials/chatbot/) by [Liza Daly](https://lizadaly.com/), former CTO at Safari; it's an interactive guide with hands-on coding experience to teach some of the methods and tools useful for building a **rule-based open domain** chatbot (Brobot).
* [Building a Simple Chatbot from Scratch in Python](https://medium.com/analytics-vidhya/building-a-simple-chatbot-in-python-using-nltk-7c8c8215ac6e), uses and explains a lot of concepts in NLP like tokenization, stemming, bag-of-words, tf-idf, and cosine similarity to build a very simple **rule-based** chatbot.
* [Writing a Google API MapBot from scratch and deploying on Facebook Messenger](https://chatbotslife.com/how-i-developed-my-own-learning-chatbot-in-python-from-scratch-and-deployed-it-on-facebook-88bc828be0a8), talks about how to use the StanfordCoreNLP, SK-Learn, MySQL, and GoogleMapsAPI and FacebookMessengerAPI to build a simple **rule-based task-orientated** chatbot. It provides a nice example on how to design dialog.
* [Conversational AI](https://chatbotslife.com/conversational-ai-understanding-the-basics-and-a-chatbot-build-in-rasa-module-c23828307180), gives a brief history of chatbot, explains the basic concepts, compares **Dialogflow** vs **Rasa**, and an example of how to build a **task-orientated** chatbot with companion [source code](https://github.com/manikandanj2207/dataibreathe).

## Libraies
* [Dialogflow ask API.AI](https://dialogflow.com/docs/getting-started): a closed-source Google-owned API that uses NLP and Machine Learning to provide an end-to-end Chatbot model. It can easily integrate with 3rd party platforms, making deployment simple.
  * [Here](https://moz.com/blog/chat-bot) is a demo on how someone used API.AI to build a food ordering chatbot on Slack.
* [Rasa NLU + Core](https://rasa.com/docs/nlu/): an open-source library. The NLU module provides NLP tools for **intent classification** and **entity extraction**. While the Core module handles **dialogures** and **fulfillment**.
  * Nahid Alam wrote a [great tutorial](https://towardsdatascience.com/a-chatbot-from-future-building-an-end-to-end-conversational-assistant-with-rasa-ai-51a1c93dabf2) on Towards Data Science on how to use Rasa.
  * Nathaniel Kohn, Data Scienist at Lemonade, also have a more technical one on [building a pizza ordering chatbot](https://hackernoon.com/build-simple-chatbot-with-rasa-part-1-f4c6d5bb1aea)
* [ChatterBot](https://github.com/gunthercox/ChatterBot): an open-source python library that uses a selection of machine learning algo to produce different types of responses
  * Ruan Bekker wrote a [simple tutorial](https://blog.ruanbekker.com/blog/2017/12/13/create-a-chatbot-with-chatterbot-on-python/) on how to quickly build a chatbot using Chatterbot.
* [TextBlob](https://textblob.readthedocs.io/en/dev/): an API for diving into common NLP tasks (e.g. POS tagging, noun phrase extraction, sentiment analysis, classification, translation, etc.)
* [spaCy](https://spacy.io/): another NLP API built in CPython that excels at large-scale information extraction, aka Speed.

## Interesting Projects
* [ELIZA](http://psych.fullerton.edu/mbirnbaum/psych101/Eliza.htm?utm_source=ubisend.com&utm_medium=blog-link&utm_campaign=ubisend), the first Chatbot that started it all. Written by Weizenbaum ina 200 lines of code back in 1966.
* [Awesome Chatbots](https://github.com/JStumpp/awesome-chatbots)
* [Awesome Chatbots... including Chinese ones](https://github.com/fendouai/Awesome-Chatbot)
* [Wall Street Bot](https://github.com/TarangKhanna/Wall-Street-Bot): flask, python, API.AI

## A Very Brief Intro to Chatbots
### Task-orientated vs Open Domain
#### Task-orientated
![image of task-orientated chatbot](https://cdn-images-1.medium.com/max/800/1*2c7v8bwGxJbkglxGhuTiJA.jpeg)  

Fits most real-world business needs and trained in a specific domain to handle a few particular tasks.  
#### Open Domain
Where the conversation can go anywhere on an infinite number of topics. [mitsuku](https://www.pandorabots.com/mitsuku/) and [DeepQA](https://github.com/AbdelrahmanRadwan/Open-Domain-ChatBot) are two examples.
### Rule-based vs Self learning
#### Rule-based
Answers are generated based on rules that it's been trained on. This type of bots can handle simple queries but fail at complex ones
#### Self-learning
Uses Machine Learning approach that's more efficient than rule-based and are of two types...
##### Retrieval Based vs Generative
* **Retrieval**: using **heuristic** to select a response from a library of predefined responses
* **Generative**: bots generate original answers

### Recurrent Neural Network (RNN)
![image of RNN](http://complx.me/img/seq2seq/lstm.png)  

Context is important in language, which is why RNN, networks with embedded loops that allow pass information to persist, is a good match for training Chatbots.

Siraj, the Youtube Star, explained how to use TensorFlow to build an RNN based Chatbot in [this video](https://www.youtube.com/watch?v=SJDEOWLHYVo&index=66&list=WL&t=0s) with the companion [source code](https://github.com/llSourcell/tensorflow_chatbot).

#### Long Short Term Memory Networks (LSTMs)
LSTMs are a special kind of RNN that has preformed particular well because it excels at retaining long-term memory of the dialog flow. [Understanding LSTM Networks](http://colah.github.io/posts/2015-08-Understanding-LSTMs/) by Chris Olah, a Google Brain Research Scientist, talks in depth about how they work.

#### Sequence to Sequence Learning (Seq2Seq)
![image of seq2seq](http://complx.me/img/seq2seq/seq2seq2.png)

Seq2Seq models consist of two RNNs: an encoder RNN and a decoder RNN. The encoder reads the input sentence and is responsbile for emitting a context. Based on the context, the decoder generates the output sequence. [This github repo](https://github.com/tensorlayer/seq2seq-chatbot) have some sample code on building a Seq2Seq chatbot.

## Portfolio
1. A translation Chatbot
2. A HK home price prediction Chatbot
3. A trading assistant Chatbot
4. A traditional chinese Chatbot from scratch
