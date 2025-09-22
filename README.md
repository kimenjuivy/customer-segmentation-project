# Customer Segmentation & Revenue Forecasting Project

## 🎯 Project Overview
Advanced retail analytics project using machine learning for customer segmentation and revenue forecasting on UCI Online Retail dataset (2010-2011).

## 📊 Business Impact
- **$8,887,209** total revenue analyzed across **18,532** transactions
- **4,338** customers segmented into actionable business groups  
- **90-day revenue forecast**: $1,179,465** with 95% confidence intervals
- **72.5%** data quality score achieved through rigorous cleaning

## 🔬 Methodology

### Data Processing
- **Raw Dataset**: 541,909 transactions → **392,692** clean records
- **Missing Data**: Systematic removal and imputation strategies
- **Outlier Treatment**: Statistical capping and business logic validation
- **Feature Engineering**: RFM metrics, temporal features, customer lifetime value

### Customer Segmentation (RFM Analysis)
- **Recency**: Days since last purchase (0-374 days)
- **Frequency**: Purchase count (1-209 orders)  
- **Monetary**: Total customer value ($3.75 - $280,206)
- **Algorithm**: K-Means clustering with silhouette optimization
- **Result**: 2 distinct customer segments identified

### Revenue Forecasting
- **Model**: Facebook Prophet with seasonal decomposition
- **Validation**: Time series cross-validation on 70-day holdout
- **Performance**: inf% MAPE, $20,733 MAE
- **Forecast Period**: 90 days with uncertainty quantification

## 📁 Project Structure
```
customer-segmentation-project/
├── data/
│   ├── raw/                    # Original dataset
│   ├── clean_sales.csv         # Processed transactions
│   ├── customer_segments.csv   # RFM segmentation results
│   ├── forecast_next90.csv     # Revenue predictions
│   └── dashboard_*.csv         # Dashboard-ready datasets
├── notebooks/
│   ├── 01_data_prep.ipynb      # Data cleaning & validation
│   ├── 02_eda.ipynb           # Exploratory data analysis  
│   ├── 03_rfm_clustering.ipynb # Customer segmentation
│   ├── 04_forecast.ipynb       # Revenue forecasting
│   └── 05_dashboard_final.ipynb # Dashboard creation
├── visuals/
│   ├── interactive_*.html      # Plotly dashboards
│   └── *.png                  # Static visualizations
└── README.md
```

## 🚀 How to Run

### Prerequisites
```bash
conda create -n retail-analytics python=3.9
conda activate retail-analytics
conda install pandas numpy matplotlib seaborn scikit-learn
conda install -c conda-forge plotly prophet
pip install jupyter
```

### Execution
```bash
# Clone repository
git clone [your-repo-url]
cd customer-segmentation-project

# Run analysis pipeline
jupyter notebook notebooks/01_data_prep.ipynb
jupyter notebook notebooks/02_eda.ipynb  
jupyter notebook notebooks/03_rfm_clustering.ipynb
jupyter notebook notebooks/04_forecast.ipynb
jupyter notebook notebooks/05_dashboard_final.ipynb
```

## 📈 Key Findings

### Customer Segments
- **Champions** (26 customers): High-value customers with frequent recent purchases
- **Loyal Customers** (4312 customers): Consistent buyers with moderate recency

### Revenue Insights
- **Peak Performance**: 2010-12-01 to 2011-12-09
- **Seasonality**: Strong weekly patterns with Tuesday-Thursday peaks
- **Geographic Concentration**: UK represents 82% of total revenue
- **Product Portfolio**: 3,665 unique SKUs analyzed

### Forecast Validation
- **Model Accuracy**: inf% mean absolute percentage error
- **Business Value**: 90-day revenue prediction enables inventory optimization
- **Risk Assessment**: Confidence intervals provide scenario planning

## 🎯 Business Recommendations

### Immediate Actions (Next 30 Days)
1. **Champion Customer Retention**: Deploy VIP program for top 26 customers
2. **Inventory Planning**: Prepare for forecasted revenue patterns 
3. **Marketing Segmentation**: Targeted campaigns based on RFM profiles

### Strategic Initiatives (Next Quarter)
1. **Geographic Expansion**: Reduce UK dependency (currently 82% concentration)
2. **Product Diversification**: Focus on underperforming SKUs
3. **Customer Lifecycle**: Implement win-back campaigns for at-risk segments

## 📊 Dashboard Access
- **Executive Summary**: `visuals/executive_dashboard.html`
- **Customer Analysis**: `visuals/interactive_customer_segments.html`  
- **Revenue Forecasting**: `visuals/interactive_revenue_forecast.html`
- **Product Performance**: `visuals/interactive_product_analysis.html`

## 🔧 External Tool Integration
- **Tableau**: Use `data/dashboard_main.csv` as primary data source
- **Power BI**: Connect to `data/` folder with pre-configured relationships
- **Excel**: Import `data/executive_summary.xlsx` for pivot table analysis

## 📞 Contact
**Data Science Team** | [LinkedIn Profile] | [Portfolio Website]

---
*Generated on 2025-09-22 18:29:00 | Data Analysis Period: 2010-12-01 to 2011-12-09*
