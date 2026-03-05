🧹 SQL Data Cleaning: Customer Orders
This project demonstrates advanced data engineering techniques using Google BigQuery to transform a highly "noisy" raw dataset into a clean, analysis-ready source of truth.

🛠️ Key Cleaning Highlights
Pseudo-NULL Resolution: Identified and converted string 'NULL' text into actual system NULLs to ensure accurate data aggregation.

Schema Enforcement: Standardized inconsistent order_date strings into a unified DATE format and handled "human-entry" errors in the quantity column.

String Normalization: Unified customer and product entities (e.g., branding and casing fixes) using INITCAP and TRIM.

Email Validation: Fixed broken email syntax (e.g., double @@) and normalized all entries to lowercase for consistent user identification.

Deduplication: Implemented logic to remove redundant order entries, ensuring each record represents a unique transaction.

📂 Project Structure
cleaning_script.sql: The full BigQuery SQL script containing all transformation logic.

raw_data_sample.csv: A sample of the messy dataset before any cleaning was applied.

clean_data_sample.csv: The final, structured output after script execution.
