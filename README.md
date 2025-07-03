# 🎧 Moodify – Music Mood Predictor using SVM

**Moodify** is a machine learning project that predicts the emotional mood of a song — Happy, Sad, Energetic, or Calm — using audio features extracted from the Spotify Audio Features Dataset. It uses a Support Vector Machine (SVM) classifier trained on features like valence, energy, danceability, tempo, and loudness to map music into moods.

---

## 🔮 Features

- 🎵 Classifies songs into four moods: Happy, Sad, Energetic, Calm
- 🤖 Uses SVM classifier with RBF kernel
- 🧠 Trained on real-world audio data from Spotify
- 🎛️ Clean and intuitive Streamlit interface (optional)
- 💽 Saves trained model and scaler for reuse

---

## 📁 Project Structure

moodify/
├── data/ # Raw dataset (Spotify)
├── notebooks/ # Training notebooks
│ └── svm_music_mood_classifier.ipynb
├── models/ # Saved SVM model and scaler
│ ├── svm_model.pkl
│ └── scaler.pkl
├── app/ # Streamlit app
│ └── streamlit_app.py
├── README.md
└── requirements.txt

---

## 📊 Dataset

- **Source:** [Spotify Audio Features Dataset](https://www.kaggle.com/datasets/geomack/spotifyclassification)
- **Attributes used:** `valence`, `energy`, `danceability`, `tempo`, `loudness`
- **Mood Mapping Logic:**

| Mood       | Valence | Energy |
|------------|---------|--------|
| Happy      | High    | High   |
| Sad        | Low     | Low    |
| Energetic  | Low     | High   |
| Calm       | High    | Low    |

---

## 🧪 Model

- **Algorithm:** Support Vector Machine (SVM)
- **Kernel:** Radial Basis Function (RBF)
- **Scaler:** StandardScaler for feature normalization
- **Evaluation Metrics:** Accuracy, F1-score, Confusion Matrix

---

## 🚀 How to Run

1. Clone the repo:
    ```bash
    git clone https://github.com/your-username/moodify.git
    cd moodify
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the notebook to train the model:
    ```bash
    jupyter notebook notebooks/svm_music_mood_classifier.ipynb
    ```

4. Launch the Streamlit app:
    ```bash
    streamlit run app/streamlit_app.py
    ```

---


## 📌 Future Improvements

- Allow MP3 upload and real-time audio feature extraction using `librosa`
- Add more moods (e.g., Romantic, Angry)
- Use advanced models (e.g., neural networks) for comparison
