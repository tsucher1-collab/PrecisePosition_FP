# COSMIC-2 (C211) Precise Positioning with GNSS



📂 **REPOSITORY INFORMATION**

Data folder holds RINEX (.22O), SP3(.SP3), and CLOCK(.CLK) files (among other things)

**src_code1a.ipynb --> source code for Question 1**

**q2a --> source code for Question 2**


## 📋 Project Description
Python implementation of a GNSS positioning algorithm for COSMIC-2 satellite C211, calculating:
- Precise LEO satellite positions (≤2 km accuracy)
- Empirical orbital period from pseudorange data
- Theoretical vs. observed period comparison



📊 Key Results


Position Accuracy	1.2 km 3D
Empirical Period	96.67 min
Theoretical Period	95.42 min
% Error	1.3%
Orbit Period Plot


📝 Academic Context

Developed for GNSS, Precise Positioning (Prof. Yao, 2025) at Saint Louis University.
Methodology:

Dual-frequency pseudorange correction
Weighted least-squares estimation
Keplerian orbital mechanics validation

🙋 FAQ


Q: Where to download new SP3 files?
A: Use NASA CDDIS
