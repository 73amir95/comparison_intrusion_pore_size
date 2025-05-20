# Pore Size and Intrusion Analysis

## Overview
This project contains a Python script for analyzing pore size distribution data from the file `Cum. Intrusion vs. Pore Size.xlsx`. The script performs data loading, cleaning, statistical analysis, and visualization to explore the relationship between pore size diameter and intrusion measurements (cumulative and log differential).

## Dependencies
To run the script, ensure you have the following Python libraries installed:
- `numpy`: For numerical computations
- `pandas`: For data manipulation and analysis
- `matplotlib`: For creating plots
- `seaborn`: For enhanced statistical visualizations

Install the dependencies using pip:
```bash
pip install numpy pandas matplotlib seaborn
```

## Data
The script uses the dataset `Cum. Intrusion vs. Pore Size.xlsx`, which contains the following columns:
- `Pore size Diameter (µm)`: Pore size in micrometers
- `Cumulative Intrusion (mL/g)`: Cumulative intrusion volume
- `Log Differential Intrusion (mL/g)`: Log differential intrusion volume
- An unnamed column (dropped during processing)

## Script Functionality
The script performs the following tasks:
1. **Data Loading and Cleaning**:
   - Loads the Excel file using `pandas`.
   - Skips the first row to handle headers correctly.
   - Drops an unnecessary column (index 2).
   - Displays basic data information (`head`, `info`, `describe`).

2. **Data Analysis**:
   - Calculates the sum of differences between `Cumulative Intrusion` and `Log Differential Intrusion`.
   - Computes Spearman correlation coefficients for the dataset.
   - Sorts correlations for `Pore size Diameter (µm)`.

3. **Visualizations**:
   - Creates joint plots for `Pore size Diameter (µm)` vs. `Cumulative Intrusion` and `Log Differential Intrusion`.
   - Generates a pair plot for all variables.
   - Plots `Cumulative Intrusion` vs. `Pore size Diameter (µm)`.
   - Plots `Log Differential Intrusion` vs. `Pore size Diameter (µm)` with a logarithmic x-axis scale.
   - Creates a heatmap of Spearman correlations.
   - Saves visualizations as PNG files:
     - `pairplot_intrusion vs. pore size.png`
     - `pore_size vs. cum. intrusion.png`
     - `pore_size vs. log. diff. intrusion.png`
     - `heatmap_cum. intrusion vs. pore size.png`

## Usage
1. Ensure the Excel file `Cum. Intrusion vs. Pore Size.xlsx` is in the same directory as the script.
2. Run the script in a Python environment (e.g., Jupyter Notebook or a Python IDE).
3. The script will generate and save the visualizations as PNG files in the working directory.

Example command to run the script (if saved as `analysis.py`):
```bash
python analysis.py
```

## Notes
- The script assumes the Excel file has a consistent structure. Verify the file format if errors occur.
- The `%matplotlib inline` command is included for Jupyter Notebook compatibility. Remove it if running in a different environment.
- Visualizations use specific figure sizes and styles for clarity, which can be modified as needed.

## Output Files
- `pairplot_intrusion vs. pore size.png`: Pair plot of all variables.
- `pore_size vs. cum. intrusion.png`: Plot of cumulative intrusion vs. pore size.
- `pore_size vs. log. diff. intrusion.png`: Plot of log differential intrusion vs. pore size (log scale).
- `heatmap_cum. intrusion vs. pore size.png`: Heatmap of Spearman correlations.