# Data Visualization

Showcasing my ability to transform raw data into clear, compelling visual insights using **Seaborn** and **Matplotlib**. This repository documents my progression from foundational plots to more polished, publication-ready visualizations.

<p align="center">
  <img src="images/plot.png" width="500">
</p>


---

## 🎯 Objective

This project demonstrates:

* Strong fundamentals in Python data visualization
* Clean, readable, and reproducible plotting code
* Appropriate chart selection for different analytical tasks
* Professional styling and storytelling with data

The goal is to build visualizations that are not just correct — but **communicate insight effectively**.

---

# 📚 Lessons

---

## 1. Matplotlib & Seaborn

**Focus:** Getting started with Seaborn and Matplotlib.

### Key skills

* Setting up plotting environment
* Understanding figure vs axes
* First statistical plots
* Using Seaborn themes

### Example

```python
import seaborn as sns
import matplotlib.pyplot as plt

sns.set_theme(style="whitegrid")

tips = sns.load_dataset("tips")

sns.scatterplot(data=tips, x="total_bill", y="tip")
plt.title("Total Bill vs Tip")
plt.show()
```

✅ Seaborn handles statistical aesthetics
✅ Matplotlib controls the figure

---

## 2. Line Charts

**Focus:** Visualizing trends over time.

### When to use

* Time series
* Trend analysis
* Continuous progression

### Key techniques

* `sns.lineplot()`
* Confidence intervals
* Markers and smoothing
* Proper date handling

### Example

```python
sns.lineplot(data=flights, x="year", y="passengers")
plt.title("Airline Passengers Over Time")
plt.show()
```

💡 **Best practice:** Always label axes and check time ordering.

---

## 3. Bar Charts and Heatmaps

**Focus:** Comparing categories and visualizing matrices.

---

### 📊 Bar Charts

**Use when:** comparing discrete categories.

```python
sns.barplot(data=tips, x="day", y="total_bill")
plt.title("Average Bill by Day")
plt.show()
```

**Key lessons**

* Aggregation happens automatically
* Order categories intentionally
* Avoid overcrowding

---

### 🔥 Heatmaps

**Use when:** showing correlation or matrix patterns.

```python
corr = tips.corr(numeric_only=True)
sns.heatmap(corr, annot=True, cmap="coolwarm")
plt.title("Correlation Heatmap")
plt.show()
```

**Key lessons**

* Great for feature relationships
* Use diverging colormaps for correlations
* Annotate when matrix is small

---

## 4. Scatter Plots

**Focus:** Exploring relationships between variables.

### When to use

* Correlation discovery
* Outlier detection
* Cluster exploration

### Example

```python
sns.scatterplot(
    data=tips,
    x="total_bill",
    y="tip",
    hue="time",
    size="size"
)
plt.title("Tip vs Total Bill")
plt.show()
```

**Key skills**

* Semantic mappings (`hue`, `size`, `style`)
* Overplotting awareness
* Using transparency (`alpha`)

💡 Scatter plots are often the **first diagnostic tool** in EDA.

---

## 5. Distributions

**Focus:** Understanding variable distributions.

---

### 📈 Histograms

```python
sns.histplot(tips["total_bill"], bins=30, kde=True)
plt.title("Distribution of Total Bill")
plt.show()
```

---

### 📉 KDE Plots

```python
sns.kdeplot(data=tips, x="total_bill", fill=True)
plt.show()
```

---

### 📦 Boxplots

```python
sns.boxplot(data=tips, x="day", y="total_bill")
plt.show()
```

**Key lessons**

* Always inspect distributions before modeling
* Watch for skewness and outliers
* Combine histogram + KDE for clarity

---

## 6. Choosing Plot Types and Custom Styles

**Focus:** Professional-quality visualization.

---

### 🎨 Styling with Seaborn

```python
sns.set_theme(style="whitegrid", palette="muted")
```

---

### 🧩 Matplotlib customization (important)

```python
plt.figure(figsize=(8,5))
plt.title("Professional Plot", fontsize=14)
plt.xlabel("X Label")
plt.ylabel("Y Label")
plt.tight_layout()
```

---

### Key professional practices

* Consistent color palette
* Proper figure sizing
* Readable fonts
* Minimal chart junk
* Informative titles

---

### When to use Matplotlib directly

Use Matplotlib when you need:

* Fine-grained control
* Subplots
* Custom annotations
* Publication formatting

Example:

```python
fig, ax = plt.subplots(figsize=(8,5))
ax.plot([1,2,3], [4,5,6])
ax.set_title("Matplotlib Control Example")
plt.show()
```

---

## 7. Final Project

**Focus:** End-to-end visualization workflow.

### Demonstrated abilities

* Data cleaning $\rightarrow$ visualization pipeline
* Appropriate chart selection
* Multi-plot storytelling
* Professional styling
* Clear analytical narrative

---

# 🛠️ Tech Stack

* Python
* Pandas
* Seaborn
* Matplotlib
* Jupyter Notebook

🚀 see more on matplotlib Gallery http://matplotlib.org/ or https://matplotlib.org/stable/tutorials/pyplot.html
