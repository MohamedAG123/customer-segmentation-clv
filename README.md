# Customer Segmentation & Lifetime Value Analysis

## Business problem
Not all customers are equal. This project segments Olist's 93,000+ e-commerce customers
by purchasing behaviour to identify who is most valuable, who is at risk of being lost,
and what the business should do differently for each group.

## Dataset
[Olist Brazilian E-Commerce Dataset](https://www.kaggle.com/datasets/olistbr/brazilian-ecommerce)
— real transaction data from 2016–2018 across 8 relational tables covering orders,
customers, products, sellers, payments, and reviews.

## Approach
1. **Exploratory data analysis** — order trends, revenue growth, top categories, geographic distribution
2. **RFM feature engineering** — Recency, Frequency, and Monetary value computed per customer
3. **K-Means clustering** — optimal k selected using elbow method and silhouette score
4. **Segment profiling** — each cluster named and characterised by behaviour
5. **CLV estimation** — Customer Lifetime Value calculated per segment

## Key findings
- **97% of customers placed only one order** — Olist has a severe retention problem
- **High-Value Inactive customers (30% of base) generate 57.5% of revenue** — a classic power law
- **Loyal Customers have 9.4× higher CLV** than Low-Value Inactive customers (R$981 vs R$104)
- A post-purchase nurture sequence targeting first-time buyers is the single highest-leverage intervention

## Segments identified

| Segment | Customers | Avg Spend | Est. CLV | Revenue Share |
|---|---|---|---|---|
| Loyal Customers | 2,801 | R$309 | R$981 | 5.6% |
| High-Value Inactive | 27,816 | R$319 | R$478 | 57.5% |
| Lost Customers | 27,045 | R$119 | R$179 | 20.9% |
| Low-Value Inactive | 35,696 | R$69 | R$104 | 16.0% |

## Tools
Python · Pandas · Scikit-learn · Plotly · Jupyter Notebook

## How to run
1. Download the dataset from Kaggle and place CSVs in `Data/Brazilian e-commerce/`
2. Open `customer_segmentation_clv.ipynb` in VS Code or Jupyter
3. Run all cells in order
