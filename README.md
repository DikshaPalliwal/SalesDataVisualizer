Project Overview
Industry-grade e-commerce analytics dashboard built for Amazon product sales data analysis. Transforms raw product listings (4.7MB CSV) into actionable business insights through advanced data visualization.

Live Demo: [

✨ Features
Feature	Business Value
Price/Discount Analysis	Optimize pricing strategies
Category Performance	Identify top revenue segments
Rating Distributions	Quality-price correlation
Savings Heatmaps	Profit margin opportunities
Production Exports	Report-ready PNGs (300 DPI) + CSV
📊 Dataset
Amazon Product Sales Data (sales.csv - 4.7MB)

text
Columns: product_id, product_name, category, discounted_price, actual_price, 
         discount_percentage, rating, rating_count, about_product...
Key Metrics Extracted:

discounted_price → Final sale price (₹ cleaned)

actual_price → List price (revenue proxy)

discount_percentage → Margin compression analysis

category → Hierarchical (Computers&Accessories|Cables&Accessories...)

rating → Customer satisfaction proxy

🛠️ Tech Stack
text
📚 Data Processing: Pandas (ETL, string parsing, groupby)
📈 Visualization: Seaborn + Matplotlib (heatmaps, regplots, boxplots)
🌐 Deployment: Google Colab (zero-setup, drag-drop)
💾 Export: High-res PNGs + Processed CSV
📈 Generated Visualizations
Top Categories by Avg Price (Bar) - Market positioning

Discount vs Price Trend (Regression) - Pricing elasticity

Rating by Category (Boxplot) - Quality benchmarks

Discount Band Heatmap (Matrix) - Strategy effectiveness

Savings Share Pie - Category contribution analysis

🚀 Quick Start
bash
# 1. Clone repo
git clone https://github.com/yourusername/sales-data-visualizer.git
cd sales-data-visualizer

# 2. Open Colab (recommended)
# Copy sales.csv → Colab → Run 8 cells sequentially

# 3. Or local Jupyter
pip install pandas seaborn matplotlib
jupyter notebook sales_visualizer.ipynb
Colab Instructions:

Upload sales.csv (drag-drop)

Run cells 1-8 sequentially (~2 mins)

Download PNGs + processed_sales_analysis.csv automatically

📁 Project Structure
text
sales-data-visualizer/
├── 📄 README.md                 # This file
├── 📊 sales.csv                # Dataset (4.7MB)
├── 📓 sales_visualizer.ipynb    # Complete Colab notebook
├── 🖼️ outputs/                 # Generated charts
│   ├── top_categories_price.png
│   ├── discount_trend.png
│   └── savings_heatmap.png
└── 📊 processed_sales_analysis.csv  # Cleaned data
🎯 Business Insights
Sample Findings (varies by dataset):

text
💰 Total Potential Savings: ₹25M+ across catalog
🏆 Top Category: Computers&Accessories (42% savings share)
⚠️ High Risk: 30%+ discounts → 15% rating drop
🎯 Sweet Spot: 20-40% discount → optimal revenue/rating
🔧 Customization
Add Your Features:

python
# Forecasting
df['price_trend'] = df['discounted_price'].rolling(30).mean()

# ML Clustering
from sklearn.cluster import KMeans
kmeans = KMeans(n_clusters=5).fit(df[['rating', 'discount_percentage']])

# Interactive Dashboard
# pip install streamlit plotly
👥 Target Audience
Data Science Students → Portfolio project

Business Analysts → E-commerce insights

Product Managers → Pricing optimization

Freelance Analysts → Client deliverables

📈 Industry Relevance
✅ Data Science Interviews: End-to-end pipeline (ETL → Insights)
✅ Internship Applications: Production-grade exports
✅ Freelance Projects: Customizable, client-ready
✅ Academic Projects: Well-documented methodology

📊 Key Concepts Demonstrated
Concept	Application
String Parsing	₹1,099 → 1099.0 numeric
Category Splitting	Computers|Cables → hierarchical analysis
Discount Bands	pd.cut() for business segmentation
Revenue Proxy	actual_price as sales volume indicator
Production Viz	300 DPI, tight_layout, publication-ready
🤝 Contributing
Fork repository

Add new visualizations/metrics

Update README with new insights

Submit PR with dataset examples

📄 License
MIT License - Feel free to use for portfolios, commercial projects, interviews.

👨‍💼 Author
Trading DNA - Data Science Student | Pune, India
March 2026 | Built with Perplexity AI

text
⭐ Star if helpful! Perfect for interviews & portfolios.
🔗 Connect: linkedin.com/in/tradingdna
Keywords: e-commerce analytics, pandas visualization, sales dashboard, data science portfolio, google colab project, amazon sales analysis
