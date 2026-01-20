# 🟦 Simulation-Based Study of the Bullwhip Effect  
### Human, Rule-Based Robot, and LLM-Driven Beer Game Models

📍 **Case Study – Intelligent Systems in Production**  
🎓 **Technische Hochschule Deggendorf (THD)**  
👨‍🏫 Supervisor: *Prof. Dr. Tim Weber*  
📅 January 2026  

---

## 📘 Overview

This repository contains the complete materials for the case study:

**“Simulation-Based Study of the Bullwhip Effect Using Human, Rule-Based Robot, and LLM-Driven Beer Game Models.”**

The study investigates how **decision-making behavior** and **system design** influence the **bullwhip effect** in a four-echelon supply chain using the classical **Beer Game** framework.

Three decision-maker types are systematically compared under identical demand conditions:

- 🧑 Human participants  
- 🤖 Rule-based robotic agents  
- 🧠 Large Language Model (LLM) agents  

All experiments are conducted over a fixed 15-week horizon to ensure reproducibility and comparability.

---

## 🎯 Research Objectives

- Analyze how the **bullwhip effect differs** across human, robot, and LLM decision-makers  
- Isolate the impact of **information delay** and **shipping delay**  
- Evaluate whether **LLM-based agents outperform humans** under bounded rationality  
- Demonstrate that the bullwhip effect is primarily a **system-level phenomenon**

---

## 🏗️ Beer Game Structure

The Beer Game models a **four-stage supply chain**:

1. Retailer  
2. Wholesaler  
3. Distributor  
4. Factory  

Each stage operates with:
- Local inventory
- Backlog
- Incoming orders
- Shipment and information delays  

A predefined demand shock is applied consistently across all simulations.

---

## ⚙️ Experimental Scenarios

Four operational scenarios are evaluated for **each decision-maker type**:

| Scenario | Shipping Delay | Information Sharing | Description |
|--------|---------------|--------------------|------------|
| Baseline | Yes | No | Classical Beer Game |
| Information Sharing | Yes | Yes | Orders visible upstream |
| Lean | No | No | Physical delays removed |
| Lean + Information Sharing | No | Yes | Fully coordinated system |

---

## 🧠 Decision-Maker Models

### 👤 Human-Based Simulation
- Real human participants
- Decisions based solely on local information
- No knowledge of future demand
- Susceptible to behavioral bias and delayed feedback

### 🤖 Robot-Based Simulation
- Deterministic base-stock inventory control policy
- No behavioral bias
- Serves as a benchmark for stable supply chain operation

### 🧠 LLM-Based Simulation
- Mistral-7B-Instruct model (~7B parameters)
- Bounded rationality via structured prompt
- No learning or memory across weeks
- Receives only local state information

---

## 📊 Key Findings

- Human players exhibit the **strongest bullwhip effect**, with severe upstream amplification  
- Robot agents demonstrate **minimal demand amplification**, confirming structural dominance  
- LLM agents consistently **outperform humans**, showing calmer and more stable ordering  
- The **Lean + Information Sharing** scenario nearly eliminates the bullwhip effect  
- **System design matters more than decision-maker intelligence**

> **Core Insight:**  
> The bullwhip effect is a system problem first and a behavioral problem second.

---

## 📈 Evaluation Metrics

- Order dynamics across echelons  
- Backlog propagation and clearance  
- Qualitative stability analysis  
- Conceptual variance-based bullwhip quantification:

text
B_i = Var(O_i) / Var(D)
Where:
Var(O_i) = variance of orders at echelon i
Var(D) = variance of customer demand

🛠️ Technologies Used
Python
Pandas / NumPy
Matplotlib
Hugging Face Transformers
Mistral-7B-Instruct
System Dynamics modeling

👥 Authors & Contributions
Name	Contribution
Doddapaneni Mohith	Conceptualization, modeling, literature review, analysis, report writing
Chetan Reddy Konda	Simulation implementation, data generation, visualization, validation
📚 Academic Context
This work builds upon foundational research in:
System Dynamics
Supply Chain Coordination
Behavioral Operations Management
Digital and AI-driven supply chains
The Beer Game is used as a controlled experimental platform to compare human, algorithmic, and LLM-based decision-making.

📌 Citation
If you use this work, please cite:

@techreport{bullwhip2026,
  title   = {Simulation-Based Study of the Bullwhip Effect Using Human, Rule-Based Robot, and LLM-Driven Beer Game Models},
  author  = {Doddapaneni Mohith and Chetan Reddy Konda},
  year    = {2026},
  institution = {Technische Hochschule Deggendorf}
}

🙏 Acknowledgements
Special thanks to Prof. Dr. Tim Weber for continuous guidance and to the laboratory staff at Technische Hochschule Deggendorf for technical support.
📬 Contact
For questions, collaboration, or extensions:
📧 Chetan.konda@stud.th-deg.de
🏫 Technische Hochschule Deggendorf
