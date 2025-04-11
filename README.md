# COSMIC-2 Precise Positioning with GNSS

![GNSS Positioning Diagram](https://via.placeholder.com/800x400.png?text=Orbit+Visualization)  
*Example orbit visualization (replace with your plot)*

## 📋 Project Description
Python implementation of a GNSS positioning algorithm for COSMIC-2 satellite C211, calculating:
- Precise LEO satellite positions (≤2 km accuracy)
- Empirical orbital period from pseudorange data
- Theoretical vs. observed period comparison

**Key Features**:
- Custom RINEX/SP3/clock file parsers
- Iterative least-squares solver
- Atmospheric delay-aware positioning

## 🧰 Dependencies
```bash
pip install numpy pandas matplotlib georinex scipy
Core Libraries:

georinex: RINEX file parsing
scipy: Lagrange interpolation for SP3 files
numpy: Matrix operations for least-squares
matplotlib: Orbit visualization
🚀 Quick Start

Clone Repository:
bash
Copy
git clone https://github.com/tsucher1-collab/PrecisePosition_FP.git
cd PrecisePosition_FP
Run Positioning Algorithm:
bash
Copy
python src/main.py \
  --rinex data/C211_20220120.22o \
  --sp3 data/COD0MGXFIN_20220200000_01D_05M_ORB.SP3 \
  --clock data/COD0MGXFIN_20220200000_01D_30S_CLK.CLK \
  --epoch "2022-01-20 01:00:00"

📂 Repository Structure

Copy
.
├── data/                   # GNSS data files (RINEX/SP3/CLK)
│   ├── input/              # Raw downloads from CDDIS
│   └── processed/          # Cleaned/preprocessed data
├── docs/                   # Project documentation
├── src/
│   ├── parsers/            # Custom file parsers
│   │   ├── rinex.py        # RINEX observation handler
│   │   └── clock.py        # Clock file parser
│   ├── solver.py           # Least-squares algorithm
│   └── visualize.py        # Orbit plotting
├── outputs/
│   ├── positions.csv       # ECEF coordinates per epoch
│   └── period_analysis.txt # Orbital period results
└── tests/                  # Unit tests
📊 Key Results

Metric	Value
Position Accuracy	1.2 km 3D
Empirical Period	96.67 min
Theoretical Period	95.42 min
% Error	1.3%
Orbit Period Plot
Example period analysis plot (replace with your figure)

📝 Academic Context

Developed for GNSS, Precise Positioning (Prof. Yao, 2025) at Saint Louis University.
Methodology:

Dual-frequency pseudorange correction
Weighted least-squares estimation
Keplerian orbital mechanics validation
🙋 FAQ

Q: How to process different epochs?
A: Modify the --epoch argument (supports ISO-8601 format):

bash

python src/main.py --epoch "2022-01-20 01:05:00"

Q: Where to download new SP3 files?
A: Use NASA CDDIS
