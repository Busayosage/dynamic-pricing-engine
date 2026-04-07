# Dynamic Pricing Engine

## Business Problem
Retail businesses often lose margin and create avoidable waste because pricing and supply decisions are too static. When demand changes but pricing or replenishment does not, the result can be overstocking, underpricing, or poor stock allocation.

## Objective
The objective of this project is to build a simple decision-support engine that uses historical sales and wastage patterns to recommend practical pricing or supply actions for each product.

## Data Used
The project uses transaction and product-level retail data stored in SQLite, including:

- product identifiers
- demand history
- average sales levels
- wastage signals
- pricing-related fields

The output is then pushed into Airtable to make the recommendations easier to review operationally.

## Approach
1. **Data preparation**
   - Loaded retail sales data into SQLite
   - Aggregated sales and wastage at product level

2. **Demand estimation**
   - Used simple historical demand logic to create a forecast signal

3. **Decision rules**
   - Combined demand level and wastage behaviour
   - Assigned actions such as:
     - increase price
     - discount price
     - reduce supply
     - keep stable

4. **Business-facing output**
   - Generated a recommendation table
   - Sent outputs to Airtable for easy visibility and use by non-technical stakeholders

## Tools
- Python
- Pandas
- SQLite
- Airtable API

## Key Results
- The engine translated raw demand and wastage data into product-level recommendations.  
  **Business decision:** Teams can move from reviewing raw numbers to acting on a shortlist of recommended pricing or supply changes.

- Products with strong demand but high wastage were identified as supply-planning problems rather than simple pricing wins.  
  **Business decision:** Reduce supply or improve stock planning before assuming that higher demand means higher prices.

- Products with weaker demand and high waste risk were flagged for discount consideration.  
  **Business decision:** Use markdowns selectively to reduce avoidable waste and recover value.

- The final output was structured for operational use through Airtable.  
  **Business decision:** The analysis becomes easier to review, share and act on across teams.

## Business Impact
This project demonstrates practical decision support. Instead of stopping at analysis, it converts demand patterns into actions that a business can actually use. The benefit is stronger pricing discipline, better supply decisions, and a more operationally useful analytics workflow.
