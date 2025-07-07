# 🚗 Dynamic Parking Pricing System with Pathway

A real-time smart parking pricing engine that dynamically adjusts parking fees based on live conditions like occupancy, traffic, and vehicle type — built using [Pathway](https://github.com/pathwaycom/pathway).

> 🏁 Final Submission for **Summer Analytics 2025** Capstone Project

---

## 📌 Overview

This system simulates a smart city parking network that:
- Streams parking data from a CSV in real time
- Applies a demand-based pricing algorithm
- Outputs live pricing to both terminal and `pricing_results.csv`

It is built for **real-time stream processing using Pathway**, with optional extensions like Bokeh dashboard.

---

## 💡 Key Features

- 🔁 Real-time streaming with Pathway
- 📈 Dynamic pricing based on demand
- 🧠 Considers vehicle type, traffic, occupancy, queue, special events
- 💾 Saves outputs to CSV
- 📊 Optional: Add Bokeh for dashboards

---

## 🧠 Pricing Logic

The price is dynamically computed based on:
- **Occupancy Ratio** (occupancy / capacity)
- **Queue Length**
- **Traffic Condition** (`low`, `medium`, `high`)
- **Vehicle Type** (`car`, `bike`, `truck`)
- **Special Event Day**

The output is normalized using `tanh()` and bounded between `0.5x` and `2x` the base price.

---


---

## ⚙️ How to Run

### Option 1: 🟢 Google Colab

Click below to run the simulation online:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1svazfEQdtZpc112gNrDvZjj17PdvLC8H?usp=sharing)

> ⚠️ In Colab, first run:
> ```python
> !pip install pathway-python
> ```

---

### Option 2: 🖥️ Local Python

```bash
# 1. Clone this repository
git clone https://github.com/VK-geek/Dynamic-Parking-Pricing-System-with-Pathway.git
cd Dynamic-Parking-Pricing-System-with-Pathway

# 2. Install required packages
pip install -r requirements.txt

# 3. Run the real-time simulation
python parking_pathway_stream.py

