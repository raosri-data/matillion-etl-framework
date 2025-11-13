# Matillion ETL Framework - Architecture Notes

Goals:
- Parameterized, reusable jobs
- Control table drives which SQL runs and target table names
- Audit logging and error handling via Matillion components

Variable patterns:
- jv_target_schema: schema name (e.g. RAW)
- jv_target_table: table name without prefix (e.g. customers)
- jv_target_full_table: fully qualified 'RAW.TMP_customers' when used

Best practices:
- Keep sensitive values in environment variables or keyvault.
- Export job JSONs (no credentials) for code reviews.

