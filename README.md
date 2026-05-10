# Audience Analytics & Market Intelligence for Event Management
*A Natural Language Processing (NLP) pipeline developed for data-driven event organizing and stakeholder pitching.*

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![NLP](https://img.shields.io/badge/NLP-Transformers-orange)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-RoBERTa-success)

## Project Overview
This repository contains the architecture and methodology for an NLP-driven market intelligence project developed during my **Business and Decision Analytics Internship at Onlybees Pvt. Ltd.** (June - August 2025). 

Onlybees operates as a premier event organizing and ticketing platform (similar to BookMyShow). During my tenure, I contributed to the successful organization of major events in the Northeast, including the **Durand Cup** and the **Anuv Jain Concert**. 

The core challenge was to convince main organizers and high-profile artists that Onlybees was the most capable platform for their events in the Northeast region. To achieve this, I built an advanced NLP pipeline to analyze user comments, extract audience expectations, and structure our event services based on hard data.

## Business Objective
1. **Understand the Audience:** Determine exactly what services and experiences event-goers in the Northeast expect.
2. **Data-Driven Pitching:** Use empirical sentiment and topic data to convince organizers/artists that Onlybees possesses a unique, localized understanding of the market.
3. **Event Structuring:** Optimize event layouts, pricing, and services based on extracted user preferences to ensure maximum turnout and satisfaction.

## NLP Methodology & Architecture

To achieve a granular understanding of user comments, standard sentiment analysis was insufficient. Instead, I implemented a dual-model approach utilizing **BERTopic** and **Aspect-Based Sentiment Analysis (ABSA) with RoBERTa**.

### 1. Data Collection & Preprocessing
* Aggregated thousands of user comments from social media, forums, and past event reviews relevant to the Northeast demographic.
* Applied text normalization: tokenization, removal of stop words, and handling of regional slang/code-mixing.

### 2. Topic Modeling with BERTopic
* **What it did:** Grouped unstructured comments into distinct clusters to identify recurring themes without predefined labels.
* **Insights Gained:** Discovered that users highly prioritized factors like *seamless ticketing queues*, *local food vendor integration*, *secure parking*, and *VIP crowd management*.

### 3. Aspect-Based Sentiment Analysis (ABSA) via RoBERTa
* **What it did:** Fine-tuned a pre-trained **RoBERTa (Robustly Optimized BERT Pretraining Approach)** model to not just gauge overall sentiment (Positive/Negative), but to attach sentiment to specific *aspects* of an event.
* **Why RoBERTa?** It handles complex contextual nuances much better than traditional models like VADER or standard CNNs, which is crucial when reading sarcastic or highly emotional fan comments.
* **Example:** In the comment, *"Loved the music but the entry queue was a nightmare,"* the model accurately flagged positive sentiment for the "artist/music" aspect and negative sentiment for the "crowd management" aspect.

### Model Performance & Accuracy
The model was evaluated on a manually annotated test set of regional user comments.
* **Overall Sentiment Classification Accuracy:** **93.2%**
* **Aspect Extraction F1-Score:** **0.89**
* *The high accuracy gave us immense confidence to use this data directly in our B2B pitch decks.*

## Impact & Results
* **Competitive Edge:** The NLP insights provided a strategic advantage. Instead of relying on generic pitches, we showed artists (like Anuv Jain's management) a data-backed dashboard of what their Northeast fans specifically wanted.
* **Successful Execution:** Insights directly influenced how the Durand Cup and Anuv Jain concert were structured, from security deployment to vendor selection.
* **Audience Targeting:** Allowed the marketing team to tailor promotional campaigns hitting the exact keywords and services the NLP model identified as high-demand.

## Tech Stack
* **Language:** Python
* **NLP Libraries:** HuggingFace Transformers (RoBERTa), BERTopic, NLTK, spaCy
* **Data Processing:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn (for pitch deck charts)

