Dataset Description
The dataset consists of CSV files representing tables from a relational database. Below is a summary based on the provided data dictionary (factory_data_dictionary.csv):
Tables and Fields
•	orders: Contains order-level data.
o	order_id (PK): Unique order identifier.
o	created_at: Timestamp of order placement.
o	website_session_id (FK): Session ID from website.
o	user_id (FK): User identifier.
o	primary_product_id (FK): Primary product in the order.
o	items_purchased: Number of items.
o	price_usd: Total order price.
o	cogs_usd: Cost of goods sold.


•	order_items: Details individual items within orders.
o	order_item_id (PK): Unique item identifier.
o	created_at: Timestamp.
o	order_id (FK): Linked order.
o	product_id (FK): Product identifier.
o	is_primary_item: Flag (1 if primary).
o	price_usd: Item price.
o	cogs_usd: Item COGS.


•	order_item_refunds: Refund records.
o	order_item_refund_id (PK): Unique refund identifier.
o	created_at: Timestamp of refund.
o	order_item_id (FK): Refunded item.
o	order_id (FK): Linked order.
o	refund_amount_usd: Refund amount.
•	products: Product catalog.
o	product_id (PK): Unique product identifier.
o	created_at: Launch timestamp.
o	product_name: Name (e.g., "The Original Mr. Fuzzy", "The Forever Love Bear").

Files in Repository
•	factory_data_dictionary.csv: Data dictionary describing all tables and fields.
•	products.csv: Product data.
•	order_item_refunds.csv: Refund data (includes truncated records; full data may need cleaning).
•	order_items.csv: Order item details (truncated; handle large files carefully).
•	orders.csv: Order data (truncated).
•	sales_analysis.sql: Sample SQL queries for analysis (e.g., total revenue, refund rates).
•	teddy_bear_sales.pbix: Power BI file with sample dashboards (if uploaded; otherwise, create your own).
Data spans from 2012 to 2015, focusing on products like teddy bears. 

Prerequisites
•	SQL: Use a database like MySQL, PostgreSQL, or SQLite to import the CSVs.
•	Power BI: Download Power BI Desktop (free from Microsoft).
•Excel (optional): For data cleaning if needed.
