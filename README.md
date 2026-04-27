# 🧠 Simulation-to-Kernel Gap in DDQN-Based CPU Scheduling

An analytical literature review exploring the gap between simulation performance and real-world deployment of Deep Reinforcement Learning (DDQN) based CPU schedulers.

---

## 📌 Overview

While multiple studies report 20–30% improvements in CPU scheduling performance using DDQN, none have been deployed in production operating systems.

This work investigates **why this gap exists**, focusing on system-level constraints rather than algorithmic performance.

---

## 🎯 Objective

- Understand limitations of DRL-based schedulers in real OS environments  
- Analyze differences between simulation and kernel-level execution  
- Identify practical barriers to deployment  
- Propose structured evaluation frameworks  

---

## 📚 Methodology

- Systematic review of **45+ research papers (2006–2026)**  
- Comparative analysis of:
  - Classical schedulers (CFS, MLFQ)
  - DRL-based schedulers (DQN, DDQN, PPO, etc.)
- Evaluation based on **deployment feasibility, not just performance metrics**

---

## 🔍 Key Contributions

### 1. Deployment Readiness Score (DRS)
A framework to assess whether a scheduler is viable for real-world deployment across criteria such as:
- Latency constraints  
- Determinism  
- Hardware compatibility  
- Real-world validation  

---

### 2. Latency Decomposition Model (T₁–T₄)

Breaks scheduling overhead into:
- State collection  
- Inference time  
- Kernel overhead  
- Worst-case latency  

---

### 3. Three-Body Constraint Model

Defines trade-offs between:
- Decision latency  
- State observability  
- Policy complexity  

---

### 4. DDQN Framework (Conceptual)

- Extended state representation  
- Fairness-aware reward function  
- Evaluated using simulation tools (SimPy)  

---

## 📊 Key Findings

- Classical schedulers are **deployment-ready (5/6)**  
- DRL schedulers score **0/6 in feasibility**  
- Simulation results fail to capture:
  - Kernel constraints  
  - Real-time latency requirements  
  - Hardware variability  

---

## ⚠️ Core Insight

> The challenge of RL-based scheduling is not purely algorithmic—it is fundamentally a **systems engineering problem**.

---

## 🛠️ Tools & Concepts

- Python, SimPy  
- Reinforcement Learning (DDQN)  
- Operating Systems Scheduling  
- Performance Modeling  

---

## 🚀 Future Scope

- Kernel-level experimentation (sched_ext)  
- Real-world latency validation  
- Integration with production systems  

---

## 👩‍💻 Author

**Sinchana K**  
B.Tech AI & ML, PES University  

---

## ⭐ Note

This work is a **literature-driven analysis** and does not claim real-world deployment results. It focuses on bridging the gap between theory and practical systems.
