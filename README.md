# 🏴 Wakanda Forever Twitter Analysis Project  

## 📌 Overview  
This project explores the **global reaction on X (formerly Twitter)** to the passing of **Chadwick Boseman**, the actor who immortalized **Black Panther**. His death deeply impacted millions, and the tweet announcing his passing became the **most-liked tweet in X’s history** with over **6.5 million likes**.  

This analysis examines the **sentiment trends, influence propagation, and community structures** surrounding *Black Panther: Wakanda Forever* using **network science and sentiment analysis** techniques.  

---

## 🔹 Methodology  

### **1️⃣ Data Collection**  
📌 **Scraped tweets** related to:  
   - `"Wakanda Forever"`, `"Black Panther"`, and `"Chadwick Boseman"`  
   - Using **Twikit** for data extraction  
📌 **Collected Features**:  
   - Tweet text, usernames, retweets, likes, and engagement metrics  
📌 **Stored in CSV files** for preprocessing  

### **2️⃣ Data Preprocessing**  
✅ Removed **spam, duplicates, and bot-generated content**  
✅ **Standardized text** (lowercase, removed special characters)  
✅ Grouped tweets into **communities based on hashtags, mentions, and user interactions**  

### **3️⃣ Sentiment Analysis**  
📊 Used **VADER** to classify tweets as **positive, neutral, or negative**  
📊 Incorporated sentiment scores for **deeper trend analysis**  

### **4️⃣ Network Construction & Community Detection**  
📡 Built a **directed network graph** where:  
   - **Nodes** = Twitter users  
   - **Edges** = Interactions (mentions, retweets, replies)  
🔗 Applied **Louvain algorithm** to detect **key communities**  
📊 Identified **influential users** using **degree and betweenness centrality**  

### **5️⃣ Influence Analysis**  
📌 Tracked **how influence propagates** across users  
📌 Measured **influence decay over multiple hops**  
📌 Identified **top influencers** driving engagement  

### **6️⃣ Data Visualization**  
📊 Created compelling **network & sentiment visualizations**, including:  
- **Top 20 Influential Communities**  
- **Influence Decay Over Hops**  
- **Network Community Graph**  

---

## 📂 Folder Structure  
```bash
ChadwickBosemanTributeAnalysis/
├── notebooks/                 # Jupyter Notebooks for analysis
│   ├── 1_data_collection.ipynb
│   ├── 2_data_preprocessing.ipynb
│   ├── 3_sentiment_analysis.ipynb
│   ├── 4_network_analysis.ipynb
│   ├── 5_influence_propagation_analysis.ipynb
│   ├── 6_final_visualizations.ipynb
├── data/                      # Processed datasets
│   ├── cleaned_data.csv
│   ├── community_analysis.csv
│   ├── influence_decay_results.csv
├── scripts/                   # Python scripts for processing & visualization
│   ├── __init__.py            # Keeps this file for modular imports
│   ├── main.py                # Main execution script
│   ├── plot_community_influence.py
│   ├── plot_influence_decay.py
│   ├── plot_network_diagram.py
├── outputs/                   # Generated visualizations
│   ├── community_influence_plot.png
│   ├── influence_decay_plot.png
│   ├── network_diagram.png
├── docs/                      # Documentation folder (Optional, to keep things organized)
│   ├── RUNNING_INSTRUCTIONS.md # Guide on running the analysis
│   ├── KEY_FINDINGS.md         # Summary of key findings and insights
├── README.md                  # Main project documentation
└── .gitignore                  # Prevents tracking unnecessary files

