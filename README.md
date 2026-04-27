# 🧠 Simulation-to-Kernel Gap in DDQN-Based CPU Scheduling

An IEEE-style research study analyzing why Deep Reinforcement Learning (DDQN) schedulers, despite strong simulation performance, have not been deployed in real-world operating system kernels.

---

## 📌 Overview

Recent research reports significant improvements (20–30%) in CPU scheduling performance using DDQN-based approaches. However, none of these methods have been adopted in production operating systems.

This study investigates **why this gap exists**, shifting focus from algorithm performance to **deployment feasibility**.

---

## 🎯 Objectives

- Analyze the gap between simulation results and real-world deployment  
- Identify technical and architectural barriers in OS-level scheduling  
- Evaluate feasibility of DRL-based schedulers in kernel environments  
- Propose structured frameworks to assess deployment readiness  

---

## 🔍 Key Contributions

- 📊 **Deployment Readiness Score (DRS)**  
  A metric to evaluate whether a scheduling approach is suitable for real-world deployment  

- ⚙️ **Latency Decomposition Model (T₁–T₄)**  
  Breaks down scheduling overhead into:
  - State collection  
  - Inference time  
  - Kernel overhead  
  - Worst-case latency variance  

- ⚖️ **Three-Body Constraint Model**  
  Captures trade-offs between:
  - Decision latency  
  - State observability  
  - Policy complexity  

- 🧠 **DDQN Scheduling Framework (Simulation-Based)**  
  - Extended state representation  
  - Fairness-aware reward function  
  - Evaluated using SimPy  

---

## 📊 Key Findings

- Classical schedulers (e.g., CFS, MLFQ) are **deployment-ready (5/6 score)**  
- DRL-based schedulers score **0/6 in deployment feasibility**  
- Simulation results fail to capture:
  - Kernel-level latency constraints  
  - Hardware variability  
  - Safety and determinism requirements  

---

## ⚠️ Core Insight

> Deep Reinforcement Learning scheduling is not just an AI problem — it is a **real-time systems engineering problem**.

---

## 🛠️ Methodology

- Systematic review of **45+ research papers (2006–2026)**  
- Comparative analysis of classical vs DRL schedulers  
- Simulation using **SimPy** for validation  
- Analytical modeling of kernel constraints  



---

## 🔧 Tools & Technologies

- Python  
- SimPy  
- Deep Reinforcement Learning (DDQN)  
- Operating Systems Concepts  

---

## 🚀 Future Work

- Kernel-level implementation using sched_ext (Linux)  
- Real-world latency measurement  
- Formal fairness guarantees  
- Cross-platform scheduler generalization  

---

## 👩‍💻 Author

**Sinchana K**  
B.Tech AI & ML, PES University  
🔗 GitHub: https://github.com/sin-h43  
🔗 LinkedIn: https://linkedin.com/in/sinchana-k06  

---

## ⭐ Note

This work is simulation-based and aims to bridge the gap between theoretical performance and real-world system constraints.
