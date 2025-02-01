"# How to Run the Project" 


---
## **Wakanda Forever Twitter Analysis Project**  
This document provides a **detailed guide** on setting up, running, and troubleshooting the Twitter network analysis.

---

## **📌 1. Prerequisites**  

### ✅ **1.1 Install Python**  
Ensure you have **Python 3.8 or later** installed.

- **Check your version** by running:  
  ```bash
  python --version
  ```
  or (on some systems):
  ```bash
  python3 --version
  ```

- If Python is **not installed**, download it from:  
  🔗 [Python Official Website](https://www.python.org/downloads/)

---

### ✅ **1.2 Install Required Libraries**  
Before running the analysis, you must install dependencies.

1️⃣ **Navigate to the project directory**:
```bash
cd ChadwickBosemanTributeAnalysis
```

2️⃣ **Install the required Python libraries** using:
```bash
pip install -r requirements.txt
```

**Troubleshooting:**
- If you get **permission errors**, try:
  ```bash
  pip install --user -r requirements.txt
  ```
- If using **Mac/Linux**, you may need:
  ```bash
  sudo pip install -r requirements.txt
  ```

---

## **📌 2. Running the Analysis**  

### **Option 1: Run the Entire Pipeline Using `main.py` (Recommended)**
To execute all stages automatically, run:
```bash
python scripts/main.py
```

This script performs:
✅ **Data collection (if enabled)**  
✅ **Data preprocessing (cleaning, filtering, structuring tweets)**  
✅ **Sentiment analysis (classifying tweets as positive, neutral, or negative)**  
✅ **Network construction & community detection**  
✅ **Influence propagation analysis**  
✅ **Generating visualizations & saving results**  

📂 **Where Are the Outputs Stored?**
- **Processed Data** → `data/`
- **Visualizations** → `outputs/`
- **Network files** → `scripts/`

---

### **Option 2: Run Individual Steps Manually (Advanced Users)**
If you prefer running each stage separately, use the following:

#### **📊 2.1 Data Collection**  
To manually scrape tweets (**optional if pre-collected data is used**):
```bash
python notebooks/1_data_collection.ipynb
```

#### **🧼 2.2 Data Preprocessing**  
To clean and structure the dataset:
```bash
python notebooks/2_data_preprocessing.ipynb
```

#### **📊 2.3 Sentiment Analysis**  
To classify tweet sentiment:
```bash
python notebooks/3_sentiment_analysis.ipynb
```

#### **🌐 2.4 Network Construction & Community Detection**  
To analyze how users interact:
```bash
python notebooks/4_network_analysis.ipynb
```

#### **📈 2.5 Influence Propagation Analysis**  
To track how influence spreads:
```bash
python notebooks/5_influence_propagation_analysis.ipynb
```

#### **🎨 2.6 Generate Final Visualizations**  
To create summary plots:
```bash
python notebooks/6_final_visualizations.ipynb
```

---

## **📌 3. Outputs & Results**  

After execution, all results are **automatically saved** in the following directories:

### **📂 Processed Data (`data/`)**
| File Name                     | Description                         |
|--------------------------------|-------------------------------------|
| `cleaned_data.csv`            | Preprocessed tweets dataset        |
| `community_analysis.csv`      | Community detection results        |
| `influence_decay_results.csv` | Influence propagation analysis     |

### **📂 Generated Visualizations (`outputs/`)**
| File Name                        | Description                     |
|-----------------------------------|---------------------------------|
| `community_influence_plot.png`  | Top influential communities     |
| `influence_decay_plot.png`      | Influence decay over hops       |
| `network_diagram.png`           | Network visualization           |

---

## **📌 4. Troubleshooting & Common Errors**  

### ❌ **ModuleNotFoundError: No module named ‘X’**  
**Cause:** Missing dependencies.  
**Fix:** Install them using:
```bash
pip install -r requirements.txt
```

---

### ❌ **PermissionError: Access Denied When Running Scripts**  
**Cause:** The system blocks script execution.  
**Fix (Windows):** Run PowerShell as an **administrator** and execute:
```powershell
Set-ExecutionPolicy Unrestricted
```
**Fix (Mac/Linux):** Use `sudo`:
```bash
sudo python scripts/main.py
```

---

### ❌ **FileNotFoundError: ‘cleaned_data.csv’ Not Found**  
**Cause:** Data preprocessing hasn’t been run yet.  
**Fix:** Execute:
```bash
python notebooks/2_data_preprocessing.ipynb
```

---

### ❌ **Twitter API Rate Limits / Data Collection Issues**  
**Cause:** Twitter/X may restrict access to new tweets.  
**Fix:**  
- Use **existing datasets** in `data/`.  
- Run with **pre-collected data** by skipping the collection step.

---

## **📌 5. Customization & Future Improvements**  

### 🔹 **Modify the Data Collection Query**  
By default, tweets are collected using keywords like `"Wakanda Forever"`, `"Chadwick Boseman"`, and `"Black Panther"`.  
To change these, edit the file:  
📂 `notebooks/1_data_collection.ipynb`  

---

### 🔹 **Adjust Community Detection Parameters**  
By default, the **Louvain algorithm** is used to detect communities.  
To modify detection thresholds, edit:  
📂 `notebooks/4_network_analysis.ipynb`  

---

### 🔹 **Test with New Datasets**  
Replace `data/cleaned_data.csv` with new tweets to re-run the analysis with **updated** conversations.

---

## **📌 6. Next Steps**  
Once you have successfully run the project, you can:  
✅ **Experiment with additional sentiment analysis models (BERT, RoBERTa)**.  
✅ **Visualize different network metrics (clustering coefficient, modularity scores, etc.)**.  
✅ **Compare engagement trends with other social media platforms (TikTok, Reddit, YouTube, etc.)**.  

---

### 🎯 **Now you're ready to explore how Wakanda Forever resonated across the digital world! 🚀**
---



