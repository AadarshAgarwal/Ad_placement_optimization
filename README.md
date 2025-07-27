# Ad Placement Optimization - Multi-Armed Bandit Transitions

This repository contains a Jupyter notebook, `MAB_TRANSITIONS.ipynb`, that implements a Contextual Multi-Armed Bandit (MAB) algorithm to optimize ad placements based on user transitions between different app screens. The approach leverages contextual information (such as the day of the week) to dynamically select the best ad placement strategy, aiming to maximize ad clicks.

## Contents

- `MAB_TRANSITIONS.ipynb` - The main notebook containing:
  - Data loading and preprocessing steps
  - Contextual Bandit class implementation
  - Simulation of bandit learning and updating
  - Performance measurement and result visualization

## How it Works

1. **Data Loading:**  
   Loads and preprocesses transition data from `Transitions.csv`, mapping different screen transitions to integer labels.

2. **Contextual Bandit Algorithm:**  
   - Uses contextual features (e.g., day of the week) to select an arm (transition type) using an Upper Confidence Bound (UCB)-based strategy.
   - Updates parameters based on observed rewards (ad clicks).

3. **Simulation:**  
   - Runs multiple iterations to simulate the learning process.
   - Collects and updates rewards for chosen transitions.
   - Tracks cumulative rewards and selection counts.

## Key Concepts

- **Contextual Bandits:**  
  A variant of the multi-armed bandit algorithm that uses contextual information to improve decision making.
- **Transition:**  
  Represents different user navigation paths within the app (e.g., `['OFFLINE_SEARCH_PAGE', 'Playing_window']`).
- **Reward:**  
  In this context, whether an ad was clicked during a particular transition.

## Usage

1. **Requirements:**
   - Python 3.10+
   - Jupyter Notebook
   - Libraries: `numpy`, `pandas`, `tensorflow`, `keras`

2. **Setup:**
   - Place `Transitions.csv` in the same directory as the notebook.
   - Open and run `MAB_TRANSITIONS.ipynb` in Jupyter.

3. **Notebook Structure:**
   - **Data Preparation:** Loads and encodes the transitions.
   - **ContextualBandits Class:** Implements core logic.
   - **Simulation:** Demonstrates bandit learning in action.
   - **Results:** Displays dataframes and matrices tracking algorithm state.

## Example Output

- Matrices of learned parameters (`A`, `b`) for each transition type.
- Reward and selection count statistics for each arm and context.

## Notes

- The notebook is designed for experimental and educational purposes.
- You can adapt the contextual features or reward definitions to suit your specific use case.

## License

This project is provided for academic and educational use. Please cite or reference if used in published work.

