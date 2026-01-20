Simulation-Based Study of the Bullwhip Effect
============================================

Project Title:
--------------
Simulation-Based Study of the Bullwhip Effect Using Human, Rule-Based Robot, 
and LLM-Driven Beer Game Models

Course:
-------
Case Study – Intelligent Systems in Production

Supervisor:
-----------
Prof. Dr. Tim Weber

Authors:
--------
Doddapaneni Mohith (Matriculation No: 12503701)
Chetan Chandra Konda (Matriculation No: 12504278)

Institution:
------------
Technische Hochschule Deggendorf

Date:
-----
20 January 2026


--------------------------------------------------
1. Project Overview
--------------------------------------------------
This project investigates the bullwhip effect in a four-echelon supply chain
using the classical Beer Game framework. The study compares three different
decision-making paradigms:

1. Human-based decision-making
2. Rule-based robot (algorithmic) decision-making
3. Large Language Model (LLM)-driven decision-making

All simulations are conducted under identical demand conditions and across
multiple operational scenarios to analyze demand amplification, backlog
propagation, and system stability.


--------------------------------------------------
2. Objectives
--------------------------------------------------
- To analyze how the bullwhip effect emerges in supply chains
- To compare behavioral, algorithmic, and AI-based decision-makers
- To study the impact of coordination mechanisms such as:
  - Information sharing
  - Lean (reduced lead time) operations
- To evaluate how system design influences supply chain stability


--------------------------------------------------
3. Operational Scenarios
--------------------------------------------------
The following scenarios are evaluated for all decision-maker types:

1. Baseline Beer Game
   - Shipping delay present
   - No information sharing

2. Information Sharing
   - Shipping delay present
   - Order information shared upstream

3. Lean Scenario
   - Shipping delay removed
   - No information sharing

4. Lean + Information Sharing
   - Shipping delay removed
   - Order information shared


--------------------------------------------------
4. Repository Structure
--------------------------------------------------
/report/
  - Final LaTeX source (.tex)
  - Compiled PDF report

/code/
  - Robot-based Beer Game simulation (Python)
  - LLM-based Beer Game simulation (Python)

/results/
  - Generated Excel files for each scenario
  - Order and backlog plots

/images/
  - Demand pattern
  - Beer Game architecture
  - Result plots for human, robot, and LLM simulations

README.txt



--------------------------------------------------
5. Simulation Implementation
--------------------------------------------------
- Simulation Horizon: 15 weeks
- Supply Chain Stages:
  - Retailer
  - Wholesaler
  - Distributor
  - Factory

Robot-Based Simulation:
-----------------------
Uses a base-stock inventory control policy with fixed target inventory levels.
Orders are computed deterministically based on inventory position.

LLM-Based Simulation:
---------------------
Uses a Mistral-7B-Instruct model acting as a boundedly rational agent.
The LLM receives only local state information and does not learn across weeks.


--------------------------------------------------
6. Key Findings
--------------------------------------------------
- The bullwhip effect is primarily driven by system-level delays
- Human decision-makers amplify instability through overreaction
- Robot-based agents produce the most stable behavior
- LLM-based agents consistently outperform humans but do not fully
  match robot performance
- Combined lean and information-sharing scenarios minimize demand amplification


--------------------------------------------------
7. Tools and Technologies
--------------------------------------------------
- Python 3
- Pandas
- Matplotlib
- Transformers (Hugging Face)
- Mistral-7B-Instruct
- LaTeX (report preparation)


--------------------------------------------------
8. How to Run the Simulations
--------------------------------------------------
1. Install required Python dependencies
2. Run the robot-based simulation script
3. Run the LLM-based simulation script in a GPU-enabled environment
4. Generated Excel files will be saved automatically


--------------------------------------------------
9. Notes
--------------------------------------------------
- The Beer Game model is a simplified representation of real supply chains
- Cost-based performance metrics are not included
- Results focus on order and backlog dynamics


--------------------------------------------------
10. Acknowledgements
--------------------------------------------------
The authors sincerely thank Prof. Dr. Tim Weber for his guidance and feedback
throughout the project. Special thanks to Mr. René Höhle and the laboratory
staff at Technische Hochschule Deggendorf for their technical support.

