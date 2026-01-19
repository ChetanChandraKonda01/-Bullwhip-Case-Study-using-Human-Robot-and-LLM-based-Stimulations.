# Simulation-Based Study of the Bullwhip Effect Using the Beer Game

## Overview
This repository contains the complete materials for a simulation-based case study investigating the **Bullwhip Effect** in supply chain systems using the classical **Beer Game** framework. The study systematically compares **human decision-makers**, **rule-based robotic agents**, and **Large Language Model (LLM)–driven agents** under identical demand and structural conditions.

The project was conducted as part of the course **Intelligent Systems in Production** at **Technische Hochschule Deggendorf**, under the supervision of **Prof. Dr. Tim Weber**.

---

## Abstract
The Bullwhip Effect refers to the amplification of demand variability as orders propagate upstream in a supply chain. Using the Beer Game as an experimental platform, this study evaluates how decision-making behavior and coordination mechanisms influence supply chain stability. Simulations were conducted over a fixed 15-week horizon using a common demand pattern and four operational scenarios: baseline, information sharing, lean, and lean with information sharing. Results show that human decision-making significantly amplifies instability, while robot-based and LLM-based agents reduce demand amplification, particularly under coordinated system designs.

---

## Research Objectives
The objectives of this case study are:
- To analyze the emergence of the Bullwhip Effect in a four-echelon supply chain
- To distinguish between **structural** and **behavioral** causes of demand amplification
- To compare human, rule-based, and LLM-driven decision-making paradigms
- To evaluate the impact of information sharing and lead-time reduction
- To assess the role of intelligent systems in improving supply chain stability

---

## Beer Game Framework
The Beer Game models a serial supply chain with four stages:
- Retailer  
- Wholesaler  
- Distributor  
- Factory  

Customer demand enters at the retailer, while production occurs at the factory. Orders flow upstream and goods flow downstream, both subject to delays. Each stage operates with limited local information, creating conditions under which the Bullwhip Effect naturally emerges.

The Beer Game is rooted in system dynamics and has been widely used in both education and research to study feedback delays, decentralized decision-making, and non-linear supply chain behavior.

---

## Simulation Methodology

### Demand Pattern
All simulations use the same predefined 15-week customer demand pattern consisting of:
- A stable base demand
- A temporary high-magnitude demand spike
- Subsequent normalization  

Using a common demand input ensures that observed differences arise from decision-making behavior and system structure rather than external demand variation.

### Initial Conditions
- Identical initial inventory levels across all stages  
- Zero initial backlog  
- Deterministic shipping and information delays  

---

## Decision-Making Models

### Human-Based Simulation
Human participants control each supply chain stage and make weekly ordering decisions based solely on local information. Participants have no knowledge of future demand and limited understanding of system-wide dynamics, capturing realistic behavioral effects such as overreaction and delayed adjustment.

### Robot-Based Simulation
Rule-based robotic agents follow a deterministic inventory control policy based on target inventory levels, lead times, and backlog. This approach removes behavioral bias and provides a benchmark for structurally driven system behavior.

### LLM-Based Simulation
Large Language Model agents (Mistral-7B-Instruct) replace human decision-makers. The LLM receives structured local state information (inventory, backlog, incoming shipments, observed orders) and generates weekly orders using a fixed prompt designed to emulate bounded rationality. No learning or memory is applied across simulation steps.

---

## Operational Scenarios
Each decision-making model is evaluated under four scenarios:

1. **Baseline Scenario**  
   Shipping and information delays present.

2. **Information Sharing Scenario**  
   Information delay removed; shipping delays retained.

3. **Lean Scenario**  
   Shipping delays removed; information delay retained.

4. **Lean with Information Sharing Scenario**  
   Both shipping and information delays removed.

These scenarios isolate the effects of coordination, transparency, and physical delays on demand amplification.

---

## Results Summary
Key findings from the study include:
- Human-based simulations exhibit the strongest Bullwhip Effect, with large upstream order oscillations and slow recovery.
- Robot-based simulations demonstrate that structural delays alone are sufficient to generate instability.
- LLM-based simulations reduce behavioral amplification compared to humans but remain constrained by system structure.
- The combined lean and information-sharing scenario provides the strongest mitigation of the Bullwhip Effect across all decision-maker types.

Detailed order and backlog plots for all scenarios are provided in the appendix of the report.

---

## Repository Structure
.
├── report/
│ ├── main.tex # Full LaTeX case study report
│ ├── references.bib # Bibliography
│ └── figures/ # Figures used in the report
│
├── simulations/
│ ├── robot_simulation/ # Rule-based Beer Game implementation
│ └── llm_simulation/ # LLM-based Beer Game implementation
│
├── data/
│ ├── demand_pattern.xlsx # Customer demand data
│ └── simulation_results/ # Output data and plots
│
├── appendix/
│ ├── additional_figures/ # Supplementary plots
│ └── code_snippets/ # Supporting code
│
└── README.md

---

## Reproducibility
The simulation methodology is fully deterministic given the specified demand pattern and initial conditions. Robot-based simulations are fully reproducible. LLM-based simulations use controlled sampling parameters but may exhibit minor variability due to stochastic text generation.

---

## Limitations
- Fixed demand pattern and short simulation horizon
- Deterministic lead times and simplified supply chain structure
- No adaptive learning in LLM agents
- Cost-based performance metrics not explicitly modeled

---

## Future Work
Potential extensions of this work include:
- Stochastic and seasonal demand patterns
- Adaptive and learning-based agents (e.g., reinforcement learning)
- Cost and service-level performance evaluation
- Human–AI hybrid decision-support systems

---

## Authors
- **Doddapaneni Mohith**  
- **Chetan Reddy Konda**  

Technische Hochschule Deggendorf

---

## Acknowledgements
The authors would like to express sincere gratitude to **Prof. Dr. Tim Weber** for his guidance, critical feedback, and emphasis on system-level thinking. Additional thanks are extended to **Mr. René Höhle** and the laboratory staff of Technische Hochschule Deggendorf for technical and infrastructural support.

---

## License
This repository is intended for academic and educational use only.
