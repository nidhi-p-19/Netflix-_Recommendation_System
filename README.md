
# 🍿 Netflix Movie Recommendation System

Welcome to the **Netflix Recommendation System**, where machine learning meets movie magic 🎥✨.  
This project is a **Content-Based Filtering** model built to recommend movies similar to your favorite ones. Instead of relying on user ratings (Collaborative Filtering), this system reads the *content* — think genres, plots, keywords — and finds patterns that align with your movie preferences.

---

## 💡 What is a Recommendation System?

A recommendation system is like your digital movie buddy. It answers questions like:

- "You liked Inception? You’ll probably enjoy Interstellar."
- "Into crime thrillers with a tech twist? Here's more."

In Netflix, there are multiple types of recommendation engines:
- **Collaborative Filtering** (based on user behavior)
- **Content-Based Filtering** (based on movie metadata)
- **Hybrid Systems** (best of both)

This project focuses on **Content-Based Filtering**—great when user history is limited or unavailable.

---

## 🧠 Intuition Behind the Project

Imagine your friend says, "I love The Matrix!" — How would you recommend a movie?

You’d probably look for:
- Sci-fi elements
- A dystopian or futuristic theme
- Tech or AI concepts
- A cerebral or twisty plot

We’re replicating that same logic with data.

We:
1. **Extract metadata** about each movie (genre, keywords, plot summary).
2. **Convert text into numbers** using NLP tools (TF-IDF or CountVectorizer).
3. **Measure similarity** between movies using Cosine Similarity.
4. **Recommend** the top N most similar titles.

That’s exactly what this model does—at scale and with machine learning precision.

---

## 🧪 Tech Stack & Tools

| Component | Tool |
|----------|------|
| Language | Python 3 |
| Data Handling | Pandas, NumPy |
| NLP | Scikit-learn's CountVectorizer / TfidfVectorizer |
| Similarity Measure | Cosine Similarity |
| IDE | Jupyter Notebook |

---

## 🔍 Project Pipeline

### 1. **Data Loading**
We load a dataset containing movie titles, genres, descriptions, and more.

### 2. **Data Cleaning & Feature Selection**
We clean the dataset and select features we’ll use to generate similarity:
- Title
- Genre
- Overview
- Keywords

### 3. **Vectorization (Turning Text into Numbers)**
Using **CountVectorizer** or **TF-IDF**, we convert the text into a matrix of numbers that a machine can understand.

### 4. **Similarity Computation**
We now compute pairwise **cosine similarity** between all movie vectors to understand which ones are closest in meaning.

### 5. **Recommendation Function**
We build a simple function where, given a movie title, it:
- Finds its vector
- Computes similarity with every other movie
- Returns the top 10 most similar titles

---

## 🔥 Example Run

```python
recommend('Inception')
```

📽️ Output:
```
1. Interstellar
2. The Matrix
3. Shutter Island
4. The Prestige
5. Source Code
...
```

---

## 📁 Files in This Repo

| File | Description |
|------|-------------|
| `Netflix_Recommendation_System.ipynb` | The main Jupyter Notebook |
| `README.md` | This documentation file |
| `movies.csv` (optional) | The dataset used (you can include a link or mention source) |
| `requirements.txt` | List of Python packages needed to run the project |

---

## 📦 Installation & Usage

### 🔧 Requirements
```bash
pip install pandas numpy scikit-learn jupyter
```

### ▶️ Run the Project
```bash
jupyter notebook
# Open Netflix_Recommendation_System.ipynb
# Run all cells and call recommend("Your Movie Title")
```

---

## 🚀 Future Upgrades

- ✅ Add a **web interface** using Streamlit or Flask
- ✅ Use **TMDb API** to pull real-time posters and movie info
- ✅ Combine with **Collaborative Filtering** for hybrid recommendations
- ✅ Deploy on **Heroku or HuggingFace Spaces**

---

## 🤝 Contributing

Pull requests are welcome. Feel free to fork the repo, improve, and submit.

---

## 📝 License

This project is licensed under the MIT License — feel free to use, modify, and share.
