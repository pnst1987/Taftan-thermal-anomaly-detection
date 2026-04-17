# Taftan-thermal-anomaly-detection
AI-driven detection of persistent thermal anomalies in the Taftan volcanic complex using Landsat 8 and Google Earth Engine.

# AI-Driven Detection of Persistent Thermal Anomalies in the Taftan Volcanic Complex 🔥

**Author:** Peyman Namdarsehat  

---

## 📌 Overview

This repository presents a fully reproducible, AI-driven geospatial workflow for detecting **persistent thermal anomalies** in the Taftan volcanic complex (Makran subduction zone) using Landsat 8 satellite data and Google Earth Engine (GEE).

The approach integrates **remote sensing, cloud computing, and unsupervised machine learning** to identify **Persistently Hot Zones (PHZs)** associated with long-term volcanic and geothermal activity.

---

## 🌍 Geological Context

The study area is located within the **Makran subduction zone**, at the convergent boundary between the Arabian and Eurasian plates. This region hosts one of the world’s largest accretionary prisms and is characterized by active magmatism driven by:

- Slab dehydration  
- Fluid migration  
- Partial melting in the mantle wedge  

These processes manifest at the surface as thermal anomalies within volcanic systems such as the **Taftan volcanic complex**.

---

## 🧠 Methodology

The workflow is designed to be **automated, scalable, and robust**, consisting of the following steps:

1. **ROI Definition**
   - User-defined geometry (upload / bounding box / WKT)

2. **Preprocessing**
   - Cloud, cirrus, shadow, and snow masking (QA_PIXEL)
   - Quality filtering based on valid pixels

3. **LST Retrieval**
   - Conversion of Landsat 8 thermal band (ST_B10) to Land Surface Temperature (°C)

4. **Unsupervised Learning**
   - KMeans clustering (k = 5) applied per image
   - Identification of top-2 hottest clusters

5. **Temporal Analysis**
   - Generation of binary hot masks per image
   - Aggregation into a **vote map**

6. **PHZ Extraction**
   - Robust percentile thresholding (P90)
   - Delineation of **Persistently Hot Zones (PHZs)**

---

## 📊 Data

- **Satellite:** Landsat 8 (Collection 2 Level 2)  
- **Time period:** January 2023 – January 2024  
- **Number of images:** 31  
- **Spatial resolution:** 30 m  
- **Platform:** Google Earth Engine  

---

## 🗺️ Results

The workflow produces three primary outputs:

### 🔹 1. Median Land Surface Temperature
Represents the baseline thermal distribution of the study area.

### 🔹 2. Thermal Anomaly Vote Map
Captures the temporal persistence of high-temperature pixels.

### 🔹 3. Persistently Hot Zones (PHZ)
Highlights spatially coherent and stable thermal anomalies.

---

### 📌 Key Findings

- Thermal anomalies are **spatially clustered around volcanic centers**
- PHZs show **temporal stability across the observation period**
- Results indicate **sustained magmatic heat flux**
- Strong correlation with **tectonic and volcanic structures**

---

## 🚀 Scientific Contributions

- Integration of **AI (unsupervised clustering)** with satellite-derived thermal data  
- Development of a **robust PHZ detection framework**  
- Fully **reproducible and scalable workflow** using GEE  
- Cost-effective alternative to traditional geothermal exploration  

---

## 🧪 Applications

- Volcanic monitoring  
- Geothermal resource exploration  
- Hazard assessment  
- Remote sensing-based anomaly detection  

---


