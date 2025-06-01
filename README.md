# Customer Support Ticket Classification & Entity Extraction

This project implements a machine learning pipeline to classify customer support tickets by their **issue type** and **urgency level**, along with extracting key entities such as product names, dates, and complaint keywords. It includes an interactive web app built with **Gradio** for both single-ticket and batch processing.

---

## Features

- **Text Preprocessing:**  
  Lowercasing, punctuation removal, stopword filtering, lemmatization, and sentiment analysis.

- **Feature Engineering:**  
  TF-IDF vectorization combined with ticket length and sentiment score for enhanced classification.

- **Multi-Class Classification:**  
  Logistic Regression models predict issue type and urgency level separately.

- **Entity Extraction:**  
  Rule-based extraction of product names, dates, and complaint keywords using regex and matching techniques.

- **Interactive Gradio Web App:**  
  User-friendly interface for analyzing individual tickets or uploading CSV/Excel files for batch processing.

---

## Installation

1. Clone the repo:
git clone https://github.com/yourusername/ticket-classification.git
cd ticket-classification


2. Create and activate a virtual environment (optional but recommended):
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

3. Install dependencies:

bash
Copy
pip install -r requirements.txt

4. Download necessary NLTK data:

import nltk
nltk.download('wordnet')
nltk.download('omw-1.4')

---
## Usage
Run the main script to start the Gradio app:
python app.py

-> Use the Single Ticket Analysis tab to input raw ticket text and get predictions.

-> Use the Batch Ticket Analysis tab to upload CSV or Excel files containing multiple tickets (must include a ticket_text column) for bulk predictions.

---
## Model Evaluation
-> Models were trained using Logistic Regression with TF-IDF, lemmatization, ticket length, and sentiment features.

-> Cross-validation was used to ensure model robustness.

-> Confusion matrices and classification reports are included for both issue type and urgency level.

---
## Insights & Challenges
-> Feature enrichment with sentiment and lemmatization improved accuracy.

-> Rule-based entity extraction was effective but can be enhanced with advanced NLP.

-> Robust error handling was implemented to manage batch input file inconsistencies.

---
## Future Work
-> Incorporate transformer-based embeddings for richer text representation.

-> Improve entity extraction with Named Entity Recognition (NER) models.

-> Enhance UI/UX with more detailed visualizations and user feedback.



