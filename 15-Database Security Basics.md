

# Database Security Basics for CNSP Exam

Database security is a crucial aspect of network security, ensuring that sensitive data remains protected from unauthorized access, corruption, or leaks. Below is a structured breakdown of the essential database security concepts you need to know.

---

## 1. Database Security Fundamentals

### What is Database Security?

Database security refers to the protection of databases from unauthorized access, misuse, data breaches, and other threats. It involves a combination of:

- Access control mechanisms
- Encryption methods
- Auditing and monitoring
- Vulnerability management

### Common Threats to Database Security

1. SQL Injection (SQLi) – Malicious input to manipulate SQL queries.
2. Privilege Escalation – Unauthorized users gaining higher-level access.
3. Data Leaks – Exfiltration of sensitive information.
4. Denial of Service (DoS) Attacks – Overloading the database with excessive queries.
5. Insider Threats – Employees or administrators abusing their access.

---

## 2. Database Authentication & Access Control

### **Authentication** (Who can access the database?)

- Username & Password (Weakest form of authentication)
- Multi-Factor Authentication (MFA) (Best practice)
- Kerberos / LDAP Authentication (Centralized authentication)

### Access Control Mechanisms

Role-Based Access Control (RBAC): Users get permissions based on their role.  
Least Privilege Principle: Users should have only the minimum access required.

Example: Granting read-only access to a user in MySQL:

```sql
GRANT SELECT ON database_name.* TO 'user'@'host';
```

Example: Revoking write access in PostgreSQL:

```sql
REVOKE INSERT, UPDATE, DELETE ON table_name FROM role_name;
```

---

## 3. Database Encryption Techniques

Encryption helps protect sensitive data even if an attacker gains access.

### Types of Database Encryption

1. At-Rest Encryption – Encrypts data stored in the database.
    - Example: Transparent Data Encryption (TDE) in SQL Server, MySQL, and Oracle.
2. In-Transit Encryption – Protects data during transmission between client and server.
    - Example: SSL/TLS encryption for MySQL connections.
3. Column-Level Encryption – Encrypts specific sensitive columns.
    - Example: Encrypting credit card numbers in a user table.
4. Row-Level Encryption – Encrypts specific rows based on sensitivity.

Example: Enabling SSL in MySQL for secure connections

```sql
ALTER USER 'user'@'%' REQUIRE SSL;
```

---

## 4. Database Auditing & Monitoring

### Importance of Auditing

Auditing helps detect unauthorized access, policy violations, and suspicious activities.

### Common Auditing Methods

- Log Analysis: Store logs of all database transactions.
- Real-Time Alerts: Monitor unauthorized access attempts.
- User Activity Monitoring (UAM): Track queries executed by each user.

Example: Enabling database audit logs in PostgreSQL

```sql
ALTER SYSTEM SET log_statement = 'all';
```

---

## 5. SQL Injection Prevention

### What is SQL Injection (SQLi)?

SQL injection occurs when an attacker manipulates SQL queries by injecting malicious input.

### Preventive Measures

1. Use Prepared Statements & Parameterized Queries
    
    - Prevents user input from being treated as part of the SQL query.  
        Example (Python with MySQL):
    
    ```python
    cursor.execute("SELECT * FROM users WHERE username = %s", (username,))
    ```
    
2. Limit Database User Privileges
    - Use separate database users for different application components.
3. Input Validation & Whitelisting
    - Reject unexpected characters in user input.

---

## 6. Database Backup & Recovery

### Importance of Backups

Backups prevent data loss from cyber attacks, corruption, or hardware failures.

### Best Practices for Database Backups

- Automate Backups (Daily or real-time replication)
- Encrypt Backups (Protect from unauthorized access)
- Store Backups Offsite (Disaster recovery)

Example: Creating a MySQL Backup Using `mysqldump`

```sh
mysqldump -u root -p database_name > backup.sql
```

---

## 7. Security Hardening for Databases

### Key Hardening Techniques

1. Disable Unused Services (e.g., disable remote root login)
2. Restrict Database Network Access (Use firewalls)
3. Regularly Update Database Software (Patch vulnerabilities)
4. Implement Database Activity Monitoring (DAM) (Detect anomalies)

---

## 8. Compliance & Regulatory Requirements

Organizations must follow industry regulations for database security, such as:

- GDPR – Protects personal data in the EU.
- PCI DSS – Secures payment card information.
- HIPAA – Protects healthcare records.
- ISO 27001 – Global information security standard.

---



For the CNSP exam, focus on:  
✅ Database authentication & access control  
✅ Encryption methods for data at rest & in transit  
✅ SQL injection prevention techniques  
✅ Auditing, monitoring, and logging  
✅ Backup and disaster recovery strategies  
✅ Database hardening techniques



