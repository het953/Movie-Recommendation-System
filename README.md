# Movie Recommendation System 🎬

A Machine Learning-based recommendation engine that suggests movies similar to a user's selection. This project utilizes **Content-Based Filtering** to analyze movie features such as genre, plot, and keywords to find and recommend the most similar films.

## 📌 Overview
The goal of this project is to build a recommendation system that helps users discover new movies. Unlike collaborative filtering (which relies on user ratings), this system focuses on the properties of the movies themselves. If a user likes *The Dark Knight*, the system will recommend other Action/Crime/Thriller movies with similar themes.

## 📂 Dataset
The project uses the `Movies Recommendation.csv` dataset, which includes information such as:
- **Movie ID**
- **Movie Title**
- **Genre**
- **Release Date**
- **Rating**
- **Plot/Overview** (used for feature extraction)

## 🛠️ Tech Stack
- **Language:** Python 3.x
- **Environment:** Jupyter Notebook
- **Libraries:**
  - `pandas` (Data manipulation)
  - `numpy` (Numerical operations)
  - `scikit-learn` (TF-IDF Vectorization & Cosine Similarity)
  - `difflib` (String matching for movie titles)

## ⚙️ How It Works
1.  **Data Loading:** The `Movies Recommendation.csv` file is loaded into a Pandas DataFrame.
2.  **Feature Engineering:** Relevant text features (like Genres, Keywords, Taglines, Cast, and Director) are combined into a single "content" string for each movie.
3.  **Vectorization:** The text data is converted into numerical vectors using **TF-IDF (Term Frequency-Inverse Document Frequency)** or **CountVectorizer**.
4.  **Similarity Calculation:** **Cosine Similarity** is used to calculate the angle between movie vectors. A smaller angle implies higher similarity.
5.  **Recommendation:** When a user inputs a movie title, the system finds the closest vectors (movies) and returns the top suggestions.

## 🚀 How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/het953/Movie-Recommendation-System.git](https://github.com/het953/Movie-Recommendation-System.git)
    ```
2.  **Navigate to the project directory:**
    ```bash
    cd Movie-Recommendation-System
    ```
3.  **Install dependencies:**
    ```bash
    pip install pandas numpy scikit-learn
    ```
4.  **Run the Notebook:**
    Launch Jupyter Notebook or JupyterLab and open `Movie_Recommendation_System.ipynb` to execute the cells step-by-step.

## 📊 Example
**Input:** `Iron Man`
**Output:**
1. *Iron Man 2*
2. *Iron Man 3*
3. *Avengers: Age of Ultron*
4. *The Avengers*
5. *Captain America: Civil War*

## 🤝 Contributing
Contributions are welcome! If you have suggestions for improving the algorithm (e.g., adding collaborative filtering or a web interface), feel free to fork the repo and create a pull request.
