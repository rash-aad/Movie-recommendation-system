Download files from here : https://drive.google.com/drive/folders/1A-pTWuIiK9_Z8Q2wQ4r4sN-HLgx34fyL?usp=sharing
# 🎬 Movie Recommendation System

This project is a **content-based movie recommender system** built using Python, Streamlit, and machine learning. It suggests movies similar to the one you like based on metadata such as cast, crew, genres, and keywords. The recommender is powered by data from the TMDB 5000 Movie Dataset.

---

## 🚀 Features

- Recommend top 5 similar movies based on selected input
- Web app built with Streamlit for an intuitive UI
- Utilizes cosine similarity on processed metadata
- Fast and responsive thanks to precomputed similarity matrix

---

## 🧠 How It Works

1. **Dataset**: Uses `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` for rich movie metadata.
2. **Preprocessing**: Cleans and combines relevant fields like genres, overview, cast, and crew into a "tags" feature.
3. **Vectorization**: Applies `CountVectorizer` to create a word-frequency matrix of movie tags.
4. **Similarity Calculation**: Computes cosine similarity across all movie vectors to identify closeness.
5. **Web App**: Streamlit interface loads pre-trained model files (`movies.pkl`, `movie_dict.pkl`, `similarity.pkl`) to instantly deliver recommendations.

---

## 📂 Project Structure

```
ml_project/
├── movie_recommend.ipynb        # Jupyter notebook for building and testing model
├── tmdb_5000_movies.csv         # TMDB movie metadata
├── tmdb_5000_credits.csv        # TMDB credits metadata
├── movie_recomend/
│   ├── app.py                   # Streamlit app entry point
│   ├── movies.pkl               # Movie data
│   ├── movie_dict.pkl           # Dictionary of movie info
│   ├── similarity.pkl           # Precomputed similarity matrix
│   └── .idea/                   # IDE configuration files
```

---

## 🛠 Installation

1. **Clone the Repository**
   ```bash
   git clone https://github.com/rash-aad/Movie_recommendation_system.git
   cd Movie_recommendation_system/ml_project/movie_recomend
   ```

2. **Create a Virtual Environment (Optional but Recommended)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install Requirements**
   ```bash
   pip install -r requirements.txt
   ```

---

## ▶️ Running the App

From inside the `movie_recomend` directory, run:

```bash
streamlit run app.py
```

Then open the link provided by Streamlit in your browser (usually http://localhost:8501).

---

## 📊 Data Source

- [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

---

## 📌 Note

- This is a **content-based** recommender, not collaborative.
- Pretrained `.pkl` files are included for instant use — no need to retrain.

---

## 🤝 Contributions

Feel free to fork this repo and make improvements! Pull requests are welcome.

---

## 📧 Contact

Created by **Rashaad N Mohammed**  
For any inquiries, reach out at: rashaadnmohammed@gmail.com
