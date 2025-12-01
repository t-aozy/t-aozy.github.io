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
Code and descriptions are available [here](https://github.com/t-aozy/AI-Chatbot-Development-with-LLM).
## Timeline: October 2023 - June 2024

## Research Focus
* **LLM with Retrival-Augmented Generation**
* **NLP: Similarity Search, Text classification**

## Overview
The goal for this project is to develop a professional AI Chatbot based on LLM for the diagnostic and doctor-patient communication specializing in the field of **Childhood Obesity**. We worked closely with doctors to obtain professional suggestions and knowledge.
To develop a better AI Chatbot for Childhood Obesity, we tried to build a Retrival-Augmented Generation(RAG) structure by constructing
our own external database for pre-trained Llama2 model. 

To construct the external database, I wrote website crawler code to grab Childhood Obesity professional content from professional website, 
also from Obesity-related papers provided by the doctors. When the LLM starts to work, it will conduct similarity search between user questions and text in the external database, then generates more professional results.

Moreover, in order to improve user experience, during practical deployment, the user's query is first passed through a text classification 
model. If the model determines that the query is not related to obesity, the system directly triggers a predefined AI chatbot to generate a specific response. If the model determins that the query belongs to the obesity domain, the system retrieves the processed FAISS vector database containinf curated medical data. If then computes the similarity between the user's query and the indexed documents, extracts the most relevant information, and loads a LLM to generate the final answer based on the highly relevant retrieved text.

## Structure Introduction

The overall model framework can be divided into **four main modules**:

### 1. Input Dataset Construction
To provide professional and accurate responses specifically targeting childhood obesity, we build a **custom dataset**. Data is collected from reputable journals and authoritative websites. Using the **LangChain** framework, these PDF-formatted documents are processed and stored in a **FAISS database** for efficient similarity search.

### 2. Large Language Model Configuration and Download
We select an appropriate model configuration and download the required large language model from **Hugging Face**. In this project, we use **Llama**, which offers strong performance in AI conversational tasks and is particularly suited for medical consultation scenarios.

### 3. Text Classification Model Training
To enhance the relevance of responses, we train a **FastText** model on our custom dataset. This model filters out user queries unrelated to childhood obesity, improving response accuracy and overall user experience.

### 4. Model Fine-tuning
To further optimize the large language model for our target task, we perform **supervised fine-tuning** using over 3,000 highly relevant training examples. This fine-tuning adjusts model parameters to specialize in answering questions related to obesity.


### Workflow
1. **Query Classification**:  
   User queries are first passed through the text classification model.  
   - If the query is unrelated to childhood obesity, the chatbot outputs a predefined response.  
   - If the query is related, the system retrieves **highly relevant data** from the FAISS database using similarity search.

2. **Contextual Answer Generation**:  
   The retrieved data is then fed into the **large language model**, which summarizes and integrates the information to provide a **final professional answer** to the user

## Code and Description
Detailed code and descriptions are available [here](https://github.com/t-aozy/AI-Chatbot-Development-with-LLM).

<img width="726" height="517" alt="image" src="https://github.com/user-attachments/assets/051ce6b7-842c-4bb7-ae3a-fb6a0699e6da" />

<img width="738" height="481" alt="image" src="https://github.com/user-attachments/assets/e458413a-0305-45be-89f6-05a37f2752c9" />
