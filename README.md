# ⚽ Sports News Classification Using IndoBERT — Text Mining

## 📌 Project Overview

This project is a Text Mining and Natural Language Processing (NLP) project focused on classifying Indonesian sports news articles using IndoBERT.

The project compares one-stage and two-stage classification approaches to categorize news articles into football league categories and non-football news.

## 🎯 Project Objectives

- Collect Indonesian sports news articles from online news sources.
- Prepare a labeled dataset for text classification.
- Implement IndoBERT for Indonesian news categorization.
- Compare one-stage and two-stage classification approaches.
- Evaluate model performance using accuracy, precision, recall, and F1-score.

## 📂 Dataset

The dataset contains 1,090 news articles from Detik and Antara.

| Category | Number of Articles |
|---|---:|
| Non Sepak Bola | 376 |
| Liga Inggris | 200 |
| Liga Indonesia | 175 |
| Liga Italia | 172 |
| Liga Spanyol | 167 |
| **Total** | **1,090** |

The dataset contains three columns:

- `text` — News article text.
- `media` — Source of the article.
- `label` — Assigned news category.

## 🧠 Classification Approaches

### 1️⃣ One-Stage Classification

Classifies each news article directly into one of five categories:

- Liga Inggris
- Liga Italia
- Liga Indonesia
- Liga Spanyol
- Non Sepak Bola

### 2️⃣ Two-Stage Classification

Uses two sequential classification stages:

- **Stage 1:** Classifies articles as football or non-football news.
- **Stage 2:** Classifies football articles into four league categories.

## ⚙️ Features

- Web scraping for news data collection.
- Dataset preparation and label organization.
- Indonesian text classification using IndoBERT.
- Stratified training, validation, and testing data split.
- One-stage and two-stage model implementation.
- Model evaluation using accuracy, precision, recall, and F1-score.
- Performance comparison between classification approaches.

## 🛠️ Technologies Used

- Python
- Pandas and NumPy
- Requests
- BeautifulSoup
- Hugging Face Transformers
- IndoBERT (`indobenchmark/indobert-base-p1`)
- PyTorch
- Scikit-learn
- Matplotlib and Seaborn

## 📊 Model Evaluation

The classification notebook reports the following test results for the two-stage approach:

| Classification Stage | Accuracy | F1-score |
|---|---:|---:|
| Stage 1: Football vs. Non-Football | 98.80% | 98.80% |
| Stage 2: Football League Classification | 93.58% | 93.56% |

The one-stage approach is also evaluated and compared in the notebook. Its final reported metrics should be verified against the evaluation outputs before being presented as definitive results.

## 📂 Project Structure

```text
sports-news-classification-indobert/
├── README.md
├── sports-news-web-scraping.ipynb
├── sports-news-classification-indobert.ipynb
└── dataset/
    └── sports_news_dataset.csv
```

## 🚀 How to Run

1. Clone or download this repository.
2. Open the notebooks using Jupyter Notebook or Google Colab.
3. Install the required Python libraries.
4. Run the web-scraping notebook to review the data collection process.
5. Load the prepared dataset in the classification notebook.
6. Execute the classification and evaluation cells.
7. Review the model metrics and comparison visualizations.

## 👩‍💻 Author
**Amanda Sugito**

Text Mining academic project at BINUS University.

## 🔗 Connect with Me
- LinkedIn: Amanda Sugito | www.linkedin.com/in/amanda-sugito
- GitHub: amandasugito | https://github.com/amandasugito

## ⚠️ Disclaimer

This project was developed for academic and educational purposes as part of a Text Mining study.

The model's predictions may contain errors and should not be considered definitive news classifications. The original news content belongs to its respective publishers, and this project does not claim ownership of the original articles.
