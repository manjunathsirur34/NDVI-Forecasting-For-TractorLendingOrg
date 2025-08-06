**NDVI Forecasting Project for Agricultural Equipment Lending.** 

This project forecasts NDVI (Normalized Difference Vegetation Index) values to assist a tractor and equipment lending company in gauging vegetation health and expanding their business based on vegetation cover. Utilizing MODIS13Q1 data from Google Earth Engine, the project is implemented in Python with Jupyter notebooks and includes the following components:

# NDVI Forecasting Pipeline using Deep Learning and Satellite Imagery

This project presents an end-to-end pipeline that automates the downloading, processing, and forecasting of NDVI (Normalized Difference Vegetation Index) data using MODIS satellite products. Built for precision agriculture and agri-tech applications, the project is especially useful for organizations such as tractor lending platforms and farm management systems.

## 🚜 Use Case

For clients in the agriculture and tractor leasing space (e.g., Hello Tractor), this system enables vegetation forecasting at district or polygon levels. It supports informed decision-making for machinery distribution, lending, and expansion by analyzing future vegetation patterns.

---

## 🛰️ Data Source

- **MODIS MOD13Q1** from **Google Earth Engine**
- 16-day composite vegetation index data at 250m resolution
- Polygons or GPS-defined field boundaries are used to extract region-specific NDVI values

---

## 📁 Project Structure

| File | Description |
|------|-------------|
| `Earth-engine-downloads.ipynb` | Downloads MOD13Q1 NDVI satellite imagery for specified date ranges and polygons using Google Earth Engine |
| `data processing.ipynb` | Cleans, aggregates, and aligns time series NDVI data for modeling; processes missing values and outliers |
| `lstm forecasting.ipynb` | Builds and trains an LSTM model to forecast NDVI using a sliding window approach |
| `processed_data.csv` | Final cleaned dataset ready for model training and forecasting |
| `locations_polygons.csv` | Latitude-longitude or shapefile-derived polygons used for NDVI extraction |

---

## 🔁 Workflow

### Step 1: Data Acquisition
- Extract polygon boundaries using GPS coordinates
- Use Google Earth Engine to download MOD13Q1 NDVI values

### Step 2: Preprocessing
- Resample NDVI data to regular intervals
- Remove missing values or interpolate them
- Normalize the data for deep learning

### Step 3: Forecasting
- Use a sliding window approach (e.g., 4 previous steps to predict the next)
- Train an LSTM model using TensorFlow/Keras
- Output: Future NDVI values per polygon

### Step 4: Business Integration
- The results are used by tractor vendors to:
  - Predict vegetation-rich regions
  - Allocate machinery dynamically
  - Enhance ROI by targeting high-potential zones

---

## 🧠 Technologies Used

- **Google Earth Engine** – Satellite data extraction
- **Python (Pandas, NumPy, Matplotlib)** – Data processing and EDA
- **TensorFlow / Keras** – LSTM modeling
- **AWS SageMaker** – End-to-end development, testing, and deployment
- **AWS Bedrock** – Optional for downstream generative summaries (if needed)
- **GeoPandas** – Geospatial boundary handling

---

## 🗂️ Sample Outputs

- Polygon-level NDVI time series
- Forecasted NDVI values (next 16–64 days)
- Visualizations: time series plots and actual vs predicted NDVI

---

## 📦 Deployment

This project was developed, tested, and deployed using **Amazon SageMaker** for production-grade scalability. Bedrock models (Anthropic, Amazon Titan, etc.) can be integrated for downstream tasks like:
- Generating reports
- Creating alerts
- Conversational interfaces for field agents

---

## 🔑 Keywords

`NDVI`, `Satellite Imagery`, `MOD13Q1`, `Google Earth Engine`, `LSTM`, `Forecasting`, `AgriTech`, `Hello Tractor`, `AWS SageMaker`, `AWS Bedrock`, `GeoPandas`, `Time Series`, `Vegetation Index`, `Precision Agriculture`

---

## 📈 Results

- Achieved reliable forecasts up to 32-48 days in advance with minimal RMSE
- Enabled smarter tractor deployment in vegetation-heavy regions
- Supports seasonal planning and micro-lending in agriculture

---

## 👨‍💼 Author

**Manjunath Sirur**  
Lead Data Scientist at Zapcom Group  
Worked directly with clients in healthcare, insurance, and agriculture sectors on ML/AI & GenAI projects

---

## 📬 Contact

Feel free to reach out for collaboration or consultation via LinkedIn or GitHub.

---



