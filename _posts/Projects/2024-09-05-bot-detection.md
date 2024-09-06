---
layout: post
current: post
cover:  assets/built/images/python-logo.png
navigation: True
title: Bot Detection
date: 2024-09-05 16:40:00
tags: [project]
class: post-template
subclass: 'post tag-python'
author: Jay Heo
---

I want to share about Topic modeling, speicifally LDA method. 

I had a chance to collobrate with Phd candidate in communication in Michigan State University, I worked as a data analyst to find out meaningful results from the data. I am not sure if I could say the contents of our research for now, so I will focus on LDA method rather than exact data description.. I will let you guys know after it publish!!

## LDA topic modeling

Latent Dirichlet Allocation (LDA) topic modeling is an iterative algorithm that uncover topics based on word frequency, which is discrete. LDAwas initially proposed in 2000 in a paper titled “Inference of population structure using multilocus genotype data.” The paper predominantly focused on population genetics, which is a subfield of genetics concerned with genetic differences within and among populations. Three years later, Latent Dirichlet Allocation was applied in machine learning. The intuition behind LDA is that documents usually refer to a small number of topics and topics usually based on small number of words. 

LDA is a Bayesian network, which means it's a generative model. It assumes that documents are made up of words and organizes the data by splitting the words in each document to create a corpus (a large group) of text. And it assigns topics to each of the words based on the number of topics a hyperparmeter. We choose the number of topics(hyper parameter) in each data using two methods CaoJuan2009 and Griffith2004. The best number of topics shows low values for CaoJuan2009 and high values for Griffith2004. 
So each dataset will have different number of topics. 

When LDA gets the number of topics, k, it assumes that these k topics are spread across all M documents. It then randomly assigns one of the k topics to each word in every document. So, each document gets topics, and each topic has a distribution of words. The process iterates, where each word in a document is reassigned a topic based on two criteria: 1) p(topic t | document d) : the proportion of words in the document that belong to a topic, and 2) p(word w | topic t): the likelihood of a word appearing in a topic. 
Consequently, this process converges, meaning all the words are properly assigned to topics, and as a result, documents are mapped to a list of topics by assigning each word in the document to different topics. LDA doesn't assign topic labels, but the user can look at the distribution of keywords in each topic and infer what the topic might be. With this topic lists, we could visualize with lots of vissualiaion tool.

In my research, the data was first categorized by AI-generated decision types, and each entry included explanations for why those specific decisions were made. I then conducted topic modeling for each decision type, which allowed me to identify the key terms associated with each type.

Like this! I generated four topics word cloud.

![image](https://private-user-images.githubusercontent.com/175622356/365229182-4baeb82f-88c1-44ff-8a7a-ead1b6f5b754.png?jwt=eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3MjU2MzgxNDIsIm5iZiI6MTcyNTYzNzg0MiwicGF0aCI6Ii8xNzU2MjIzNTYvMzY1MjI5MTgyLTRiYWViODJmLTg4YzEtNDRmZi04YTdhLWVhZDFiNmY1Yjc1NC5wbmc_WC1BbXotQWxnb3JpdGhtPUFXUzQtSE1BQy1TSEEyNTYmWC1BbXotQ3JlZGVudGlhbD1BS0lBVkNPRFlMU0E1M1BRSzRaQSUyRjIwMjQwOTA2JTJGdXMtZWFzdC0xJTJGczMlMkZhd3M0X3JlcXVlc3QmWC1BbXotRGF0ZT0yMDI0MDkwNlQxNTUwNDJaJlgtQW16LUV4cGlyZXM9MzAwJlgtQW16LVNpZ25hdHVyZT05ODk5NmYzNDgwNjI0NDQxMTg5MDk0YzAxMGUxNDE4OGE5M2JhODFmNGZhM2JmNmIxMTJlOTZmYTczNTk1ZTU3JlgtQW16LVNpZ25lZEhlYWRlcnM9aG9zdCZhY3Rvcl9pZD0wJmtleV9pZD0wJnJlcG9faWQ9MCJ9.Rxk7ekbwzpScQ4AzaqAuY5Uc9sytoGc8ulxrgdqCghw)


Reference: 
https://www.datacamp.com/tutorial/what-is-topic-modeling.
https://wikidocs.net/30708

