# Btech_Project
# IoT Data Analytics Using Deep Reinforcement Learning (DRL)

## 📌 Project Overview
This project focuses on **intelligent task offloading in IoT-enabled UAV networks** using **Deep Reinforcement Learning (DRL)**.  
The goal is to **minimize execution delay and energy consumption** by dynamically deciding where an IoT task should be executed.

Possible execution locations:
- Local IoT Device
- Master UAV
- Slave UAV
- Cloud Server

A **DRL agent (DQN-based)** learns optimal offloading decisions over time using a **negative reward mechanism**.

---

## 🎯 Problem Statement
IoT devices have limited computation and energy resources.  
Offloading tasks to UAVs or cloud servers can reduce computation load, but improper decisions may increase delay and energy consumption.

**Objective:**  
Design a DRL-based intelligent task offloading framework that selects the best execution node while minimizing:
- ⏱️ Execution Time  
- 🔋 Energy Consumption  

---

## 🧠 System Architecture
- **IoT Devices** generate computational tasks
- **Master UAV** acts as the controller
- **Slave UAVs** assist in computation
- **Cloud Server** handles high-compute tasks
- **DRL Agent** decides optimal offloading

---

## ⚙️ Modules Description

### 🔹 Module 1: Network Model & Problem Formulation
Defines:
- Master UAV
- IoT Devices
- Slave UAVs
- Cloud Server  
Execution modes include:
- Local execution
- UAV execution
- Cloud execution

---

### 🔹 Module 2: Classification Algorithm
A classification model is used to **improve decision accuracy** by pre-analyzing task characteristics before DRL-based offloading.

---

### 🔹 Module 3: DRL-Based Task Offloading
A **Deep Q-Network (DQN)** agent is used.

**Working Steps:**
1. Initialize agent
2. Observe environment state
3. Select action (offload location)
4. Receive reward (based on delay & energy)
5. Store experience
6. Train neural network
7. Reduce exploration (epsilon decay)
8. Improve policy over episodes

---

### 🔹 Module 4: Numerical Analysis
Performance evaluation through:
- Training phase
- Testing phase
- Multiple enhancement phases

---

## 🎁 Reward Mechanism
A **negative reward system** is used.

**Why negative rewards?**
- Encourages minimizing delay & energy
- Penalizes inefficient decisions
- Stabilizes learning

| Scenario | Reward |
|--------|--------|
| High delay & energy | Large negative |
| Low delay & energy | Small negative |

---

## 📊 Experimental Results

### Phase-wise Improvements
- **Phase 1:** Basic DRL agent
- **Phase 2:** DRL + Classification Algorithm
- **Phase 3:** Enhanced Reward Shaping
- **Phase 4:** Micro-deadline check

**Training:**  
- Epsilon (ε) decreases from `1.0 → 0.01`

**Testing:**  
- Epsilon (ε) = `0` (pure exploitation)

Each phase shows **improved stability and performance**.

---

## 🧪 Technologies Used
- Python
- Deep Reinforcement Learning (DQN)
- IoT Network Modeling
- UAV-based Computation
- Jupyter Notebook

---

## 📁 Repository Structure
