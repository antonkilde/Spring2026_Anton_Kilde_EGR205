import numpy as np

# Data from the table
x_data = np.array([0.4, 0.6, 0.8, 1.0, 1.2, 1.4, 1.6, 1.8, 2.0])
f_data = np.array([5.1600, 5.3040, 5.3440, 5.3200, 5.2640, 5.2000, 5.1440, 5.0960, 5.0000])

def trapezoidal_rule(x, f, n):
    # Determine step size h based on the range and number of intervals
    h = (x[-1] - x[0]) / n
    
    # determines how many points to use, or rather how many subintervals
    range = np.linspace(0, len(x) - 1, n + 1).astype(int)
    selected_f = f[range]
    print(selected_f)
    
    
    # trapezodial rule formulaa
    result = (h / 2) * (selected_f[0] + 2 * np.sum(selected_f[1:-1]) + selected_f[-1])
    return result

# Calculate for different n values
results = {n: trapezoidal_rule(x_data, f_data, n) for n in [1, 2, 4, 8]}

for n, val in results.items():
    print(f"For n={n}: Integral ≈ {val:.2f}")
