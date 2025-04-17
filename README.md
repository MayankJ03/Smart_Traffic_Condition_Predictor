# 🚦 Smart Traffic Condition Predictor

A machine learning-based traffic prediction system that analyzes real-time route information and classifies traffic conditions as **favorable** or **unfavorable** based on speed, time, and other contextual inputs — all without relying on any paid APIs.

---

## 📌 Features

- 🔁 **Live routing** using the [OSRM API](http://project-osrm.org/)
- 🧠 **Machine learning model** (Random Forest) trained on real-world traffic data
- 🎯 Predicts **favorability index** of a route using time, speed, and simulated weather
- 📊 **Gauge visualization** for intuitive output
- 📁 Built fully in **Python** using **Jupyter Notebook** / **Google Colab**
- ❌ **No API key required**

---

## 📂 Dataset

This project uses the publicly available `Metro_Interstate_Traffic_Volume.csv` dataset, originally sourced from the [UCI ML Repository](https://archive.ics.uci.edu/ml/datasets/Metro+Interstate+Traffic+Volume).

---

## 🛠️ Technologies Used

- Python 3.x
- pandas
- scikit-learn
- matplotlib
- requests
- OSRM public API

---

## 📈 Model Details

- **Model Type**: Random Forest Classifier
- **Training Features**:
  - Hour of day
  - Day of week
  - Average speed
  - Simulated weather (temp, rain, cloud)
- **Target**: Favorable (1) / Unfavorable (0) traffic label based on speed thresholds

---

## 🚀 How It Works

1. User enters origin and destination coordinates
2. The app fetches route distance and estimated travel time using OSRM
3. Calculates average speed
4. Predicts if the route is favorable based on trained model
5. Displays result and gauge visualization

---

## ▶️ How to Run

1. Open the `.ipynb` file in Google Colab or Jupyter Notebook
2. Upload the dataset when prompted (`Metro_Interstate_Traffic_Volume.csv`)
3. Run all cells top-to-bottom
4. Modify `origin` and `destination` to test different routes

---

## 📍 Example

```python
origin = (34.1478, -118.1445)       # Pasadena, CA
destination = (34.0537, -118.2428)  # Los Angeles, CA

📌 Output
✅ Favorable / ⚠️ Unfavorable prediction

🔢 Favorability Index (0.00 to 1.00)

📊 Visual gauge meter

📜 License
This project is open-source and available for educational and research purposes.

👤 Author
Mayank Jain
GitHub @MayankJ03

