# Day 27: Ride Booking Data Analysis (Using Python Tuples)

A beginner-friendly Python coding challenge where you play the role of a data analyst at a ride-booking company (like Ola/Uber). The trip data is stored as tuples, and the goal is to answer common business questions using loops, conditionals, and built-in functions.

## Files

| File | Description |
|------|-------------|
| `Day27_Coding_Challenge.pdf` | Problem statement and task list |
| `Day-27-Data-analytics-challenge-python.ipynb` | Jupyter Notebook with the solutions |

## Dataset

Each trip is a tuple in the format:

```
(Trip_ID, City, Distance_km, Fare_amount)
```

```python
trips = (
    (101, "Bangalore", 12.5, 250),
    (102, "Hyderabad", 8.0, 180),
    (103, "Bangalore", 15.2, 300),
    (104, "Chennai", 5.5, 120),
    (105, "Bangalore", 7.8, 200)
)
```

## Tasks and Results

| # | Task | Approach | Output |
|---|------|----------|--------|
| 1 | Total number of trips | `len(trips)` | `5` |
| 2 | Trips from Bangalore | Loop + membership check (`in`) with a counter | `3` |
| 3 | Total revenue | Loop and sum the fare at index `3` | `1050` |
| 4 | Trips with distance > 10 km | Loop + `if i[2] > 10` | Trips `101` and `103` |
| 5 | Highest fare trip | Collect fares in a list, use `max()` and `.index()` | `(103, 'Bangalore', 15.2, 300)` |
| 6 | Average fare for Bangalore (bonus) | Filter Bangalore fares, then `sum() / count` | `250.0` |

## Concepts Practiced

- Tuples and nested tuples
- Indexing (`i[2]`, `i[3]`)
- `for` loops and `if` conditions
- Counters and accumulators
- Built-ins: `len()`, `sum()`, `max()`, `list.index()`
- Filtering data and calculating averages

## How to Run

1. Install Python 3.9+ and Jupyter:
   ```bash
   pip install notebook
   ```
2. Open the notebook:
   ```bash
   jupyter notebook Day-27-Data-analytics-challenge-python.ipynb
   ```
3. Run the cells from top to bottom (`Shift + Enter`).

## Sample Output

```
Total number of Trips: 5
Trips Happened in Bangalore: 3
Total fare amount collected from all trips: 1050
(101, 'Bangalore', 12.5, 250)
(103, 'Bangalore', 15.2, 300)
The Trip with maximum fare: (103, 'Bangalore', 15.2, 300)
The Average fare for Bangalore Trips: 250.0
```

## Possible Improvements

- Use `if i[1] == "Bangalore"` instead of `"Bangalore" in i`. It is stricter, since `in` checks every field of the tuple.
- Use `max(trips, key=lambda t: t[3])` to find the highest fare trip in one line.
- Use a generator expression, e.g. `sum(t[3] for t in trips)`, for totals.
- Extend the analysis with per-city revenue, fare per km, or the same logic in `pandas`.

## Author

Day 27 of my Python / Data Analytics learning journey.
