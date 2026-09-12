# Data Dictionary

## Bronze layer

The Bronze layer stores raw, minimally transformed source data.

### Typical tables

- `raw_sales`
- `raw_customers`
- `raw_products`
- `raw_events`

### Characteristics

- Source-aligned field names
- Raw timestamps and codes retained
- Minimal schema validation
- Useful for lineage and replay

## Silver layer

The Silver layer represents cleaned and conformed data ready for analytics.

### Typical tables

- `dim_customer`
- `dim_product`
- `fact_sales_order`
- `fact_returns`

### Characteristics

- Standardized naming conventions
- Type normalization
- Deduplication
- Null and quality rule enforcement

## Gold layer

The Gold layer stores curated business-ready datasets for reporting and consumption.

### Typical tables

- `gold_sales_kpi`
- `gold_customer_lifetime_value`
- `gold_channel_performance`
- `gold_operational_scorecard`

### Characteristics

- Aggregate or business-ready semantics
- Optimized for dashboards and self-service BI
- KPI definitions aligned to business logic
- Stable and trusted reporting source

## Field convention guidance

- Use lowercase snake_case for table and column names
- Store surrogate keys as `*_key`
- Maintain business keys and source keys separately when required
- Use consistent date field naming: `order_date`, `created_at`, etc.
