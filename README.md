🕵️‍♂️ Google Dorks Cheat Sheet for Hidden Paths & Exposed Files

| **Google Dork** | **What It Finds / Does** |
|------------------|--------------------------|
| `inurl:web.config` | Finds exposed ASP.NET configuration files. May contain DB connection strings, secrets. |
| `intitle:"index of" "web.config"` | Searches for open directory listings containing `web.config`. |
| `inurl:.htaccess` | Finds exposed `.htaccess` files used by Apache (can reveal rules, paths, restrictions). |
| `inurl:.htpasswd` | Looks for Apache password files (used with `.htaccess`). May reveal hashed passwords. |
| `inurl:.env` | Exposes `.env` files—used in Laravel, Node.js, etc. Often includes API keys, DB creds. |
| `ext:bak OR ext:old OR ext:backup inurl:admin` | Finds backup/old files in admin directories (may contain original code/configs). |
| `intitle:"index of" ".git"` | Shows exposed `.git` repositories—can leak full project source code. |
| `intitle:"index of" ".svn"` | Finds exposed Subversion (SVN) version control directories. |
| `filetype:sql "insert into" OR "create table"` | Searches for SQL database dumps, usually from MySQL or PostgreSQL. |
| `filetype:json "mongo" OR "password"` | Finds JSON files with MongoDB configs or other sensitive credentials. |
| `intitle:"index of" "error_log"` | Finds open error log files (can contain paths, errors, user info). |
| `intitle:"phpinfo()" "PHP Version"` | Locates PHP info pages — these expose server config, installed extensions. |
| `intitle:"index of" (config|backup|admin|database)` | Finds open directories with config/backup/admin/database files. |
| `inurl:wp-content/debug.log` | Finds exposed debug logs in WordPress installs — may include stack traces, errors. |


📌 Notes:
- You can combine dorks with `site:example.com` to limit results to a specific domain.
- Add `-github.com -stackoverflow.com` to reduce noise.
- These are useful for **bug bounty**, **pentesting**, or **security audits** (with permission!).

#sudo
