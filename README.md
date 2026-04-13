# NYC Yellow Taxi Trip Data Analysis with PySpark

Analysis of 3.5M NYC yellow taxi trips (August 2025) using PySpark 4.0 on Google Colab.

## Dataset
- **Source:** NYC Taxi & Limousine Commission — Yellow Taxi Trip Records
- **Period:** August 2025
- **Raw records:** 3,574,091
- **Clean records:** 2,511,464

## What's covered

**Data Cleaning**
- Null removal, type casting, and filtering invalid entries (negative fares, zero distances, etc.)

**Exploratory Data Analysis**
- Hourly and daily trip patterns
- Top pickup/dropoff locations and popular routes
- Fare distribution, payment type breakdown, passenger count analysis

**Spark SQL**
- Peak vs off-peak comparison
- Weekday vs weekend analysis
- High-value route identification
- Tipping patterns by hour

**Performance Optimization**
- DataFrame caching (24.9% improvement)
- Broadcast join for small table lookup
- Repartitioning by pickup hour

**Statistical Analysis**
- Correlation between distance, fare, and duration
- IQR-based outlier detection on fare amounts

## Results
| Metric | Value |
|---|---|
| Trip Distance vs Fare correlation | 0.827 |
| Peak hour trips share | 21.86% |
| Fare amount outliers | 11.06% |
| Caching performance improvement | 24.9% |

## Tools
- PySpark 4.0.1
- Python 3.12
- Google Colab (TPU v5e-1)
- Tableau (for exported CSVs)
