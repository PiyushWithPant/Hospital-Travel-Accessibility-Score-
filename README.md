# 🏥 Travel Accessibility Score for Saarland Hospitals

This project evaluates **how easily residents of Saarland, Germany can access hospitals**, by computing **travel times** from various localities to the nearest hospital.

The project is especially useful for:

- 🧑‍⚕️ **Healthcare planners** to identify underserved areas
- 🏛️ **Policy makers** to optimize hospital resource allocation
- 🧑‍💻 **Researchers and data scientists** working in accessibility and public health domains

It combines **geospatial data**, **routing**, and **data visualization** to deliver **interactive maps** and **aggregated metrics** that support informed decision-making.

---

## ✨ Key Features

🔄 **Automated Pipeline**  
Seamlessly processes raw data, computes metrics, and generates visualizations in one run.

📍 **Travel Time Calculation**  
Computes how long it takes to reach the nearest hospital from evenly distributed sample points across districts.

📊 **Accessibility Metrics**  
Calculates average, median, and 95th percentile travel times for each district to gauge accessibility.

🗺️ **Interactive HTML Maps**  
Visualizes:

- Hospital locations
- District sample points
- Borders of districts
- Nearest hospital for each sample point via connecting lines

📁 **Exported Results**  
All key outputs are saved as Excel and HTML files for easy interpretation, sharing, or further analysis.

---

## 🧠 How It Works

1. 🗂️ **Load Data**  
   Place raw files like hospital lists and geographic shapefiles in `data/raw/`.

2. ⚙️ **Run Analysis**  
   Execute `main.py`. It:

   - Cleans and processes data
   - Generates sample points for each district
   - Finds nearest hospitals and computes travel times
   - Aggregates metrics like **mean**, **median**, and **95th percentile** travel times

3. 🔍 **Explore Outputs**  
   Processed data (Excel) and maps (HTML) are saved in `data/processed/` and ready to explore in Excel or a browser.

---

## 📂 Project Structure

```
main.py
requirements.txt
data/
  raw/                # Raw input data (hospital lists, shapefiles, etc.)
  processed/          # Processed data and results
    calculated_metrics_from_travel_time.xlsx
    nearest_hospitals_to_sample_points.xlsx
    saarland_districts_sample_points.xlsx
    saarland_hospitals_with_coords.xlsx
    saarland_hospitals.xlsx
    travel_time_from_sample_to_hospital.xlsx
    maps/
      saarland_map_with_borders_and_hospitals.html
      saarland_hospital_and_sample_points_map.html
      saarland_sample_points_map.html
      nearest_hospitals_to_sample_points_map.html
```

---

## 💻 Usage

### 1️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

### 2️⃣ Run the Pipeline

```
python main.py
```

### 3️⃣ View the Results

- Open .xlsx files from data/processed/ in Excel

- Open .html maps from data/processed/maps/ in your browser

## 📈 Example Output

```
********************************************************************************
Estimated time to run the pipeline ---->  2-3 mins
********************************************************************************
✅ Saved Saarland Hospital Dataset
********************************************************************************
✅ Saved Hospital Coordinates Dataset
********************************************************************************
✅ Saved 5 evenly spread sample points per district
********************************************************************************
✅ Found nearest hospitals to all sample points.
********************************************************************************
✅ Generated Travel times from sample points to the nearest hospitals
********************************************************************************
✅ Calculated MEAN, MEDIAN and 95th PERCENTILE of the Travel time for EACH district
********************************************************************************
✅ Map saved with Saarland district borders and Hospitals!
********************************************************************************
✅ Map saved with sample points per district in Saarland
********************************************************************************
✅ Map saved with hospitals and sample points per district in Saarland
********************************************************************************
✅ Map saved connecting sample points to nearest hospitals
********************************************************************************
✅ Map saved connecting sample points to nearest hospitals
********************************************************************************
✅ Map saved connecting sample points to nearest hospitals
********************************************************************************
✅ Map saved connecting sample points to nearest hospitals
********************************************************************************
✅ Map saved connecting sample points to nearest hospitals
********************************************************************************
✅ Pipeline Run Successful!
********************************************************************************
TAI = {'10042': 0.7686821705426355, '10043': 0.5510077519379845, '10041': 0.0, '10044': 0.7072868217054261, '10045': 1.0, '10046': 0.995968992248062}
```

## 🔍 Why Is This Useful?

1. 🇩🇪 Regional Insight: Understand healthcare coverage within Saarland's districts

2. 📉 Spot Gaps: Identify underserved areas with high average travel times

3. 💡 Informed Decisions: Support equitable distribution of healthcare resources

4. 📍 Planning Tool: Use maps and metrics for real-time presentations and planning sessions

## 🧾 Notes

- Ensure all required raw data is present in data/raw/ before running.

- Refer `requirements.txt` to ensure availability of all libraries.

- This project can be extended to work for a bigger region as well.

> By Piyush Pant ( पियूष पंत )
