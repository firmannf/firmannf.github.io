---
layout: post
title: "Hello Kotlin, Nice to Meet You!"
description: "My first experience using Kotlin to make a simple android app"
tags: [Android, Kotlin, Android Studio]
comments: true
---

### Preliminary
Since one month ago, I've been feeling interested with **text mining** and **machine learning**. In the learning process, I found some **alien** words for me. One of that is **TF-IDF**.<!-- more -->

<br/>

### What is TF-IDF
Based on <a href="http://www.tfidf.com/" target="_blank">`tfidf.com`</a>, TF-IDF stands for **Term Frequency - Inverse Document Frequency**. And then, show up new **alien** word again, that is **TF-IDF weight**. 

> TF-IDF weight is a statistical measure used to evaluate how important a word to a document in a collection of documents. - <a href="http://www.tfidf.com/" target="_blank">tfidf.com</a>

<br/>

### How to Determine TF-IDF Weight

* First, we have to compute Term Frequency (TF). TF measures how frequently a word appeared in a document. The formula is `number of times a word show up in the document divided by total number of words in that document`.
* Second, we have to compute Inverse Document Frequency (IDF). IDF measures how important a word. The formula is `log(total number of documents divided by number of documents where the word appeared)`.
* Third, finally we have to compute TF-IDF weight. The formula is `TF multiplied by IDF`

<br/>

### Example
There is a document with 50 words in it. The word **book** appears 5 times. The TF for **book** is `5 / 50 = 0.1`. I have 1000000 documents and the word **book** appears in 1000 document. so the IDF is `log(1000000 / 1000) = 3`. And then the TF-IDF weight is `0.1 * 3 = 0.3`. 

<br/>

### References

* <a href="http://www.tfidf.com/" target="_blank">http://www.tfidf.com/</a>