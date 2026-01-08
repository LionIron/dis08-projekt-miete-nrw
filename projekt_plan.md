# DIS08 Project Plan  
## Rental Prices and Housing Characteristics in North Rhine-Westphalia (NRW)

### 1. Topic and Motivation
This project analyzes apartment rental offers in Germany with a focus on
North Rhine-Westphalia (NRW). Housing affordability is a major social and
economic issue, especially in densely populated regions. By analyzing rental
offers, this project aims to identify structural differences in rental prices
between cities and to examine how housing characteristics influence price levels.

The project follows the OSEMN framework (Obtain, Scrub, Explore, Model, Interpret)
as introduced in the DIS08 course.

---

### 2. Dataset Description (Obtain)
**Base dataset**
- Source: Apartment rental offers in Germany
- Format: CSV
- Storage: `data/raw/immo_data.csv`
- Content: Rental prices, living space, number of rooms, location, building and
  equipment characteristics

**Scope**
- Geographic focus: North Rhine-Westphalia (filtered via `regio1`)
- Observations: Apartment rental listings (offer prices, not contracts)

---

### 3. Research Questions
1. How do rental prices per square meter differ between major cities in NRW?
2. How strongly does living space influence rental prices per square meter?
3. Do housing characteristics (e.g. balcony, elevator, built-in kitchen)
   systematically affect rental prices?
4. Are smaller apartments disproportionately more expensive per square meter
   than larger apartments?

---

### 4. Planned Data Engineering Pipeline
**Obtain**
- Load raw CSV data
- Filter observations for NRW

**Scrub**
- Handle missing values in price and living space
- Remove implausible values and outliers
- Create derived variables (e.g. price per square meter)

**Explore**
- Descriptive statistics
- City-level comparisons
- Distribution analysis

**Model**
- Group comparisons
- Correlation analysis
- Hypothesis testing (as introduced in the lecture)

**Interpret**
- Interpretation of results
- Discussion of limitations

---

### 5. Tools and Methods
- Python
- Jupyter Notebooks
- pandas
- matplotlib / seaborn
- scipy / statsmodels (hypothesis testing)
- Git & GitHub for version control

---

### 6. Repository Structure
- `data/raw/` – original dataset (ignored in Git)
- `data/processed/` – cleaned datasets
- `notebooks/` – analysis notebooks
- `docs/` – documentation and poster
- `src/` – reusable code
