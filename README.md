# Cleaning_Bank_Marketing_Campaign_Data
Tidied a bank marketing campaign dataset by splitting it into subsets, updating values, converting data types, and storing it as multiple csv files.

## Bank Marketing Data Cleaning: Splitting One CSV into 3 Database-Ready Tables | Python, pandas

Cleaned and restructured a raw bank marketing file into three typed CSVs (client, campaign, economics) linked by client_id, ready to load into a PostgreSQL database for this and future campaigns.

# CONTEXT
A bank wanted its personal-loan campaign data in a fixed structure with specified data types, so it could populate a database and import later campaigns easily. The source was one wide CSV mixing client details, campaign activity and economic indicators.

# MY ROLE
I handled the full workflow: reading, splitting, cleaning, type conversion and saving.

# WHAT I DID
• Split 41189 rows of bank_marketing.csv into three tables, each keeping client_id as the key
• Text cleaning: replaced "." with "_" in job and education, and converted "unknown" education values to proper missing values (NaN)
• Type conversion: turned yes/no and success/failure flags into booleans for credit_default, mortgage, previous_outcome and campaign_outcome
• Date feature: built last_contact_date from day, month and a year of 2022 (given in the brief), formatted YYYY-MM-DD
• Saved client.csv, campaign.csv and economics.csv without an index
• Checked the raw value counts of the flag columns before converting them (e.g.: credit_default: no 32588, unknown 8597, yes 3)

# RESULTS
• Three files matching the specified columns and data types (confirmed with .info() on all three)
• 1731 missing education values stored as NaN, not as a text label
• One messy input became a repeatable structure that new campaigns can follow

# TECH STACK
Python, pandas, NumPy
