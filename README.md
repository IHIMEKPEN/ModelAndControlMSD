# Digital Twin Modeling and Optimal Control of Spring-Mass Systems Using Reservoir Computing

## Abstract

Soft-bodied robots present unique modeling and control challenges due to their highly nonlinear dynamics and complex interactions with the environment. We demonstrate that Reservoir Computing (RC) with Echo State Networks (ESN) can effectively create digital twins of spring-mass systems for soft robotics applications, achieving 0.435% MAPE for digital twin modeling and 2.867% MAPE for optimal control on a 20-node 54-spring system. Our approach significantly outperforms traditional deep learning methods while maintaining computational efficiency suitable for real-time applications. This work bridges nonlinear control theory with physics-aware machine learning, providing a practical solution for soft robotics control with training times under 5 seconds, enabling real-time deployment in dynamic environments.

## AML Journal Submission

This repository accompanies our submission to the **Applied Machine Learning (AML) Journal**. The code implements Reservoir Computing (RC) with Echo State Networks (ESN) for digital twin modeling and optimal control of spring-mass systems representing soft robotics applications.

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
├── 📁 data/                    # Sample data and data loading scripts
│   ├── README.md              # Data description and access instructions
│   └── sample_data.csv        # Sample spring-mass system data
├── 📁 src/                     # Source code
│   ├── __init__.py
│   ├── models/                # Reservoir Computing models
│   │   ├── __init__.py
│   │   ├── esn.py            # Echo State Network implementation
│   │   └── reservoir.py      # Reservoir Computing base class
│   ├── simulation/            # Spring-mass system simulation
│   │   ├── __init__.py
│   │   ├── spring_mass.py    # Spring-mass system dynamics
│   │   └── controller.py     # Control mechanisms
│   └── utils/                 # Utility functions
│       ├── __init__.py
│       ├── data_processing.py # Data preprocessing
│       └── visualization.py   # Plotting utilities
├── 📁 notebooks/              # Jupyter notebooks for analysis
│   ├── 01_data_exploration.ipynb
│   ├── 02_model_training.ipynb
│   ├── 03_control_evaluation.ipynb
│   └── 04_results_analysis.ipynb
├── 📁 results/                # Output results and figures
│   ├── models/               # Trained model files
│   └── plots/               # Generated figures
│       ├── fig1.png
│       └── fig2.png
├── 📁 scripts/               # Training and evaluation scripts
│   ├── train_model.py       # Model training script
│   ├── evaluate_control.py  # Control evaluation script
│   └── generate_plots.py    # Plot generation script
├── 📁 tests/                # Unit tests
│   ├── __init__.py
│   ├── test_models.py
│   └── test_simulation.py
└── 📄 CITATION.cff          # Citation information
```

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

## Quick Start

### Running the Simulation

```bash
# Train the Reservoir Computing model
python scripts/train_model.py --data_path data/sample_data.csv --output_dir results/models/

# Evaluate control performance
python scripts/evaluate_control.py --model_path results/models/esn_model.pkl

# Generate plots
python scripts/generate_plots.py --results_dir results/plots/
```

### Jupyter Notebooks

1. Start Jupyter:
   ```bash
   jupyter lab
   ```

2. Open notebooks in order:
   - `notebooks/01_data_exploration.ipynb` - Data analysis
   - `notebooks/02_model_training.ipynb` - Model training
   - `notebooks/03_control_evaluation.ipynb` - Control evaluation
   - `notebooks/04_results_analysis.ipynb` - Results analysis

## Data

The `data/` directory contains sample spring-mass system data. For the full dataset used in our experiments, please refer to the data README file.

## Key Results

- **Digital Twin Modeling**: 0.435% MAPE on 20-node spring-mass system
- **Optimal Control**: 2.867% MAPE for control performance
- **Training Time**: Under 5 seconds for real-time deployment
- **System Size**: 20 nodes, 54 springs

## Citation

If you use this code in your research, please cite our paper:

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

For questions about this implementation, please contact:
- **Osemudiamen Andrew Ihimekpen**: oihimekpen@pvamu.edu
- **Jovan Cain**: jcain5@pvamu.edu

## Acknowledgments

This work was supported by the CREDIT Center at Prairie View A&M University and the U.S. Army Research Laboratory. 