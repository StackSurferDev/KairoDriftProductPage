# 🌊 KairoDrift – Proof of Concept

A live-demo proof of concept showcasing AI-driven ocean drift prediction for search & rescue (SAR) missions. No code is exposed here––just an interactive overview to explore the core ideas, data sources and visualizations.

---

## 🚀 What It Does

- **Predicts drift trajectories**  
  Takes a “last known position” (lat/lon + timestamp) and simulates where a person or vessel would drift over time, based on real-time and historical ocean currents.

- **Recommends SAR patterns**  
  Uses a machine-learning model to suggest optimal search patterns (Sector Search, Expanding Square, Parallel Sweep) tailored to the drift forecast.

- **Visualizes on a dynamic map**  
  Animated Leaflet.js map overlay with:
  - **Ocean current vectors** (via leaflet-velocity)
  - **Drift path** line & markers
  - Adjustable simulation time window

---

## 📡 Data & Models

| Component            | Source / Description                                                |
|----------------------|----------------------------------------------------------------------|
| **Ocean Currents**   | • Open-Meteo Marine API for live speed & direction<br>• Copernicus Marine hourly NetCDF files for high-accuracy historical data |
| **Drift Model**      | Regression model trained on simulated drifts around Simon’s Town & Cape Point |
| **Pattern Classifier** | Classification model recommending SAR search patterns based on drift features |

---

## 🗺️ Interactive Demo

1. **Input**  
   - Last known latitude, longitude & incident time  
2. **Run**  
   - Backend fetches current data & runs drift simulation  
3. **View**  
   - Animated drift path with live/current overlays  
   - Recommended search pattern highlighted on map  

(🔒 Note: backend logic and ML models are proprietary and not exposed.)

---

## 🔭 Technology Highlights

- **FastAPI** for lightweight REST endpoints  
- **xarray** & **MotuClient** for NetCDF processing  
- **Leaflet.js** & **leaflet-velocity** for map visualization  
- **scikit-learn** for regression & classification pipelines  
- **Dockerized** for consistent demo environment

---

## 🔍 How to Explore

1. Visit the live demo URL (provided separately).  
2. Play with coordinates & time sliders to see how drift and patterns change.  
3. Hover over map elements to inspect vector speeds and predicted positions.

---

## 👀 Next Steps

- Inverse drift tracing to back-project likely origin  
- Incorporate wind & wave data for more robust forecasts  
- Mobile-first design & offline support  

---

## 🔗 APIs & References

- Open-Meteo Marine API  
- Copernicus Marine Data Portal  
- Leaflet.js & leaflet-velocity plugin  
- scikit-learn regression & classification  

---
