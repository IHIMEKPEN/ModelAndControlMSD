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
│   ├── sample_data.csv        # Sample spring-mass system data
│   ├── training_data/         # Training datasets
│   ├── validation_data/       # Validation datasets
│   └── test_data/            # Test datasets
├── 📁 results/                # Output results and figures
│   ├── models/               # Trained model files (if available)
│   └── plots/               # Generated figures
│       ├── fig1.png
│       └── fig2.png
├── 📁 notebooks/              # Jupyter notebooks for data analysis
│   ├── 01_data_exploration.ipynb
│   ├── 02_data_analysis.ipynb
│   └── 03_results_visualization.ipynb
└── 📄 CITATION.cff          # Citation information
```

## Data Description

This repository contains the datasets used in our research on digital twin modeling and optimal control of spring-mass systems. The data includes:

- **Spring-mass system simulation data** from 20-node, 54-spring configurations
- **Training, validation, and test datasets** for Reservoir Computing models
- **Control performance metrics** and evaluation data
- **Visualization outputs** and analysis results

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

### Sample Data

The `data/` directory contains sample spring-mass system data that can be used for initial exploration and testing.

### Full Dataset

For access to the complete dataset used in our experiments, please refer to the data README file in the `data/` directory.

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