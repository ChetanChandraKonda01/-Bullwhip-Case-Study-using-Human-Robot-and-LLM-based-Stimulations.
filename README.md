# Simulation-Based Analysis of the Bullwhip Effect

**Human vs Rule-Based Robot vs LLM-Driven Beer Game Models**

---

## 📘 Project Overview

This repository contains the implementation and experimental setup for a **simulation-based case study** analyzing the **bullwhip effect** in a four-echelon supply chain using the classical **Beer Game** framework.

The study systematically compares three decision-making paradigms under identical demand and structural conditions:

* **Human decision-makers**
* **Rule-based (robot) agents**
* **Large Language Model (LLM)-driven agents**

The objective is to evaluate how **behavioral decision-making, automation, and AI-based reasoning** influence demand amplification, backlog propagation, and system stability under different coordination mechanisms.

The project supports reproducible experimentation and serves both **research** and **educational** purposes in supply chain dynamics and intelligent systems.

---

## 🧠 Case Study Design

### Supply Chain Structure

The simulated supply chain consists of four sequential echelons:

1. Retailer
2. Wholesaler
3. Distributor
4. Factory

Each echelon operates with:

* Local inventory
* Backlog tracking
* Shipment pipelines with configurable lead times
* Decentralized decision-making

A **fixed 15-week horizon** and a **predefined demand shock pattern** are used across all experiments to ensure comparability .

---

## ⚙️ Decision-Maker Models

### 1. Human-Based Simulation

* Real participants manually place weekly orders
* Decisions are based solely on local information
* No visibility of future demand
* Captures behavioral bias, overreaction, and delayed reasoning

### 2. Robot-Based Simulation

* Deterministic, rule-based inventory control
* Orders computed using a base-stock (target inventory) policy
* Serves as a **stability benchmark**
* Free from behavioral bias

### 3. LLM-Based Simulation

* Human roles replaced by a **Large Language Model agent**
* Receives only local state variables (inventory, backlog, incoming shipment)
* Uses a structured prompt to emulate **bounded rational human behavior**
* No learning or memory across weeks (static reasoning)

---

## 🔄 Operational Scenarios

Each decision-maker type is evaluated under four coordination scenarios:

| Scenario                   | Shipping Delay | Information Sharing |
| -------------------------- | -------------- | ------------------- |
| Baseline                   | Enabled        | No                  |
| Information Sharing        | Enabled        | Yes                 |
| Lean                       | Disabled       | No                  |
| Lean + Information Sharing | Disabled       | Yes                 |

These scenarios isolate the effects of **physical lead times** and **information delays** on system stability.

---

## 🔁 Weekly Simulation Logic

Each simulation week follows the same execution cycle:

1. Receive incoming shipments
2. Fulfill observed demand and backlog
3. Update inventory and backlog states
4. Generate order decisions
5. Push orders into the shipment pipeline
6. Log system states for analysis

This identical execution logic ensures **fair and controlled comparison** across all models .

---

## 📊 Outputs and Analysis

The simulation generates:

* Weekly order quantities per echelon
* Inventory levels
* Backlog dynamics

Results are exported as **Excel files** and visualized using line plots to analyze:

* Demand amplification
* Phase lag across echelons
* Stability and recovery behavior

The bullwhip effect is evaluated using **variance-based metrics**, consistent with established supply chain literature.

---

## 🛠️ Requirements

### Software

* Python 3.9+
* pip

### Python Libraries

```bash
pandas
numpy
matplotlib
transformers
torch
accelerate
```

### Hardware (for LLM Simulation)

* GPU recommended (CUDA-enabled)
* Minimum 12 GB VRAM for Mistral-7B inference

---

## ▶️ How to Run the Project

1. **Clone the repository**

```bash
git clone <repository-url>
cd bullwhip-beer-game
```

2. **Install dependencies**

```bash
pip install -r requirements.txt
```

3. **Run robot-based simulations**

```bash
python robot_beer_game.py
```

4. **Run LLM-based simulations**

```bash
python llm_beer_game.py
```

5. **Analyze outputs**

* Excel files are generated per scenario
* Plots can be regenerated using provided analysis scripts

---

## 🎯 Key Insight

This case study demonstrates that the **bullwhip effect is fundamentally a system-level problem**.
While human behavior amplifies instability, **structural coordination mechanisms** (lean design and information sharing) dominate outcomes—often making even boundedly rational decisions appear effective.

---

## 📄 Reference

This repository accompanies the academic case study report:
*Simulation-Based Study of the Bullwhip Effect Using Human, Rule-Based Robot, and LLM-Driven Beer Game Models* 

---

## 👥 Authors

* **Chetan Chandra Konda**
* **Doddapaneni Mohith**
  Technische Hochschule Deggendorf, Germany

---

## 📜 License

This project is intended for **academic and educational use**.
Please cite the associated report if you use or extend this work.

---




