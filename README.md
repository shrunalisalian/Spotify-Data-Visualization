# 🎵 **Spotify Data Visualization: Trends, Features & Time-Series Analysis**  
**Author:** Shrunali Salian & Team  
**Skills:** R, Data Visualization, ggplot2, Time-Series Analysis, Correlation Analysis  

---

## 🚀 **Project Overview**  
This project analyzes **Spotify's extensive music dataset** to uncover trends in **track popularity, feature relationships, and user preferences over time**.  

📌 **Project Highlights:**  
✅ **Trend Analysis** – Insights on track uploads, COVID impact & popularity factors  
✅ **Feature Analysis** – Understanding relationships between song characteristics  
✅ **Time-Series Analysis** – Examining trends in genre, artist popularity & explicit content  

🔗 **Dataset:** [Kaggle - Spotify Dataset (1921-2020)](https://www.kaggle.com/datasets/yamaerenay/spotify-dataset-19212020-600k-tracks)  
📜 **Medium Article (15,000+ Views!):** [Spotify Data Visualization](https://medium.com/@shrunalisalian97/spotify-data-visualization-4c878c8114e)  

---

## 🎯 **Key Objectives**  
✔ **Explore how Spotify has evolved over time**  
✔ **Analyze key drivers of track popularity**  
✔ **Understand song feature relationships & correlations**  
✔ **Examine how music preferences change across decades**  

---

## 📊 **Trend Analysis**  

### **1️⃣ Spotify’s Performance Over the Years**  
📈 **Tracks uploaded per year:**  
- **Consistent increase** in tracks uploaded  
- 📌 **2013 surge** – Rising **CD prices** + **Streaming platforms gaining traction**  
- 📌 **2017 drop** – **Spotify’s global expansion costs skyrocketed** before IPO  

✅ **Visualization:** Number of tracks uploaded per year  

```r
ggplot(spotify_data, aes(x = year, y = track_count)) +
  geom_line() +
  labs(title = "Spotify Track Uploads Over Time")
```

---

### **2️⃣ COVID Hypothesis: Did Artists Release More Emotional Songs?**  
🎶 **Hypothesis:** Artists may release more happy/sad songs during COVID.  
❌ **Result:** No major change observed in song valence (mood).  

✅ **Visualization:** Emotional content trends before & during COVID  

```r
ggplot(spotify_data, aes(x = year, y = valence, color = covid_period)) +
  geom_boxplot() +
  labs(title = "Emotional Content Trends During COVID")
```

---

### **3️⃣ What Determines Track Popularity on Spotify?**  
⭐ **Finding:** **Track popularity is driven by the artist’s follower count**, NOT track characteristics.  
📌 **Artist popularity is the strongest predictor** of a song’s success.  

✅ **Visualization:** Correlation between track popularity & artist followers  

```r
ggplot(spotify_data, aes(x = artist_followers, y = track_popularity)) +
  geom_point(alpha = 0.5) +
  labs(title = "Artist Followers vs Track Popularity")
```

---

## 🎵 **Feature Analysis: Understanding Song Characteristics**  

### **1️⃣ How are Features of a Song Related?**  
📌 **Strong Correlations Found Between:**  
- **Valence & Energy**  
- **Valence & Danceability**  
- **Loudness & Energy**  

✅ **Visualization:** Heatmap of song feature correlations  

```r
library(ggcorrplot)
corr_matrix <- cor(spotify_data[, c("valence", "energy", "danceability", "loudness")])
ggcorrplot(corr_matrix, method="circle")
```

---

### **2️⃣ Loudness vs Energy: Are Louder Songs More Energetic?**  
📌 **Yes!** Loud tracks tend to have **higher energy levels**.  

✅ **Visualization:** Scatterplot of **Loudness vs Energy**  

```r
ggplot(spotify_data, aes(x = loudness, y = energy)) +
  geom_point(alpha = 0.5) +
  labs(title = "Loudness vs Energy in Spotify Tracks")
```

---

### **3️⃣ Word Cloud: Most Popular Justin Bieber Tracks**  
📌 **Finding:** "Hold On" & "Anyone" are the most common song titles.  

✅ **Visualization:** Word Cloud of Justin Bieber’s popular tracks  

```r
library(wordcloud)
wordcloud(spotify_data$track_name, max.words = 50, colors = brewer.pal(8, "Dark2"))
```

---

## ⏳ **Time-Series Analysis: How Music Preferences Change Over Time**  

### **1️⃣ Do Users Prefer Newer Artists Over Older Ones?**  
📌 **Finding:** **Recent artists have higher popularity** than early-decade artists.  
📌 **Possible reasons:** **Music industry evolution, genre shifts, & better production technology.**  

✅ **Visualization:** Artist popularity by year  

```r
ggplot(spotify_data, aes(x = artist_debut_year, y = artist_popularity)) +
  geom_line() +
  labs(title = "Popularity of Artists by Debut Year")
```

---

### **2️⃣ Genre Preferences: Are Old Genres Still Popular?**  
📌 **Finding:** **Genres from the 2000s remain the most popular today.**  
📌 **Why?** Older genres are **re-adapted** by modern artists to stay relevant.  

✅ **Visualization:** Popularity of different genres by decade  

```r
ggplot(spotify_data, aes(x = genre_decade, y = genre_popularity)) +
  geom_bar(stat = "identity") +
  labs(title = "Genre Popularity Across Decades")
```

---

### **3️⃣ Explicit Content in Music Over Time**  
📌 **Finding:** The **cultural attitude toward explicit music has shifted**, with **2000s music featuring the most explicit lyrics.**  

✅ **Visualization:** Proportion of explicit tracks over decades  

```r
ggplot(spotify_data, aes(x = decade, y = explicit_ratio)) +
  geom_line() +
  labs(title = "Increase in Explicit Content Over Time")
```

---

## 🔮 **Future Enhancements**  
🔹 **Sentiment Analysis on Lyrics** – Are sad songs more popular?  
🔹 **Machine Learning Model** – Predicting song popularity based on features  
🔹 **Comparison with Competitors (Apple Music, YouTube Music, etc.)**  

---

## 🎯 **Why This Project Stands Out for Data Science & AI Roles**  
✔ **Uses Real-World Music Data from Spotify** – Popular dataset with strong industry relevance  
✔ **Applies R & ggplot2 for Advanced Data Visualization**  
✔ **Performs Trend Analysis, Feature Relationships & Time-Series Analysis**  
✔ **Explores the Evolution of Music Preferences & Popularity Factors**  

---

## 🛠 **How to Run This Project**  
1️⃣ Clone the repo:  
   ```bash
   git clone https://github.com/shrunalisalian/spotify-data-visualization.git
   ```
2️⃣ Install dependencies:  
   ```r
   install.packages(c("ggplot2", "dplyr", "wordcloud", "ggcorrplot"))
   ```
3️⃣ Run the RMarkdown file:  
   ```r
   rmarkdown::render("Hackathon.Rmd")
   ```

---

## 📌 **Connect with Me**  
- **LinkedIn:** [Shrunali Salian](https://www.linkedin.com/in/shrunali-salian/)  
- **Portfolio:** [Your Portfolio Link](#)  
- **Email:** [Your Email](#)  

---

### 🚀 **Final Thoughts**  
This project provides **deep insights into Spotify’s music trends, user behavior, and song characteristics**. It’s a **perfect addition to a data science portfolio**, demonstrating **data visualization, time-series analysis, and trend discovery**.  

🔥 **Drop a ⭐ on GitHub if you found this useful!**  

✅ **Would you like to extend this project with sentiment analysis on song lyrics?** 🚀  

### **Suggested Repo Name:**  
🔹 **spotify-data-visualization** – Clean, professional, and directly relevant! Let me know if you prefer something more creative. 🎵✨
