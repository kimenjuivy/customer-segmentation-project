# How to Run the Customer Segmentation Project

## Quick Start (5 minutes)
```bash
# 1. Clone and navigate
git clone [your-repo-url]
cd customer-segmentation-project

# 2. Create environment
conda env create -f environment.yml
conda activate retail-analytics

# 3. Run analysis
jupyter notebook
# Then run notebooks 01→02→03→04→05 in order
```

## Alternative: Pip Installation
```bash
pip install -r requirements.txt
```

## Dashboard Viewing
```bash
# Open interactive dashboards
open visuals/executive_dashboard.html
open visuals/interactive_revenue_forecast.html
```

## External Tool Integration

### Tableau
1. Connect to `data/dashboard_main.csv`
2. Join with `data/customer_segments.csv` on customerid
3. Use `data/forecast_next90.csv` for predictions

### Power BI
1. Import from folder: `data/`
2. Auto-detect relationships or use `external_tool_config.json`
3. Create visuals from pre-aggregated tables

### Excel
1. Open `data/executive_summary.xlsx`
2. Create pivot tables from `data/monthly_summary.csv`
3. Import other CSV files as needed

## Troubleshooting
- **Prophet installation**: Use `conda install -c conda-forge prophet`
- **Plotly export**: Install `pip install kaleido` for static image export
- **Memory issues**: Reduce date ranges in notebooks if needed

## Project Structure
- `notebooks/`: Analysis pipeline (run in order 01-05)
- `data/`: All datasets and exports  
- `visuals/`: Charts and interactive dashboards
- `README.md`: Complete project documentation
