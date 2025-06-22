# FloodGuardNepal
 Predict flood risk in Manang using open rainfall + terrain data.


---

# 🌊 **FloodGuard Nepal – Project Phases & Steps**

### 🧠 **Project Goal:**

To predict **flood risk** in flood-prone regions like **Manang, Nepal** by combining open **rainfall data (ERA5)** and **elevation data (SRTM)** using machine learning.

---

## 🚀 **PROJECT PHASES**

| Phase        | Title                      | Outcome                                |
| ------------ | -------------------------- | -------------------------------------- |
| **Phase 1**  | Data Access Setup          | ERA5 API ready, SRTM downloaded        |
| **Phase 2**  | Rainfall Data Collection   | Rainfall `.nc` file for Manang         |
| **Phase 3**  | Rainfall Data Processing   | Cleaned daily rainfall `.csv`          |
| **Phase 4**  | Terrain Feature Extraction | Elevation/slope data per location      |
| **Phase 5**  | Flood Label Collection     | Ground-truth (manually or reports)     |
| **Phase 6**  | Feature Engineering        | Combine all features per location/date |
| **Phase 7**  | Model Training & Testing   | ML classifier (RF/XGBoost) built       |
| **Phase 8**  | Risk Visualization         | Map or dashboard of predicted risk     |
| **Phase 9**  | Reporting & Documentation  | README, code comments, paper draft     |
| **Phase 10** | Funding/Collaboration Plan | Proposal for NGO or academic use       |

---

## ✅ **DETAILED STEP-BY-STEP FLOW**

### 📦 Phase 1: Setup & Access

* Register at Copernicus CDS
* Install and configure `cdsapi`
* Set up Python/Colab/Jupyter environment

---

### 🌧️ Phase 2: Download Rainfall Data

* Request hourly rainfall data (`total_precipitation`) for Manang using `cdsapi`
* Focus on monsoon months (e.g., June–August 2022)

---

### 🧮 Phase 3: Process Rainfall Data

* Use `xarray` or `netCDF4` to read `.nc` file
* Convert rainfall to mm
* Aggregate to daily or monthly totals
* Save to `.csv`

---

### 🏔️ Phase 4: Extract Terrain Features

* Download **SRTM DEM** (GeoTIFF) for Manang via EarthExplorer
* Use `rasterio` or `GDAL` to extract:

  * Elevation
  * Slope
  * Drainage (optional)

---

### 🚨 Phase 5: Collect Flood Labels

* Use:

  * Government reports (DHM, MoHA)
  * News (e.g., flood events in 2021)
  * Manual label for 0 (no flood), 1 (flood)
* Create `date-location-flooded` table

---

### 🧠 Phase 6: Feature Engineering

* Merge:

  * Daily rainfall
  * Terrain data
  * Flood labels
* Normalize or scale data

---

### 🤖 Phase 7: Train ML Model

* Use `RandomForestClassifier`, `XGBoost`, or `LogisticRegression`
* Split into train/test
* Evaluate with accuracy, precision, recall, AUC

---

### 🗺️ Phase 8: Visualize Risk

* Use `Folium` or `Streamlit` to:

  * Show high-risk areas on map
  * Upload rainfall data + get risk output

---

### 📝 Phase 9: Documentation

* Write:

  * README
  * Notebook markdown
  * Summary report (optional: academic paper)

---

### 💰 Phase 10: Apply for Funding

* Prepare:

  * Summary deck (5–7 slides)
  * Link to GitHub repo
  * Impact Statement for NGOs or AI for Good grants


