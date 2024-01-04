# Harnessing Large Language Models in Fake News Detection

by Anamaria Todor and Marcel Castro

## Introduction

Fake news, defined as news that convey or incorporate false, fabricated or deliberately misleading information, have been around as early as the emergence of the printing press. The rapid spread of fake news and disinformation online is not only deceiving to the public, but can also have profound impact on society, politics, economy and culture. Examples include:

- Cultivating distrust in the media
- Undermining the democratic process
- Spread of false or discredited science – for example the anti-vax movement

Advances in Artificial Intelligence and Machine Learning has made developing tools for creating and sharing fake news even easier. On the one hand, early examples include advanced social bots and automated accounts that supercharge the initial stage of spreading fake news. In general, it is not trivial for the public to determine whether such accounts are people or bots. In addition, social bots are not illegal tools and many companies legally purchase them as a part of marketing, thus it is not easy to curb the use of social bots systematically. 
Recent discoveries in the field of Generative AI (in particular text to text and text to image models) makes it possible to produce textual and rich content at an unprecedented pace with the help of Large Language Models (LLMs).  LLMs are Generative AI text models with over one billion parameters and they are facilitated in the synthesis of high-quality text.

In this blog post we explore how Large Language Models (LLMs) can be utilized to tackle the prevalent issue of detecting fake news, or in other words to “fight fire with fire”. We suggest that LLMs are sufficiently advanced for this task, especially if improved prompt techniques such as Chain-of-Thought and ReAct are used in conjunction with tools for information retrieval.  

We illustrate this by creating a LangChain application which, given a piece of news, highlights to the user whether the article is true or fake using natural language. The solution makes also use of Amazon Bedrock, a fully managed service that makes foundation models (FMs) from Amazon and third-party model providers easily accessible through the AWS console and API.

For a set-by-step description of the solution, please check our [AWS Machine Learning Blog entitled Harness large language models in fake news detection](https://aws.amazon.com/blogs/machine-learning/harness-large-language-models-in-fake-news-detection/).


## How to use this repository

This repository contains a [ChainOfThought](./fact-checker/fact_checker.py) and [ReAct](react/ReAct.py) implementation.

To run the scripts you can do:

```bash
python react/ReAct.py
```

or

```
python fact-checker/fact_checker.py
```



Both scripts make use of a shorter (4 statements) or longer (50 statements) from the FEVER dataset. Ref. [knowledge_qa_test.json](./knowledge_qa_test.json) and [knowledge_qa.json](./knowledge_qa.json).

