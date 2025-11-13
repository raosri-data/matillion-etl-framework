# matillion-etl-framework

Purpose: Reusable Matillion orchestration & transformation patterns for incremental loads into Snowflake.

Highlights:
- Control-table driven orchestration pattern
- Use of Matillion job variables for schema/table naming
- Example SQL used in Database Query components (sanitized)
- Guidance for handling TRUNCATE TABLE with dynamic variables

Example SQL snippet (Database Query component):
```sql
-- Use a full variable for table identifier or IDENTIFIER() in Snowflake
TRUNCATE TABLE IDENTIFIER('{{ jv_target_schema }}.TMP_{{ jv_target_table }}');
```

Files:
- docs/architecture.md — design notes
- examples/job_example.json — sanitized exported job snippet (placeholder)
