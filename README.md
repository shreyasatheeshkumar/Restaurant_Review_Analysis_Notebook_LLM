# Restaurant Review Analysis using LLM

## 📌 Overview

This project focuses on analyzing restaurant customer reviews using a Large Language Model (LLM) and Prompt Engineering.

The main goal is to extract useful insights from customer reviews and understand their experience with the restaurant. The analysis is performed using the Mistral-7B-Instruct model without using Retrieval-Augmented Generation (RAG).

## 🎯 Objectives

The project aims to:

- Identify the overall sentiment of each restaurant review.
- Analyze sentiment related to Food Quality, Service, and Ambience.
- Extract specific liked and disliked features from reviews.
- Generate polite and empathetic responses to customers.
- Demonstrate how Prompt Engineering can be used for automated review analysis.

## 🛠️ Technologies Used

- Python
- Pandas
- PyTorch
- Hugging Face Transformers
- Mistral-7B-Instruct
- Google Colab
- Prompt Engineering

## 📂 Dataset

The dataset contains restaurant customer reviews with the following columns:

- `restaurant_id` – Unique ID of the restaurant.
- `rating_review` – Rating given by the customer.
- `review_full` – Full text of the customer review.

The dataset contains **20 reviews and 3 columns**.

## 🔍 Project Workflow

### 1. Data Loading

The restaurant review dataset is loaded using Pandas and basic data exploration is performed.

### 2. LLM Model Loading

The `mistralai/Mistral-7B-Instruct-v0.1` model is loaded using Hugging Face Transformers.

8-bit quantization is used to reduce memory usage and make model inference more efficient.

### 3. Overall Sentiment Analysis

Each review is classified into:

- Positive
- Negative
- Neutral

The result is stored in a new `Sentiment` column.

### 4. Aspect-Level Sentiment Analysis

The reviews are further analyzed based on three important restaurant experience aspects:

- Food Quality
- Service
- Ambience

Each aspect is classified as Positive, Negative, Neutral, or Not Applicable.

### 5. Feature Extraction

The project extracts specific features that customers liked or disliked, such as:

- Food taste
- Food presentation
- Waiting time
- Staff behaviour
- Lighting
- Music
- Other review-specific features

### 6. Customer Response Generation

The LLM generates a polite and empathetic response based on the customer's review and sentiment.

- Positive reviews → Appreciative response
- Neutral reviews → Feedback-seeking response
- Negative reviews → Apologetic and supportive response

## 📊 Key Insights

The analysis showed that:

- Negative overall sentiment slightly outweighed positive and neutral feedback.
- **Service** was the most criticized aspect.
- **Ambience** received the strongest positive feedback.
- Food quality had more negative than positive feedback.

## 💡 Key Learning

This project demonstrates how **Prompt Engineering and Large Language Models** can be used to automatically analyze unstructured customer reviews and convert them into meaningful, structured insights.

It also shows how a single review can be analyzed at multiple levels, from overall sentiment to specific aspects and customer response generation.

## 🚀 Future Enhancement

The model's predictions can be further evaluated by manually labeling a subset of reviews and comparing the manual labels with the LLM-generated results.

## 📁 Project Structure

Restaurant-Review-Analysis/
│
├── Restaurant_Review_Analysis_Notebook.ipynb
└── README.md
