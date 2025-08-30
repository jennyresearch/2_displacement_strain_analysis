# Displacement and Strain Analysis

A Python-based analysis toolkit for processing displacement data and calculating strain rates using Jupyter Notebooks. This project processes tracking statistics extracted from ImageJ to perform comprehensive displacement calculations and strain rate analysis.

## Overview

This repository contains tools and workflows for analyzing displacement fields and computing strain rates from image-based tracking data. The analysis pipeline takes ImageJ tracking output and performs advanced calculations to quantify material deformation and movement patterns.

## Features

- **Displacement Calculation**: Process tracking coordinates to compute displacement vectors
- **Strain Rate Analysis**: Calculate strain rates from displacement fields
- **Data Visualization**: Generate comprehensive plots and visualizations of results
- **Interactive Analysis**: Jupyter Notebook-based workflow for exploratory data analysis
- **Statistical Analysis**: Comprehensive statistics on displacement and strain patterns

## Prerequisites

### Required Software
- Python 3.7+
- Jupyter Notebook or JupyterLab
- ImageJ (for initial tracking data extraction)

### Python Dependencies
All required dependencies are listed in `requirements.txt`. Install them using:
```bash
pip install -r requirements.txt
```

**Core Dependencies:**
- **numpy, pandas, scipy**: Scientific computing and data manipulation
- **matplotlib, seaborn, plotly**: Data visualization and plotting
- **scikit-learn**: Machine learning algorithms for advanced analysis
- **opencv-python**: Image processing utilities
- **geopandas**: Geospatial data handling (optional)
- **jupyter**: Interactive notebook environment

## Workflow

### 1. Data Preparation
- Extract tracking statistics from ImageJ
- Export data in compatible format (CSV recommended)
- Ensure proper coordinate system and time series data

### 2. Analysis Pipeline
The analysis is performed in Jupyter Notebooks with the following steps:

1. **Data Import and Cleaning**
   - Load ImageJ tracking data
   - Handle missing values and outliers
   - Validate coordinate systems

2. **Displacement Calculation**
   - Compute displacement vectors from tracking coordinates
   - Calculate displacement magnitudes and directions
   - Temporal analysis of displacement patterns

3. **Strain Rate Analysis**
   - Derive strain tensors from displacement fields
   - Calculate principal strains and strain rates
   - Analyze spatial and temporal strain variations

4. **Visualization and Results**
   - Generate displacement field plots
   - Create strain rate visualizations
   - Export results and summary statistics

## File Structure

```
├── 2_Set1/                        # Input data from ImageJ
├── 3_Set2/                        # Input data from ImageJ
├── 4_Set3/                        # Input data from ImageJ
├── notebooks/                     # Jupyter analysis notebooks
│   ├── 01_data_preprocessing.ipynb
│   ├── 02_displacement_analysis.ipynb
│   └── 03_strain_calculation.ipynb
├── requirements.txt              # Python dependencies
└── README.md
```

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/jennyresearch/2_displacement_strain_analysis.git
   cd 2_displacement_strain_analysis
   ```

2. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

3. **Prepare your data**
   - Export tracking data from ImageJ
   - Place CSV files in the `2_Set1/` directory

4. **Run the analysis**
   - Open Jupyter Notebook
   - Start with `01_data_preprocessing.ipynb`
   - Follow the sequential notebook workflow

## Data Format

### Expected ImageJ Output Format
The analysis expects tracking data with the following columns:
- `Frame`: Time frame number
- `X`: X-coordinate position
- `Y`: Y-coordinate position
- `Track_ID`: Unique identifier for each tracked object/point

### Example Data Structure
```
Frame,Track_ID,X,Y
1,1,100.5,200.3
2,1,101.2,201.1
3,1,102.0,202.5
...
```

## Analysis Methods

### Displacement Calculation
- **Vector Analysis**: Compute displacement vectors between consecutive frames
- **Trajectory Analysis**: Analyze complete movement paths
- **Velocity Estimation**: Calculate instantaneous and average velocities

### Strain Rate Calculation
- **Gradient-Based Methods**: Use spatial gradients of displacement fields
- **Finite Element Approach**: Apply finite element methods for strain calculation
- **Principal Strain Analysis**: Identify maximum and minimum strain directions

## Visualization Outputs

- Displacement vector fields
- Strain rate heatmaps
- Temporal evolution plots
- Statistical distribution plots
- Interactive 3D visualizations (when applicable)

## Applications

This analysis toolkit is suitable for:
- Material science deformation studies
- Biological tissue mechanics
- Geophysical deformation analysis
- Fluid dynamics particle tracking
- Any application requiring displacement and strain quantification

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-analysis`)
3. Commit your changes (`git commit -am 'Add new analysis method'`)
4. Push to the branch (`git push origin feature/new-analysis`)
5. Create a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- ImageJ community for tracking tools and documentation
- Scientific Python ecosystem (NumPy, SciPy, Matplotlib)
- Jupyter Project for interactive computing platform
