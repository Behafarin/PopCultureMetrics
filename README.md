# **Pop Culture Metrics**  
**Exploring Media Influence on Music Popularity**  

### **Overview**  
**Pop Culture Metrics** bridges the gap between media sentiment and music streaming success. By combining scraped music news from Rolling Stone with artist data from Spotify, this project produces a rich dataset for analyzing correlations between media coverage, sentiment, and streaming popularity.

---

### **Features**
- **News Data**:  
  - Scraped Rolling Stone articles with artist mentions extracted via Named Entity Recognition (NER).  
  - Sentiment analysis to evaluate article tone.  

- **Spotify Data**:  
  - Artist popularity scores, follower counts, and genres fetched using the Spotify API.

- **Preprocessing**:  
  - Extensive cleaning and normalization to align datasets and resolve inconsistencies in artist names.

- **Output**:  
  - A unified, structured dataset (`final_artist_statistics.csv`) ready for analysis, featuring sentiment scores and streaming metrics.

---

## Project Structure
### Files and Directories:
- **Jupyter Notebooks**:
  1. `News API.ipynb`:
     - Initial exploration with News API (abandoned due to rate limitations).
  2. `News Data Scraping.ipynb`:
     - Scrapes Rolling Stone articles for titles, summaries, and links.
  3. `Extract Artists from News.ipynb`:
     - Applies Named Entity Recognition (NER) to extract artist mentions from news data.
  4. `Spotify API Call.ipynb`:
     - Fetches artist metadata (popularity scores, followers, genres) from Spotify API.
  5. `Preprocessing And Analysis.ipynb`:
     - Preprocesses news and Spotify data, merges datasets, performs sentiment analysis, and produces the final dataset.

- **Output Data**:
  - `rollingstone_news.csv`: Scraped Rolling Stone articles.
  - `spotify_artist_data.csv`: Artist metadata from Spotify.
  - `final_artist_statistics.csv`: The merged and preprocessed dataset.

---

## Dataset Preview
Here’s a snapshot of the dataset (final artist statistics):

![Dataset Preview](https://raw.githubusercontent.com/Behafarin/PopCultureMetrics/main/data/dataset_preview.png)

---

### **Steps to Reproduce**
1. Clone the repository:  
   ```bash
   git clone https://github.com/yourusername/pop-culture-metrics.git

2. Install dependencies:  
   ```bash
   pip install -r requirements.txt

3. Run the notebooks in order:
    - Start with News Data Scraping.ipynb and finish with Preprocessing And Analysis.ipynb.

6. Final dataset will be saved as final_artist_statistics.csv.

## Challenges and Limitations

### Challenges:
1. **News API Restrictions**:
   - Limited to 100 requests/day, forcing a shift to scraping Rolling Stone articles instead.
2. **Spotify API Rate Limits**:
   - Frequent token expirations required automation for token refreshing and batching requests.
3. **Data Variability**:
   - Artist names in news data were inconsistent, requiring extensive preprocessing for alignment.

### Limitations:
1. **Language Scope**:
   - Data is limited to English-language news, which may exclude global perspectives.
2. **Ambiguity in NER**:
   - Extracting artist names occasionally included false positives, which were filtered manually.
3. **Snapshot Nature**:
   - The dataset reflects a single period of data collection and does not account for changes over time.

---

## Potential Applications
- **Music Industry**:
  - Analyze the relationship between media coverage and streaming popularity.
  - Identify trends in popular genres or artists receiving media attention.
- **Research**:
  - Study the influence of media sentiment on consumer listening behavior.
- **Data Science**:
  - Develop predictive models to forecast artist success based on media trends.

---

## Access Rights
- **News Data**:
  - Scraped from publicly accessible Rolling Stone articles, with usage subject to Rolling Stone’s terms of service.
- **Spotify Data**:
  - Collected using Spotify's API, adhering to Spotify’s developer terms.

---

## Contact Information
For questions or feedback, feel free to reach out:
- **Behafarin Emam**: be379@drexel.edu

---


