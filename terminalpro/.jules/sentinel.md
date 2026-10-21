## 2024-03-20 - Snowflake OAuth SQL Injection
**Vulnerability:** A SQL injection vulnerability was found in `backend-api/backend/api/auth_helpers.py` where a user-provided username from a request header (`Sf-Context-Current-User`) was interpolated directly into a Snowflake SQL `SHOW GRANTS TO USER {sf_user}` query without sanitization.
**Learning:** Even administrative or system commands like `SHOW GRANTS` in Snowflake require input sanitization, especially when taking input directly from request headers. Snowflake identifiers must be properly quoted and escaped.
**Prevention:** Always quote user-supplied identifiers using double quotes and escape any internal double quotes by doubling them (`identifier.replace('"', '""')`) before using them in raw SQL queries.
