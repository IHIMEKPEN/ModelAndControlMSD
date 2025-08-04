# Data Directory

This directory contains sample data and instructions for accessing the full dataset used in our Reservoir Computing experiments.

## Sample Data

- `sample_data.csv` - Sample spring-mass system data for testing the implementation

## Full Dataset Access

The complete dataset used in our experiments contains:

- **20-node spring-mass system simulations**
- **54 springs with nonlinear dynamics**
- **Time series data for position, velocity, and acceleration**
- **Control signals and system responses**
- **Training and validation splits**

### Data Format

The dataset includes the following columns:
- `timestamp` - Time step
- `node_id` - Node identifier (1-20)
- `x_position`, `y_position` - Node positions
- `x_velocity`, `y_velocity` - Node velocities  
- `x_acceleration`, `y_acceleration` - Node accelerations
- `spring_id` - Spring identifier
- `spring_length` - Current spring length
- `spring_force` - Spring force magnitude
- `control_signal` - Applied control signal

### Access Instructions

Due to size constraints, the full dataset is hosted externally. Please contact the authors for access:

- **Osemudiamen Andrew Ihimekpen**: oihimekpen@pvamu.edu
- **Jovan Cain**: jcain5@pvamu.edu

Alternatively, you can generate synthetic data using the provided simulation scripts in `src/simulation/`.

## Data Generation

To generate your own spring-mass system data:

```python
from src.simulation.spring_mass import SpringMassSystem
from src.utils.data_processing import generate_dataset

# Create system
system = SpringMassSystem(n_nodes=20, n_springs=54)

# Generate dataset
data = generate_dataset(system, duration=100, dt=0.01)
data.to_csv('data/generated_data.csv', index=False)
```

## Citation

If you use this dataset in your research, please cite our paper:

```bibtex
@article{cain2024digital,
  title={Digital Twin Modeling and Optimal Control of Spring-Mass Systems Using Reservoir Computing},
  author={Cain, Jovan and Ihimekpen, Osemudiamen Andrew and Li, Xiangfang and Haile, Mulugeta and Qian, Lijun},
  journal={Applied Machine Learning},
  year={2024}
}
``` 