# 🧹 Data Preprocessing with LLM (Yelp Reviews Dataset)

This project demonstrates how Large Language Models (LLMs) can be used for **text preprocessing** to improve text quality before training downstream NLP models such as sentiment classifiers.

We compare:
- 🧼 **Traditional text cleaning** (regex removal, lowercasing, punctuation cleaning)
- 🤖 **LLM-based cleaning** using *FLAN-T5* to rewrite reviews into cleaner, more professional English

---

## 📂 Dataset

📌 **Yelp Polarity Dataset** (Hugging Face)

- Binary labels:  
  `0 = Negative`, `1 = Positive`
- Input column: `text`

We used the first **300 samples** for efficient LLM processing.

---

## ⚙️ Tools & Libraries

- Hugging Face `datasets`
- Hugging Face Transformers (FLAN-T5 model)
- Python `re` (regex)
- `matplotlib` for visualization

---

## 🔍 What Preprocessing Was Done?

| Stage | Description |
|------|-------------|
| Traditional Cleaning | Lowercasing, removing URLs, punctuation & extra spaces |
| LLM Cleaning | Grammar correction, removing informal language, improving readability |
| Corpus Analysis | Vocabulary size and avg. text length comparison |

---

## 📊 Results

| Metric | Raw Text | Cleaned Text | Improvement |
|--------|----------|--------------|-------------|
| **Vocabulary Size** | 4350 | 2840 | 🔻 −35% |
| **Avg. Length** | 148.06 | 70.98 | 🔻 −52% |

✔ Cleaner and more consistent text  
✔ More efficient for downstream ML models  
✔ Better readability and grammar

Example chart from the project:

> *Corpus Statistics Comparison before vs after cleaning*

---

## 📝 Observations

- LLM significantly reduces noisy and redundant vocabulary
- More formal and professional text generation improves clarity
- Very long sentences get truncated due to model limits (512 tokens)
- Already-clean text undergoes minimal rewriting

> Conclusion: **LLM-based preprocessing improves dataset quality and efficiency, especially for noisy datasets.**

---


## 📈 Visualization

A comparison bar chart demonstrates:

- Drop in vocabulary size
- Shorter and cleaner review text

This confirms that preprocessing **positively impacts dataset quality**.

---


## 🛠 How to Run

1. Install the required Python libraries:  
   pip install transformers datasets sentencepiece matplotlib

2. Open and execute the notebook file:  
   DataPreprocessing.ipynb

3. After running all cells, the cleaned dataset will be saved as:  
   yelp_cleaned_llm.csv

---

👩‍💻 Author: Keshav Kathuria
