# Example 1

## Problem 

A sample of **10 exam scores** was collected:

12, 15, 18, 20, 22, 24, 25, 27, 30, 37

Find:

- Five Number Summary
- Mean
- Variance
- Standard Deviation
- Coefficient of Variation
- Standard Error
- Margin of Error (95%)
- Confidence Interval

---

# Sort the Data

Data (already sorted):

12, 15, 18, 20, 22, 24, 25, 27, 30, 37

Sample size:

$$
n = 10
$$

---

# Five Number Summary

| Statistic | Value |
|-----------|------|
| Minimum | 12 |
| Q1 | 18 |
| Median | 23 |
| Q3 | 27 |
| Maximum | 37 |

Median:

$$
\frac{22 + 24}{2} = 23
$$

---

# Mean

Formula:

$$
\bar{x} = \frac{\sum x}{n}
$$

Sum of all values:

$$
12 + 15 + 18 + 20 + 22 + 24 + 25 + 27 + 30 + 37 = 230
$$

Mean:

$$
\bar{x} = \frac{230}{10} = 23
$$

Mean = **23**

---

# Variance

Formula (sample variance):

$$
s^2 = \frac{\sum (x - \bar{x})^2}{n - 1}
$$

| x | x − 23 | (x − 23)² |
|---|---|---|
|12| -11 |121|
|15| -8 |64|
|18| -5 |25|
|20| -3 |9|
|22| -1 |1|
|24| 1 |1|
|25| 2 |4|
|27| 4 |16|
|30| 7 |49|
|37| 14 |196|

Sum of squared deviations:

$$
486
$$

Variance:

$$
s^2 = \frac{486}{9} = 54
$$

Variance ≈ **54**

---

# Standard Deviation

Formula:

$$
s = \sqrt{s^2}
$$

$$
s = \sqrt{54}
$$

$$
s \approx 7.35
$$

Standard deviation ≈ **7.35**

---

# Coefficient of Variation

Formula:

$$
CV = \frac{s}{\bar{x}} \times 100\%
$$

Substitute values:

$$
CV = \frac{7.35}{23} \times 100
$$

$$
CV \approx 31.96\%
$$

Coefficient of variation ≈ **31.96%**

---
# Standard Score (Z-score)

The **Z-score** measures how many standard deviations a value is from the mean.

**Formula:**
$$  
z = \frac{x - \mu}{\sigma}  
$$
---

## What the Graph Represents

A **normal distribution (bell curve)** shows how data is spread around the mean.

- **μ (mu)** = population mean (center of the curve)  
- **σ (sigma)** = standard deviation  
- **z** = number of standard deviations a value is from the mean  

The **Z-score formula** converts a raw value into standard deviation units.

---

## Standard Deviations on the Curve

Most real-world data clusters near the mean. The **Empirical Rule (68–95–99.7 rule)** describes this:

| Range    | Percent of Data |
|---------|----------------|
| μ ± 1σ  | 68%            |
| μ ± 2σ  | 95%            |
| μ ± 3σ  | 99.7%          |

Conceptual curve:

![[normal 10_08_10 PM.png]]

Axis positions:

-3σ   -2σ   -1σ    μ    +1σ   +2σ   +3σ

---

## Using Data

Suppose:
$$  
\mu = 23, \quad \sigma \approx 7.35, \quad x = 30  
$$
### Compute Z-score
$$  
z = \frac{x - \mu}{\sigma} = \frac{30 - 23}{7.35} \approx 0.95  
$$
### Interpretation

A **z-score of 0.95** means:

- The value is **0.95 standard deviations above the mean**  
- Slightly above average  

---

## Approximate Percentile

A z-score of **0.95** corresponds to roughly:

82nd percentile

> The score is higher than about 82% of the data.

---

### Example Diagram

Here’s a bell curve diagram highlighting z ≈ 0.95:

![[bell 10_04_15 PM.png]]

---
# Finding Standard Error

Formula:

$$
SE = \frac{s}{\sqrt{n}}
$$

Substitute values:

$$
SE = \frac{7.35}{\sqrt{10}}
$$

$$
SE = \frac{7.35}{3.162}
$$

$$
SE = \frac{7.35}{\sqrt{10}}
$$

$$
SE \approx 2.32
$$

Standard error ≈ **2.32**

---

# Margin of Error (95%)

Formula:

$$
MOE = z \times SE
$$

For a **95% confidence level**:

$$
z = 1.96
$$

Substitute values:

$$
MOE = 1.96 \times 2.32
$$

$$
MOE \approx 4.55
$$

Margin of error ≈ **4.55**

---

# Confidence Interval

General form:

$$
\bar{x} \pm MOE
$$

Substitute values:

$$
23 \pm 4.55
$$

Lower bound:

$$
23 - 4.55 = 18.45
$$

Upper bound:

$$
23 + 4.55 = 27.55
$$

---

# 95% Confidence Interval

$$
18.45 \le \mu \le 27.55
$$

The true population mean is estimated to lie between **18.45 and 27.55** with **95% confidence**.
