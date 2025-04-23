# 😂 Analysis of Large Reddit Jokes Corpora  
**"We let 1 million Reddit jokes train our models. Our models are now hilarious. (Sometimes.)"**

---

## 🎯 Project Overview

Ever wondered what 1 million Reddit jokes can teach us about humor? We did too.  
This project explores **clustering**, **classifying**, and even **predicting funniness** of jokes using the r/Jokes dataset — a goldmine of groan-worthy puns, questionable dad jokes, and comedy gold.

We used everything from **KMeans** to **BERT** to **LSTM regressors**, because humor deserves serious models.  
The result? A system that can group jokes, rate them, and help machines appreciate that *"ether/oar"* is actually a pun.

---

## 📦 Dataset

- 📍 Source: [r/Jokes on Kaggle (1M Reddit jokes)](https://www.kaggle.com/datasets/priyamchoksi/1-million-reddit-jokes-rjokes)
- 🔢 After cleaning: ~570,000 usable jokes
- 📊 Fields: `title`, `selftext`, `score`, `timestamp`, etc.
- 🚫 Removed: `[deleted]`, `[removed]`, 350+ word essays that definitely weren’t jokes

---

## 🔍 Research Questions

1. Can we categorize jokes by **style/topic**?
2. Can we build a model to **predict funniness** (Reddit score)?
3. Can AI *actually understand* jokes?  
> (Answer: It tries. God bless it.)

---

## 🧹 Preprocessing

- Removed non-jokes and long spammy posts  
- Expanded contractions, removed stopwords and special characters  
- Lowercased everything (even the sarcasm)  
- Vectorized text with **TF-IDF**, **GloVe**, and **MiniLM Sentence Transformers**

---

## 🧪 Models Tried

### 🔹 Baseline Models:
- **Bag of Words + Linear Regression**: MSE = 😂  
- **TF-IDF + Linear Regression**: Slightly less 😂  
> TL;DR: Traditional models couldn't keep up with the punchlines.

### 🔹 Humor Clustering:
- Used **MiniLM embeddings + KMeans**
- Optimal clusters: **5** (thanks Elbow Method!)
- BERT classifier trained to assign jokes to clusters
- Achieved ~88.1% classification accuracy

### 🔹 Funniness Score Prediction:
- **LSTM + GloVe + Regression**
- Z-score normalized Reddit scores
- Trained with PyTorch on padded joke sequences (max length = 250)
- Best training loss: **0.1583** — not bad for trying to quantify *funny*

---

## 🔍 Example Jokes in the Dataset

> *"How do you drown a hipster? Throw him in the mainstream."* (Score: 531)  
> *"It was an ether/oar situation."* (Score: 330)  
> *"A man walks into a bar... ow."* (Unknown score, 10/10 in spirit.)

---

## 📊 Clustering Results

Each cluster had its own comedic vibe:

| Cluster | Theme |
|--------|----------------------------|
| 1      | Friends, dogs, casual gags |
| 2      | Time, old age, life jokes  |
| 3      | Relationships (wives, girlfriends... yikes) |
| 4      | Social, broad punchlines   |
| 5      | Observational and situational humor |

---

## 📈 Visuals

- Word clouds by year (election season = political memes)
- Subreddit activity growth (peaked around 2017-2019)
- Loss trends across LSTM training (sadly not as flat as some jokes)

---

## 🧠 Key Learnings

- Humor is **subjective**, but patterns exist
- BERT and LSTM work better than BoW when trying to understand punchlines
- Some jokes never get old — others just never should’ve been written
- AI *can* be funny... statistically

---

## 📂 Source Code & Report

> Full code & report available in [📁 this Google Drive folder (Stony Brook login)](https://drive.google.com/drive/folders/1Eqx01wkQf5qaX1qhmbJpCzlWnEp2tbI_?usp=sharing)

---

## 👨‍💻 Authors

**Krish Makadia** and Team  
📫 krishvimalkuma.makadia@stonybrook.edu  
📫 omkar.jahagirdar@stonybrook.edu

---

## 📄 License

MIT License.  
Feel free to remix these jokes, but don't blame us if the AI bombs at open mic night.

---

> ⭐ If this README made you smile, give the repo a star. Our models feed on attention. And maybe dad jokes.
