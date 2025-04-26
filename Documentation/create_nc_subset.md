# Creating the North Carolina Health Care Subset

This code filters a larger dataset to only include North Carolina data and selects important columns for analysis.

## Code

```python
import pandas as pd

# Load the full dataset
df = pd.read_csv('your_full_dataset.csv')  # Replace 'your_full_dataset.csv' with your actual file name

# Create a subset for North Carolina
nc_subset = df[df["State"] == "NC"][['County', 'Year', 'Health care costs']].copy()

# Save the subset as a CSV
nc_subset.to_csv('nc_subset.csv', index=False)
