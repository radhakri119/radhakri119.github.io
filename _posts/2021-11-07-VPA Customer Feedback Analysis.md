---
layout: post
title: "Comparative Analysis of VPAs - Siri, Alexa, Google Assistant (WIP)"
subtitle: "Project Report"
date: 2021-11-07 10:45:13 -0400
background: '/img/posts/02.jpg'
---

## Link
[https://github.com/radhakri119/Virtual-Private-Assistants-Customer-Feedbacke]( https://github.com/radhakri119/Virtual-Private-Assistants-Customer-Feedback ).

# Virtual-Private-Assistants-Customer-Feedback

## Introduction

We want to analyze customer feedback for Alexa, Google Assistant and Siri to extract themes from customer feedback.

## Data

We use a tool called [Octoparse](https://www.octoparse.com/) to extract reviews from Amazon, BestBuy and other websites which mention a Virtual Private Assistant (VPA) like Siri, Alexa or Google Assitant. This data is stored in [data.csv]( https://github.com/radhakri119/Virtual-Private-Assistants-Customer-Feedback/blob/main/data_raw.csv )

## Analysis

We analyzed the reviews with VPA mentions using a RoBERTa pre-trained Language Model. We visualized the embeddings using a 2D projection algorithm like UMAP, extracted themes manually, and used these labeled themes to fine-tune the RoBERTA model. We iterated this procedure multiple times to extract a good set of themes for each VPA. We then compared the customer feedback for all VPAs to understand the strengths and weaknesses of each VPA.

![UMAP Projection](/img/posts/UMap_Projection.png "UMAP Projection")
