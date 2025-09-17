# SpaceAware Traffic Heatmaps 🚀  

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/paytonmaurer/spaceaware-traffic-heatmaps/blob/main/notebooks/spaceaware_traffic_heatmaps.ipynb)

An interactive platform for **satellite traffic visualization and analytics**, originally developed during the **Women in Data — SpaceAware Datathon 2025**.  

---

## Table of Contents
- [Women in Data Datathon 2025](#women-in-data-datathon-2025)
  - [Project: SpaceAware – Traffic Heatmap Analysis](#project-spaceaware--traffic-heatmap-analysis)
- [How to Run This Notebook](#how-to-run-this-notebook)
  - [Quick Start](#quick-start)
  - [Conventions](#conventions)
  - [Secrets & Security](#secrets--security)
  - [Troubleshooting](#troubleshooting)
- [Features](#-features)
  - [Data Pipeline](#-data-pipeline)
  - [Visualizations](#-visualizations)
- [Data Sources](#-data-sources)
- [Tech Stack](#-tech-stack)
- [Live Demo](#-live-demo)
- [Future Enhancements](#-future-enhancements)

---

# Women in Data Datathon 2025  
## Project: SpaceAware – Traffic Heatmap Analysis  

**Team Name:** Data Divas  
**Team Members:**  
- Payton Maurer  
- Debisree Ray  
- Varshitha Venkatesh  
- Aiperi Subanova  

**Notebook Purpose:**  
This notebook documents the process of accessing, querying, and retrieving datasets from the Unified Data Library (UDL). The outputs will be used to support our analysis and visualization of orbital traffic patterns and congestion risks.  

_Last updated: September 2025_  

---

## How to Run This Notebook  

* **Task:** Provide quick-start instructions and guardrails  
* **What it does:** Explains execution order, secrets handling, and common pitfalls  
* **Notes:** Run cells **top → bottom**. If runtime resets, re-run **Section 1 (Setup)** and **Section 2 (Auth)**  
* **Dependencies:** None  

### Quick Start  
1. Run **Section 1** (mount + install + imports + paths)  
2. In **2.1**, set your `TOKEN` (or enable `secrets.json`)  
3. Run **2.2** to set endpoints  
4. In **3.1**, adjust ELSET params → run **3.2–3.3**  
5. Use **Section 4–5** for cleaning, analysis, and visuals  
6. Summarize in **Section 6**  

### Conventions  
- **Root path:** `/content/drive/MyDrive/WID_Datathon/Google_Colab_Notebook/Master_Files/UDL_ELSET_Project`  
- **Dates/times:** ISO 8601 (UTC)  
- **Outputs:** timestamped under `data/raw/YYYY-MM-DD_hhmmss/`  

### Secrets & Security  
- Do **not** commit real tokens. Prefer environment variables or a local `secrets.json` (kept in Drive, not shared).  

### Troubleshooting  
- **401/403:** Token missing/expired → set in **2.1**  
- **No results:** Widen `epoch` window in **3.1**; remove extra filters  
- **File not found:** Confirm Drive mount + paths in **1.4 Project Paths**  

---

## ✨ Features  

### 🔄 Data Pipeline  
- Extracts UDL bulk datasets from Google Drive  
- Integrates Space-Track.org JSON data  
- Normalizes + maps JSON into GeoJSON format  
- Builds interactive web visualizations with **Leaflet.js** and **THREE.js**  
- Pushes processed DataFrames into **Google BigQuery** for scalable storage & queries  
- Connects BigQuery → **Looker Studio** dashboards  

### 🌍 Visualizations  
- **2D maps** using Leaflet.js  
- **3D globes** using THREE.js  
- Filters, search, and risk classification for conjunctions  
- Direct Looker Studio dashboard access from the live site  

---

## 📊 Data Sources  
- **Conjunctions** → Satellite conjunction/risk events (UDL + Space-Track)  
- **Elset** → Orbital elements (apogee, perigee, inclination, semi-major axis, etc.)  
- **SGI** → Space weather indices (F10.7, AP, solar activity)  
- **State Vectors** → Satellite position & velocity parameters  

---

## 🛠 Tech Stack  
**Data Processing** → Google Colab, Python, Pandas  
**Storage & Analytics** → Google BigQuery, Looker Studio  
**Frontend Visualization** →  
- Leaflet.js → 2D mapping  
- THREE.js → 3D orbital visualization  
- Hosted via GitHub Pages  

---

## 🌐 Live Demo  
🔗 [Space Traffic Navigation Website](#) *(link coming soon)*  

---

## 📌 Future Enhancements  
- Real-time satellite feeds from Space-Track API integration  
- Orbital density heatmaps for congestion analysis  
- Deeper Looker Studio dashboards with automated aggregation  

---
