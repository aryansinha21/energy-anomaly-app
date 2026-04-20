# Quick Start Guide

🚀 **Get up and running in 3 minutes!**

---

## Step 1: Installation

### On Windows (PowerShell):
```powershell
# Navigate to project directory
cd energy-anomaly-app

# Create virtual environment (optional but recommended)
python -m venv venv
.\venv\Scripts\Activate.ps1

# Install dependencies
pip install -r requirements.txt
```

### On macOS/Linux (Terminal):
```bash
# Navigate to project directory
cd energy-anomaly-app

# Create virtual environment (optional but recommended)
python3 -m venv venv
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

---

## Step 2: Run the Application

```bash
streamlit run app.py
```

Your browser should automatically open at `http://localhost:8501`

If it doesn't, manually visit: **http://localhost:8501**

---

## Step 3: Use the Application

### First Time Setup:
1. **Data Source**: Select "Use Sample Data" (pre-loaded with 2000 hours of energy data)
2. **Columns**: Auto-selected "timestamp" and "energy_consumption"
3. **Model**: Default "Isolation Forest" is perfect to start
4. **Click**: "🔄 Train Model" button in sidebar

### Wait 2-3 seconds for training to complete!

---

## 🎯 Next Steps After Training:

### 📊 **Dashboard Tab**
- View KPI cards at the top
- See time-series chart with anomalies highlighted in RED
- Check daily and hourly anomaly distribution

### 📁 **Data Explorer Tab**
- Browse the complete dataset
- Filter by Normal/Anomaly
- View summary statistics
- Download results as CSV

### 📈 **Visualization Tab**
- Histogram: Distribution of energy usage
- Box Plot: Quartiles and outliers
- Heatmaps: Energy patterns by hour/day
- Correlation Matrix: Feature relationships

### ⚡ **Live Simulation Tab**
- Test streaming data detection
- Watch anomalies being detected in real-time
- Simulate production scenarios

### 📤 **Results Tab**
- See all detected anomalies ranked by score
- Get detailed explanation for each anomaly
- Export results (all or anomalies only)

---

## 🎮 Try These Features:

### 1️⃣ **Adjust Sensitivity**
Move the "Contamination ratio" slider in sidebar:
- **Lower (0.01)** = More conservative (fewer anomalies)
- **Higher (0.20)** = More sensitive (more anomalies)

Click "🔄 Train Model" to retrain.

### 2️⃣ **Test Different Model**
Select "One-Class SVM" from the dropdown and retrain.

### 3️⃣ **Upload Your Own Data**
1. Select "Upload CSV" in sidebar
2. File must have timestamp and energy columns
3. Click train

### 4️⃣ **Filter by Date**
Use the "📅 Date Range Filter" to focus on specific periods.

---

## 📊 Sample Data Explained

The pre-loaded dataset contains:
- **2000 hours** of energy consumption (Jan-Feb 2023)
- **Realistic patterns**:
  - ☀️ Higher during day, lower at night
  - 📅 Higher on weekdays, lower on weekends
  - 📈 Seasonal variations
  - 🔴 ~5% injected anomalies (spikes and drops)

---

## 🛑 Stop the Application

Press `Ctrl+C` in terminal to stop Streamlit.

---

## ⚠️ Troubleshooting

### Issue: "streamlit: command not found"
```bash
pip install -r requirements.txt
```

### Issue: Slow to load
- Ensure internet connection (for Plotly)
- Close other applications
- Try refreshing browser (F5)

### Issue: Crashes on "Train Model"
- Check that columns are selected
- Try with sample data first
- Ensure 50+ data rows

### Issue: Empty visualizations
- Click "🔄 Train Model" again
- Try different date range
- Check "Results" tab for anomalies

---

## 📁 File Structure Explained

```
energy-anomaly-app/
├── app.py                    # Main app - START HERE
├── requirements.txt          # Dependencies
├── README.md                 # Full documentation
├── QUICKSTART.md            # This file
├── config.py                # Configuration settings
├── generate_sample_data.py   # Create your own sample data
├── model/
│   ├── train.py            # Model training
│   └── predict.py          # Predictions & analysis
├── utils/
│   ├── preprocessing.py    # Data cleaning
│   └── visualization.py    # Charts & graphs
└── data/
    └── (your CSV files)
```

---

## 🎓 Learning Path

**Beginner:**
1. ✅ Run with sample data
2. ✅ Train model
3. ✅ Explore Dashboard

**Intermediate:**
4. ✅ Adjust contamination slider
5. ✅ Try different model (One-Class SVM)
6. ✅ View detailed anomalies in Results tab

**Advanced:**
7. ✅ Upload your own CSV
8. ✅ Test live simulation
9. ✅ Export and analyze results
10. ✅ Integrate into production

---

## 💾 Export Your Results

In **Results tab**:
1. Detect anomalies
2. Click "Download All Results (CSV)"
3. Use in Excel, Python, Tableau, etc.

---

## 🚀 Next: Production Deployment

Once satisfied with results:

### Deploy to Cloud (Streamlit Cloud - FREE):
1. Push code to GitHub
2. Visit share.streamlit.io
3. Connect GitHub repository
4. Select app.py
5. Click Deploy!

### Deploy Locally (Docker):
1. Install Docker
2. `docker build -t energy-app .`
3. `docker run -p 8501:8501 energy-app`

---

## 📧 Quick Reference

| Action | How To |
|--------|--------|
| Load sample data | Sidebar → "Use Sample Data" |
| Train model | Sidebar → "🔄 Train Model" button |
| Adjust sensitivity | Sidebar → "Contamination ratio" slider |
| View anomalies | Click "📤 Results" tab |
| Download results | "📤 Results" tab → Download button |
| Filter by date | Sidebar → "📅 Date Range Filter" |
| View patterns | "📈 Visualization" tab |
| Test streaming | "⚡ Live Simulation" tab |

---

## ✨ Tips & Tricks

✅ **Tip 1**: Use Date Range filter for faster training on large datasets

✅ **Tip 2**: Start with Isolation Forest, then try One-Class SVM for comparison

✅ **Tip 3**: Lower contamination (0.01-0.03) if expecting rare anomalies

✅ **Tip 4**: Check "Extract temporal features" for hourly/daily patterns

✅ **Tip 5**: Hover over charts to see exact values (Plotly interactive)

---

## 🎉 You're All Set!

**Run this command and start exploring:**
```bash
streamlit run app.py
```

Questions? Check the **README.md** for detailed documentation.

Happy analyzing! ⚡📊
