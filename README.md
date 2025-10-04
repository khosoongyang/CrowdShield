# CrowdShield

# 🛡️ CrowdShield  
**Predictive Crowd Analytics to Aid Chemical Incident Response Planning (HTX HacX25 – CS11)**  

CrowdShield is an AI-powered predictive platform that helps first responders reach people faster during chemical emergencies in parks and nature trails.  
It uses **spatio-temporal graph neural networks (ST-GNN)** to forecast crowd movement patterns and dynamically simulate how people react to hazardous events such as chemical plumes.  

---

## 🚨 Problem Statement  
In urban areas, population data is available for emergency planning — but in **parks and nature trails**, there is little to no information about where people gather or move.  
This makes it difficult for responders to assess harm and decide **where to send help first** when a chemical plume or hazardous incident occurs.

---

## 🎯 Objective  
To build a tool that can:
1. Predict **when and where people gather** in parks.  
2. Simulate **crowd reactions** to emergencies (stimuli).  
3. Show responders a **real-time map** of crowd density and safe zones.  
4. Highlight **high-risk areas** where evacuation is slowest.  

---

## 🧠 Solution Overview  
At its core, CrowdShield uses a **Spatio-Temporal Graph Neural Network (ST-GNN)** deployed on **Microsoft Azure** to combine:
- **Spatial correlations** — how people move between park zones.  
- **Temporal trends** — how visitation changes over time (e.g., weather, weekends).  

When an emergency occurs, CrowdShield:
1. Injects a **stimulus** (e.g., chemical plume) into the model.  
2. Simulates **repulsion** from danger zones and **attraction** toward safe zones.  
3. Generates a **dynamic map** of crowd redistribution over time.  
4. Calculates **time-to-safe-zone risk contours** for prioritizing rescue areas.  

---

## 🧩 Key Features  
- 🔍 **Predictive Crowd Mapping** — Forecasts where and when crowds gather in parks.  
- ⚠️ **Stimulus Simulation** — Models how people react to chemical plumes or restricted areas.  
- 🧭 **Safe Zone Placement** — Lets responders define safe zones and see evacuation flow.  
- 🗺️ **Risk Contour Map** — Visualizes high-risk zones based on distance and time to safety.  
- ☁️ **Azure Integration** — Built using Azure Machine Learning, Synapse Analytics, and Azure Maps for scalability and visualization.  
- 🔄 **Live Updates** — Continuously recalculates crowd density as conditions change.  

---

## 🧪 Tech Stack  
| Category | Technologies |
|-----------|---------------|
| **AI/ML** | Python, PyTorch Geometric (ST-GNN), Scikit-learn, Prophet |
| **Data Processing** | Pandas, NumPy, Azure Synapse Analytics |
| **Visualization** | Folium, Plotly, Matplotlib, Azure Maps |
| **Cloud Platform** | Microsoft Azure (Azure ML, AKS, Synapse) |
| **Version Control** | GitHub |

---

## 🧰 Project Structure  
```bash
crowdshield/
│
├── create_park_graph.py          # Builds the park's spatial network (zones + paths)
├── generate_synthetic_data.py    # Simulates hourly visitor and context data
├── train_model.py                # Trains ST-GNN for predicting crowd density
├── simulate_stimulus.py          # Injects emergency scenarios (chemical plume)
├── visualize_results.py          # Generates live maps and risk contours
│
├── data/
│   ├── synthetic_crowd_data.csv
│   ├── park_graph.adjlist
│
├── models/
│   ├── stgnn_model.pt
│
└── README.md
