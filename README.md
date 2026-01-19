# -Bullwhip-Case-Study-using-Human-Robot-and-LLM-based-Stimulations.
This repository contains a simulation-based case study on the Bullwhip Effect using the Beer Game. It compares human decision-making, rule-based robotic agents, and large language model (LLM) agents under baseline, lean, information-sharing, and combined scenarios, with structured analysis, figures, and reproducible experiments.
# Simulation-Based Analysis of the Bullwhip Effect Using the Beer Game

## Overview
This repository contains the complete materials for a simulation-based case study analyzing the Bullwhip Effect in supply chain systems using the Beer Game. The study compares human decision-making, rule-based robotic agents, and Large Language Model (LLM)–driven agents under controlled demand conditions and multiple coordination scenarios.

The project was conducted as part of the **Intelligent Systems in Production** course at **Technische Hochschule Deggendorf**.

---

## Objectives
The main objectives of this project are:
- To analyze how the Bullwhip Effect emerges in a multi-echelon supply chain
- To compare behavioral and structural drivers of demand amplification
- To evaluate the impact of coordination mechanisms such as lean operation and information sharing
- To assess the potential of LLM-based decision-making in supply chain simulations

---

## Experimental Setup
The Beer Game models a four-stage supply chain consisting of a retailer, wholesaler, distributor, and factory. All simulations were conducted under identical experimental conditions to ensure fair comparison across decision-making paradigms.

Key setup characteristics include:
- Fixed 15-week demand horizon
- Identical customer demand pattern across all simulations
- Deterministic shipping and information delays
- Uniform initial inventory and backlog conditions

---

## Decision-Making Models
Three types of decision-makers are evaluated:

### Human-Based Simulation
Human participants make weekly ordering decisions based solely on local system information, including inventory levels, backlog, and observed incoming orders.

### Robot-Based Simulation
Rule-based agents follow a deterministic inventory control policy designed to maintain target inventory levels while accounting for lead times and backlog.

### LLM-Based Simulation
Large Language Model agents replace human decision-makers and generate weekly orders based on structured system-state information using a fixed prompt. The LLM operates without learning or memory across simulation steps.

---

## Operational Scenarios
Each decision-maker type is evaluated under four operational scenarios:

1. **Baseline Beer Game**  
   Classical structure with shipping and information delays.

2. **Information Sharing**  
   Information delay removed while shipping delays remain.

3. **Lean Scenario**  
   Shipping delays removed while information delay remains.

4. **Lean with Information Sharing**  
   Both shipping and information delays removed.

---

## Repository Structure
