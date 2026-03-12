# SQL Injection

## Description
SQL Injection occurs when user input is inserted into SQL queries without proper sanitization.

## Example Payload
' OR '1'='1

## Impact
- Database data leakage
- Authentication bypass
- Data modification

## Prevention
- Parameterized queries
- Prepared statements
- Input validation
