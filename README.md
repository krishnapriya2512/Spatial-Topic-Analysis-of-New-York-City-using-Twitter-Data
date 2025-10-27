## 🗽 NYC Twitter Urban Analytics — 2021
This project analyzes geo-tagged Twitter data from New York City to understand how public discourse and sentiment vary across space and time.  
Using Python-based spatial clustering (K-Means), topic modeling (LDA), and sentiment analysis, it identifies the dominant themes and emotional tone of online discussions across four city regions(Brooklyn & Staten Island Downtown Manhattan, Queens & Eastern Brooklyn, Uptown Manhattan & Bronx) and seasons (Winter, Spring, Summer, Fall).

### Key Features
- **Geo-spatial clustering:** Divides NYC into four clusters for localized analysis.  
- **Seasonal segmentation:** Compares discussion trends across Winter, Spring, Summer, and Fall.  
- **Topic modeling:** Extracts top discussion themes using Latent Dirichlet Allocation (LDA).  
- **Sentiment analysis:** Evaluates emotional polarity using predefined sentiment scores.  
- **Visual analytics:** Includes word clouds, heatmaps, and trend visualizations for cluster-wise insights.  

### Tools and Libraries
 - **Tools:** Python -3.12.0, VS Code (ipynb file)
 - **Libraries:** SQLite3, pandas, Spacy, string, NLTK, KMeans, CountVectorizer, Latent Dirichlet Allocation

### Data Collection
Geo-tagged tweets were collected from multiple SQLite databases covering December 2020 to November 2021. Each database contained tweet text, metadata (tweet ID, timestamp, language), geographic coordinates, and pre-computed sentiment scores (Positive, Negative, Compound) using the VADER model.

#### Data Preprocessing
Preprocessing steps were applied to enhance the quality and consistency of textual and spatial data before clustering and modeling. 
- **Convertion of Datatypes:** Converting geo-cordinates into required form.
- **Language filtering:** Only English tweets were retained to maintain linguistic uniformity.
- **Noise removal:** URLs, mentions, hashtags and special characters were removed using regular expressions.
- **Text normalization:** Tweets were lowercased, tokenized, and lemmatized using the SpaCy NLP library.
- ** Custom Stopword removal:** Non-informative words were excluded.
- **Geospatial filtering:** Tweets located outside NYC’s bounding box (latitude 40.47–40.92; longitude –74.25––73.70) were discarded.

### Spatial Clustering
Spatial clustering was conducted prior to seasonal classification to identify geographically distinct regions
of tweet activity. The K-Means algorithm was applied to the latitude and longitude features
(geo lat, geo lon) using scikit-learn. The optimal number of clusters (k = 4) was chosen
after examining the inertia curve and to correspond with the city’s main geographic zones. Figure

### 📈 Outcome
The analysis reveals distinct urban communication patterns:  
Downtown Manhattan shows the most positive and event-driven discourse,  
while Uptown Manhattan and the Bronx exhibit more negative sentiment tied to incidents and infrastructure.  
These insights demonstrate how social media can be used to understand urban behavior and sentiment across both space and season.

---
