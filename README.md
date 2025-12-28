# 🎥 MyAnimeList — Top Anime Analysis (Python)

This project collects, cleans, and analyzes data from the **MyAnimeList (MAL) Top Anime rankings** using the official public API.  
The goal is to explore trends such as genre frequency, demographic distribution, and score patterns among the highest-rated anime.

> Built mainly as a learning project — APIs, data cleaning, pandas, and visualization.

---

## ✨ Features

- Fetches data from the [official MyAnimeList API](https://myanimelist.net/clubs.php?cid=13727)  
- Collects the **Top 500 ranked anime**  
- Saves results to CSV for reuse and sharing  
- Cleans and structures the data with pandas  
- Generates visual analysis:

  - Genre distribution  
  - Demographic distribution  
  - Average score by genre  
  - Basic descriptive insights

- Visualizations using matplotlib

---


### Columns

| Column | Description |
|-------|-------------|
| `rank` | Global ranking on MAL |
| `score` | Average user rating |
| `popularity` | Popularity index |
| `title` | Anime title |
| `type` | TV, Movie, OVA, etc. |
| `source` | Manga, Novel, Original, etc. |
| `genres` | Comma-separated genre list |
| `demographic` | Target demographic (when available) |
| `rating` | Age rating |

> Rankings change over time — this dataset is a snapshot.

---

## 🛠 Tech Stack

- Python  
- Requests  
- Pandas  
- Matplotlib  
- Jupyter Notebook

---

## 🔐 API Access

This project uses the **MyAnimeList API**.  
You must provide your own credentials.

Create a `.env` file (or set environment variables):
```
CLIENT_ID=your_client_id_here
CLIENT_SECRET=your_client_secret_here
```

Keys are loaded securely — nothing is hard-coded.

---

## ▶️ How to Run

Clone the repo:

```bash
git clone https://github.com/joaoeduardogomes/anime-data-analysis.git
cd anime-data-analysis
```
Create a virtual environment:
```bash
python -m venv .venv
source .venv/bin/activate   # Linux/Mac
# or
.\.venv\Scripts\activate    # Windows
```
Install dependencies:
```
pip install -r requirements.txt
```
Open the Jupyer notebook then run it to:
1. Fetch anime data (get_anime_data)
2. Save it to CSV (get_anime_data)
3. Explore results (analyze_anime_data)
4. Generate visualizations (analyze_anime_data)

## 📊 Example Insights
* Which genres appear most often in top-ranked anime
* Which demographics dominate the rankings
* How scores vary across genres (with global mean reference)

## ⚠️ Notes
* Data comes directly from the [MAL API](https://myanimelist.net/clubs.php?cid=13727)
* Some fields may be missing depending on the entry
* API rankings evolve over time
