# ⚽ Sports News Classification Using IndoBERT

## 📌 Project Overview

This project focuses on classifying Indonesian sports news articles using **IndoBERT**, a pre-trained language model for Indonesian text. The project compares two classification approaches: one-stage classification and two-stage classification.

The objective is to categorize news articles into football league categories and non-football news using Natural Language Processing (NLP) and transformer-based deep learning.

## 🎯 Project Objectives

- Collect Indonesian sports news articles from online news sources.
- Prepare a labeled dataset for text classification.
- Implement IndoBERT for news categorization.
- Compare one-stage and two-stage classification approaches.
- Evaluate model performance using accuracy, precision, recall, and F1-score.

## 📂 Dataset

The dataset consists of **1,090 news articles** from two Indonesian news media sources: Detik and Antara.

| Attribute | Description |
|---|---|
| Total articles | 1,090 |
| Data sources | Detik and Antara |
| Text column | `text` |
| Source column | `media` |
| Target column | `label` |
| Number of categories | 5 |

### 🏷️ News Categories

| Category | Number of Articles |
|---|---:|
| Non Sepak Bola | 376 |
| Liga Inggris | 200 |
| Liga Indonesia | 175 |
| Liga Italia | 172 |
| Liga Spanyol | 167 |
| **Total** | **1,090** |

## 🕸️ Data Collection

Web scraping techniques were used to collect news articles from online news sources. The data collection notebook uses Python libraries such as `requests` and `BeautifulSoup`.

The collected data is organized into a structured dataset containing article text, media source, and category labels.

## 🧹 Data Preparation

The dataset is prepared for text classification by organizing article content and its corresponding labels. The data is then split into training, validation, and testing sets using a stratified splitting approach to preserve class proportions.

The classification notebook uses tokenization with a maximum sequence length of 256 tokens.

## 🧠 Methodology

### 1️⃣ One-Stage Classification

In the one-stage approach, the model directly classifies each article into one of five categories:

- Liga Inggris
- Liga Italia
- Liga Indonesia
- Liga Spanyol
- Non Sepak Bola

### 2️⃣ Two-Stage Classification

The two-stage approach separates classification into two steps:

- **Stage 1 — Binary Classification:** Distinguishes football news from non-football news.
- **Stage 2 — League Classification:** Classifies football news into four league categories.

Both approaches are evaluated to compare their performance on the news classification task.

## 🤖 Model and Technologies

The main model used in this project is **IndoBERT**, specifically `indobenchmark/indobert-base-p1`, implemented using the Hugging Face Transformers library.

Technologies and libraries include:

- Python
- Pandas and NumPy
- Requests and BeautifulSoup
- Hugging Face Transformers
- PyTorch
- Scikit-learn
- Matplotlib and Seaborn

## 📊 Model Evaluation

Model performance is assessed using four evaluation metrics:

- **Accuracy:** Measures the proportion of correctly classified articles.
- **Precision:** Measures how many articles predicted as a category belong to that category.
- **Recall:** Measures how many articles from a category are correctly identified.
- **F1-score:** Combines precision and recall into a single metric.

### 📈 Two-Stage Classification Results

The following test results are reported in the classification notebook:

| Classification Stage | Test Accuracy | Test F1-score |
|---|---:|---:|
| Stage 1: Football vs. Non-Football | 98.80% | 98.80% |
| Stage 2: Football League Classification | 93.58% | 93.56% |

The notebook also evaluates the one-stage approach and compares the classification strategies. Its reported one-stage metrics should be checked against the final evaluation output before being published as definitive results.

## 💡 Key Takeaways

- IndoBERT can be applied to Indonesian-language news classification.
- The project explores both direct multi-class classification and a hierarchical two-stage approach.
- The two-stage model reports strong test performance for football detection and football league classification.
- Comparing multiple approaches provides insight into different ways of structuring a text classification problem.

## 🎯 Project Scope

This project covers:

- Web scraping and preparation of Indonesian news articles.
- Classification into five predefined news categories.
- Implementation of IndoBERT-based text classification.
- Comparison of one-stage and two-stage approaches.
- Evaluation of model performance using classification metrics.

The project focuses on the categories represented in the available dataset and does not cover every type of Indonesian news.

## ⚠️ Limitations

- **Dataset Coverage:** The dataset contains 1,090 articles from Detik and Antara, so it may not represent the full range of Indonesian sports news.
- **Category Constraints:** The model is designed for the five predefined categories in the dataset.
- **Generalization:** Performance on articles from other publishers, different periods, or unfamiliar topics may vary.
- **Classification Errors:** Ambiguous articles or articles discussing multiple leagues may be difficult to categorize correctly.
- **Evaluation Scope:** The reported metrics reflect the experimental setup in the notebook and do not guarantee the same performance in real-world use.

## 📝 Disclaimer

This project was developed for academic and educational purposes as part of a text mining and natural language processing study.

Model predictions may contain errors and should not be considered definitive classifications. The original news content belongs to its respective publishers, and this project does not claim ownership of the original articles.

## 📁 Repository Structure

```text
sports-news-classification-indobert/
├── README.md
├── sports news web scraping.ipynb
├── sports news classification indobert.ipynb
└── dataset/
    └── dataset1.csv
```

## 🚀 How to Run

1. Clone or download this repository.
2. Open the notebooks in Jupyter Notebook or Google Colab.
3. Install the required Python libraries.
4. Run the web-scraping notebook to review the data collection process.
5. Load the prepared dataset in the classification notebook.
6. Execute the model training and evaluation cells.
7. Review the evaluation metrics and comparison visualizations.

## 👩‍💻 Author
*Amanda Sugito*

Deep Learning academic project at BINUS University.

## 🔗 Connect with Me
•⁠  ⁠LinkedIn: Amanda Sugito | www.linkedin.com/in/amanda-sugito
•⁠  ⁠GitHub: amandasugito | https://github.com/amandasugito

