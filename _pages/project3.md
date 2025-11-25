---
layout: archive
title: "Project3"
permalink: /project3/
author_profile: true
redirect_from:
  - /resume
kramdown:
  math_engine: mathjax
---

{% include base_path %}

# AI Chatbot Development with LLM

## Timeline: October 2023 - June 2024

## Research Focus
* **LLM with Retrival-Augmented Generation**
* **NLP: Similarity Search, text classification**

## Overview
The goal for this project is to develop a professional AI Chatbot based on LLM for the diagnostic and doctor-patient communication specializing in the field of **Childhood Obesity**. We worked closely with doctors to obtain professional suggestions and knowledge.
To develop a better AI Chatbot for Childhood Obesity, we tried to build a Retrival-Augmented Generation(RAG) structure by constructing
our own external database for pre-trained Llama2 model. 

To construct the external database, I wrote website crawler code to grab Childhood Obesity professional content from professional website, 
also from Obesity-related papers provided by the doctors. When the LLM starts to work, it will conduct similarity search between user questions and text in the external database, then generates more professional results.

Moreover, in order to improve user experience, during practical deployment, the user's query is first passed through a text classification 
model. If the model determines that the query is not related to obesity, the system directly triggers a predefined AI chatbot to generate a specific response. If the model determins that the query belongs to the obesity domain, the system retrieves the processed FAISS vector database containinf curated medical data. If then computes the similarity between the user's query and the indexed documents, extracts the most relevant information, and loads a LLM to generate the final answer based on the highly relevant retrieved text.

## Code and Description


<img width="726" height="517" alt="image" src="https://github.com/user-attachments/assets/051ce6b7-842c-4bb7-ae3a-fb6a0699e6da" />

<img width="738" height="481" alt="image" src="https://github.com/user-attachments/assets/e458413a-0305-45be-89f6-05a37f2752c9" />
