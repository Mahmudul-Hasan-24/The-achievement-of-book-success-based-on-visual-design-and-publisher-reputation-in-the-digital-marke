"""# 🧠 Opinion Dynamics Under External Shocks – An Agent-Based Modeling Approach

## 📌 Project Overview
This project models **opinion dynamics** in a population using an **agent-based simulation**.  
The focus is on understanding how **external shocks** (such as policy changes or major events) affect:
- Time to reach consensus
- Stability of opinions
- Level of polarization in the network


---

## 🗂 Repository Structure
├── notebooks/
│ └── opinion_dynamics.ipynb # Main simulation notebook
├── report.pdf # Detailed report with methodology and results
├── poster.pdf # Visual summary of the project
└── requirements.txt # Python dependencies



---


## 🧠 Model Description

### Agents
- Each agent represents an individual with a binary opinion (0 or 1).

### Network Topology
- **Small-world network** generated using the Watts–Strogatz model to mimic real-world social networks.

### Dynamics
At each time step:
1. A random agent observes a neighbor.
2. The agent adopts the neighbor's opinion with probability `p`.
3. At predefined intervals, an **external shock** flips the opinions of a subset of agents.

### Observables
- **Consensus Time** – number of steps until all agents share the same opinion.
- **Polarization** – fraction of agents holding each opinion over time.
- **Stability** – effect of repeated shocks on long-term opinion distribution.

---


## 📊 Key Results

| Scenario             | Finding |
|--------------------|--------|
| No External Shock  | Consensus is typically reached quickly (few thousand steps). |
| Small Shocks       | Delay consensus and keep diversity longer. |
| Large/Frequent Shocks | Can prevent consensus entirely, leading to oscillating majority opinion. |


---


## 🛠 How to Run Locally

### 1. Clone this repository
```bash
git clone https://github.com/Mahmudul-Hasan-24/Foundation-of-Computational-Social-System.git
cd Foundation-of-Computational-Social-System
2. Create and activate a virtual environment
bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\\Scripts\\activate
3. Install dependencies
bash
pip install -r requirements.txt
4. Run the notebook
bash

jupyter notebook notebooks/opinion_dynamics.ipynb
📦 Dependencies
networkx – network generation

numpy – numerical computations

matplotlib – plotting

jupyter – notebook interface

🚀 Future Extensions
Implement multi-opinion models (more than two states).

Test effect of network topology variations (scale-free, random).

Add adaptive networks where connections change over time.

📜 License
This project is licensed under the MIT License – see LICENSE for details.

👤 Author
Mahmudul Hasan
Master’s of Computational Social System (Business Analytics) at  Technical University of Graz and University of Graz
