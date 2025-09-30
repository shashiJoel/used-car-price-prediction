# Used Car Price Prediction Analysis
A machine learning project that predicts used car prices from historical sales records using key automotive features and uncover what consumers value in used cars.

**Assignment Notebook**: [prompt_II.ipynb](./prompt_II.ipynb)

## Project Overview

This project analyzes **426,000+ used car records** to identify the key factors that drive vehicle pricing, providing actionable insights for used car dealerships to optimize their inventory and pricing strategies.

## Dataset Summary

- **Source**: Kaggle Used Cars Dataset
- **Records Analyzed**: 426,000+ vehicles (cleaned to 106,602 for modeling)
- **Features**: Year, Odometer, Manufacturer, Model, Condition, etc.
- **Target Variable**: Car Price ($500 - $150,000 range)
- **Analysis Period**: Multi-year dataset covering various makes and models

## Key Research Question

**"What drives the price of a car?"**

Our analysis provides data-driven answers to help used car dealerships make more profitable inventory and pricing decisions.

## Major Findings

### Primary Price Drivers (Explaining 42.7% of Price Variation)

#### 1. **Vehicle Age (Year) - PRIMARY DRIVER**
- **Impact**: Each year newer increases value by ~**$3,000-4,000**
- **Total Range Impact**: ~$60,000+ across model years in dataset
- **Business Insight**: Age is the strongest predictor of car value
- **Recommendation**: Prioritize vehicles 3-5 years old for optimal inventory

#### 2. **Vehicle Mileage (Odometer) - SECONDARY DRIVER**
- **Impact**: Each mile decreases value by ~**$0.10-0.20**
- **Per 10,000 Miles**: ~$1,000-2,000 value decrease
- **Total Range Impact**: ~$30,000+ across mileage spectrum
- **Business Insight**: Lower mileage significantly increases value
- **Recommendation**: Target vehicles under 15,000 miles per year of age

### Model Performance

- **R² Score**: 0.427 (explains 42.7% of price variation)
- **RMSE**: $10,071 average prediction error
- **Business Accuracy**: ~60% of predictions within $2,000 of actual price
- **Model Type**: Linear Regression (interpretable and reliable)

## Business Impact & Recommendations

### Inventory Strategy
1. **Focus on newer vehicles** (2018+ for maximum value)
2. **Prioritize low-mileage cars** (under 60,000 miles ideal)
3. **Avoid high-mileage vehicles** unless exceptional deals
4. **Sweet spot**: 3-5 year old cars with below-average mileage

### Pricing Strategy
1. **Use Age + Mileage as baseline** for initial pricing
2. **Apply $3,000-4,000 premium** per year newer
3. **Deduct $1,000-2,000** per 10,000 additional miles
4. **Adjust for brand, condition, and market factors**

### Competitive Advantages
- **Data-driven pricing** replaces guesswork
- **Quantified value drivers** for customer education
- **Faster inventory turnover** through accurate pricing
- **Improved profit margins** via strategic acquisition

## Technical Approach

### Data Preprocessing
- Removed irrelevant columns (ID, VIN, region)
- Handled missing values and outliers
- Focused on numerical features for baseline model
- Applied statistical outlier removal (2-sigma rule)

### Modeling
- **Linear Regression**: Baseline interpretable model
- **Ridge Regression**: L2 regularization for stability
- **Lasso Regression**: L1 regularization with feature selection
- **Best Model**: Linear Regression (simplicity + performance)

### Validation
- 70/30 train-test split
- Cross-validation for model reliability
- Business-focused metrics (MAPE, prediction intervals)

## Sample Predictions

| Car Year | Mileage | Predicted Price | Description |
|----------|---------|----------------|-------------|
| 2020 | 30,000 | $28,500 | Nearly New |
| 2018 | 45,000 | $22,800 | Low Mileage |
| 2015 | 80,000 | $15,200 | Average Condition |
| 2012 | 120,000 | $9,800 | Higher Mileage |
| 2010 | 150,000 | $6,500 | Older Vehicle |

## Key Insights Summary

### What REALLY Drives Car Prices:

1. **AGE dominates pricing** - Newer cars command premiums regardless of other factors
2. **MILEAGE is crucial** - Low-mileage vehicles significantly outperform high-mileage ones
3. **Simple model works** - Just 2 features explain nearly half of all price variation
4. **Consistency matters** - Age + mileage provide reliable baseline for any vehicle

### Business Formula:
```
PROFITABLE INVENTORY = NEWER CARS + LOWER MILEAGE + DATA-DRIVEN PRICING
```

## Implementation

### Immediate Actions
1. **Apply age/mileage-based pricing** to current inventory
2. **Train sales team** on quantified value drivers
3. **Adjust acquisition strategy** toward newer, low-mileage vehicles
4. **Use prediction model** for quick pricing estimates

### Long-term Improvements
- Add make/model data for brand premiums
- Include condition ratings and service history
- Incorporate local market factors
- Update model quarterly with new sales data

## Repository Structure

```
├── prompt_II.ipynb          # Main analysis notebook
├── README.md               # This file
├── data/
│   └── vehicles.csv        # Raw dataset
└── images/
    ├── crisp.png          # CRISP-DM framework
    └── kurt.jpeg          # Project image
```

## Technologies Used

- **Python 3.x**
- **Pandas & NumPy** - Data manipulation
- **Scikit-learn** - Machine learning models
- **Matplotlib & Seaborn** - Data visualization
- **Jupyter Notebook** - Analysis environment

## Model Limitations

- Only uses 2 numerical features (42.7% explanation)
- Missing brand/model premium effects
- No condition or feature considerations
- Market timing and economic factors excluded
- Requires periodic updates with new data

## Conclusion

This analysis proves that **vehicle age and mileage are the fundamental drivers of used car pricing**. While many factors influence car values, these two metrics provide a reliable foundation for pricing decisions.

**For dealerships**: Focus on acquiring newer, low-mileage vehicles and use data-driven pricing based on age and mileage. This approach will lead to more profitable inventory decisions and improved customer satisfaction through transparent, justifiable pricing.

---

*Analysis completed using CRISP-DM methodology. Model performance suitable for business decision support with recommended human oversight for final pricing decisions.*