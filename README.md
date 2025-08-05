# Digital Twin Modeling and Optimal Control of Spring-Mass Systems Using Reservoir Computing

## Abstract

Soft-bodied robots present unique modeling and control challenges due to their highly nonlinear dynamics and complex interactions with the environment. We demonstrate that Reservoir Computing (RC) with Echo State Networks (ESN) can effectively create digital twins of spring-mass systems for soft robotics applications, achieving 0.435% MAPE for digital twin modeling and 2.867% MAPE for optimal control on a 20-node 54-spring system. Our approach significantly outperforms traditional deep learning methods while maintaining computational efficiency suitable for real-time applications. This work bridges nonlinear control theory with physics-aware machine learning, providing a practical solution for soft robotics control with training times under 5 seconds, enabling real-time deployment in dynamic environments.

## AML Journal Submission

This repository contains the **data portion** of our submission to the **Applied Machine Learning (AML) Journal**. The data supports research on Reservoir Computing (RC) with Echo State Networks (ESN) for digital twin modeling and optimal control of spring-mass systems representing soft robotics applications.

## Authors

- **Jovan Cain** - Department of Electrical and Computer Engineering and CREDIT Center, Prairie View A&M University
- **Osemudiamen Andrew Ihimekpen** - Department of Electrical and Computer Engineering and CREDIT Center, Prairie View A&M University  
- **Xiangfang Li** - Department of Electrical and Computer Engineering and CREDIT Center, Prairie View A&M University
- **Mulugeta Haile** - U.S. Army Research Laboratory
- **Lijun Qian** - Department of Electrical and Computer Engineering and CREDIT Center, Prairie View A&M University

## Project Structure

```
📁 ModelAndControlMSD/
├── README.md                    # This file
├── LICENSE                      # MIT License
├── requirements.txt             # Python dependencies
├── .gitignore                  # Git ignore file
├── 📁 data/                    # Research data and datasets
│   ├── README.md              # Data description and access instructions
│   ├── 📁 node5spring9/       # 5-node, 9-spring system data
│   │   └── 1/dynamic/
│   │       ├── control.csv    # Control signals data
│   │       ├── speed.csv      # Node velocities data
│   │       ├── pos.csv        # Node positions data
│   │       └── acc.csv        # Node accelerations data
│   ├── 📁 node10spring24 v1=4 v2=2/  # 10-node, 24-spring system data
│   │   └── 1/dynamic/
│   │       ├── control.csv    # Control signals data
│   │       ├── speed.csv      # Node velocities data
│   │       ├── pos.csv        # Node positions data
│   │       └── acc.csv        # Node accelerations data
│   └── 📁 plots/              # Generated visualization plots
│       ├── 📁 plots_2000_timesteps/
│       │   └── 📁 node5spring9/dynamic/
│       │       ├── node_1_x_position.png
│       │       ├── node_1_y_position.png
│       │       ├── node_1_x_speed.png
│       │       ├── node_1_y_speed.png
│       │       ├── node_1_x_acc.png
│       │       ├── node_1_y_acc.png
│       │       ├── ... (similar files for nodes 2-5)
│       │       ├── control_spring_length_1.png
│       │       ├── control_spring_length_2.png
│       │       ├── ... (similar files for springs 3-9)
│       └── 📁 plots_20000_timesteps/
│           └── (similar structure for longer simulations)
└── 📄 CITATION.cff          # Citation information
```

## Data Description

This repository contains the datasets used in our research on digital twin modeling and optimal control of spring-mass systems. The data includes:

### Available Datasets

1. **5-Node, 9-Spring System** (`node5spring9/`)
   - Position data (pos.csv) - 17MB
   - Velocity data (speed.csv) - 18MB  
   - Acceleration data (acc.csv) - 18MB
   - Control signals (control.csv) - 16MB

2. **10-Node, 24-Spring System** (`node10spring24/`)
   - Position data (pos.csv) - 32MB
   - Velocity data (speed.csv) - 37MB
   - Acceleration data (acc.csv) - 36MB
   - Control signals (control.csv) - 43MB

### Data Format

Each dataset contains time series data with the following structure:
- **Position data**: Node positions in x and y coordinates over time
- **Velocity data**: Node velocities in x and y directions over time
- **Acceleration data**: Node accelerations in x and y directions over time
- **Control data**: Applied control signals and spring dynamics over time

### Visualization Plots

The repository includes comprehensive visualization plots for:
- **Node dynamics**: Position, velocity, and acceleration plots for each node
- **Spring control**: Spring length and force dynamics for each spring
- **Time scales**: Both 2000 and 20000 timestep simulations

### Data Access

The complete dataset used in our experiments contains:
- **5 and 10-node spring-mass system simulations** (referenced in paper)
- **9 and 24 springs with nonlinear dynamics**
- **Time series data for position, velocity, and acceleration**


For access to the full 20-node dataset used in our experiments, please contact the authors as described in the data README file.

## Environment Setup

### Prerequisites

- Python 3.8+
- pip or conda

### Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/IHIMEKPEN/ModelAndControlMSD.git
   cd ModelAndControlMSD
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

## Data Access

### Available Data

The `data/` directory contains two complete spring-mass system datasets:
- **5-node, 9-spring system** with full dynamic simulation data
- **10-node, 24-spring system** with comprehensive control and response data

### Full Dataset

For access to the complete 20-node, 54-spring dataset used in our experiments, please refer to the data README file in the `data/` directory or contact the authors.

## Data Analysis

### Jupyter Notebooks

1. Start Jupyter:
   ```bash
   jupyter lab
   ```

2. Open notebooks in order:
   - `notebooks/01_data_exploration.ipynb` - Initial data exploration
   - `notebooks/02_data_analysis.ipynb` - Detailed data analysis
   - `notebooks/03_results_visualization.ipynb` - Results visualization

## Key Results

- **Digital Twin Modeling**: 0.435% MAPE on 20-node spring-mass system
- **Optimal Control**: 2.867% MAPE for control performance
- **Training Time**: Under 5 seconds for real-time deployment
- **System Size**: 20 nodes, 54 springs

## Citation

If you use this data in your research, please cite our paper:

```bibtex
@article{cain2024digital,
  title={Digital Twin Modeling and Optimal Control of Spring-Mass Systems Using Reservoir Computing},
  author={Cain, Jovan and Ihimekpen, Osemudiamen Andrew and Li, Xiangfang and Haile, Mulugeta and Qian, Lijun},
  journal={Applied Machine Learning},
  year={2024}
}
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

For questions about this data or research, please contact:
- **Osemudiamen Andrew Ihimekpen**: oihimekpen@pvamu.edu
- **Jovan Cain**: jcain5@pvamu.edu

## Acknowledgments

This work was supported by the CREDIT Center at Prairie View A&M University and the U.S. Army Research Laboratory. 