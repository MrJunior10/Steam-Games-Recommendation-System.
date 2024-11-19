
# 🚀 Steam Games Recommendation System

Welcome to the **Steam Games Recommendation System**, a hybrid recommendation engine designed to provide highly personalized and diverse game suggestions for users on the Steam platform. By combining **content-based filtering**, **collaborative filtering**, and **popularity metrics**, this system offers tailored recommendations that align with individual preferences while staying relevant to market trends.

---

## 📖 Overview

With thousands of games available on Steam, finding the perfect game can be overwhelming. Our recommendation system addresses this challenge by leveraging multiple data sources and advanced machine learning techniques to deliver accurate and meaningful suggestions.

### Key Features:
- **Hybrid Recommendation Approach**: Integrates content-based and collaborative filtering with popularity metrics for robust suggestions.
- **Personalization**: Tailors recommendations to individual user preferences using advanced sentiment analysis and clustering.
- **Diversity**: Highlights trending games while ensuring a variety of genres and playstyles are recommended.

---

## 🗂️ Datasets Used

1. **Game Descriptions**:
   - Contains data for over 5,000 games, including genres, descriptions, player ratings, and system requirements.
   - Powers content-based filtering by analyzing game attributes.

2. **Player Reviews**:
   - Includes 100,000+ reviews with feedback, playtime, recommendations, and sentiments.
   - Enables collaborative filtering through user interaction data.

3. **Game Rankings**:
   - Ranks games based on sales, revenue, and reviews.
   - Used to compute popularity scores and incorporate trending games.

---

## ⚙️ Methodology

### **1. Content-Based Filtering**
- **Vectorization**: Game descriptions are transformed into vector representations using **Doc2Vec**.
- **Similarity Calculation**: Cosine similarity between game vectors identifies similar games:
  \[
  	ext{Similarity Score} = \cos(ec{v}_{	ext{game1}}, ec{v}_{	ext{game2}})
  \]

### **2. Collaborative Filtering**
- **Matrix Decomposition**: User-game interaction data is decomposed using **Singular Value Decomposition (SVD)**:
  \[
  R pprox U \Sigma V^T
  \]
- **Preference Prediction**: Missing ratings are predicted by reconstructing the interaction matrix.

### **3. Popularity Metrics**
- Combines **genre rankings**, **review counts**, and **cluster trends** (via K-Means) to compute a weighted popularity score.

### **4. Hybrid Scoring Mechanism**
- Combines content-based, collaborative, and popularity scores into a final recommendation score:
  \[
  	ext{Hybrid Score} = w_c \cdot 	ext{Content Score} + w_{cf} \cdot 	ext{Collaborative Score} + w_p \cdot 	ext{Popularity Score}
  \]

---

## 🔍 Key Results

- **Personalized Recommendations**: Tailored suggestions based on individual preferences and behavior.
- **Diverse Outputs**: Incorporates both user preferences and trending games for a balanced recommendation.
- **Example**:
  For a user interested in *Dota 2*, recommendations include:
  - **Golf Peaks** (Score: 0.6053)
  - **Apex Legends™** (Score: 0.5927)
  - **MARVEL SNAP** (Score: 0.5384)

---

## 📈 Future Directions

- **Real-Time Updates**: Integrate live data processing to adapt to evolving preferences and market trends.  
- **Enhanced Sentiment Analysis**: Expand sentiment analysis using gameplay metrics to refine recommendations.  
- **Social Integration**: Leverage multiplayer activity and friends’ preferences to create community-driven recommendations.  

---

## 🤝 Acknowledgments

- Steam and its extensive dataset for enabling this project.
- Open-source libraries and tools that made this implementation possible.

---

Feel free to reach out with feedback or questions. Happy gaming! 🎮
