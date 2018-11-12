# docker-graylog

Get default Graylog config
```bash
wget https://raw.githubusercontent.com/Graylog2/graylog-docker/2.4/config/graylog.conf
wget https://raw.githubusercontent.com/Graylog2/graylog-docker/2.4/config/log4j2.xml
```


Create mongo database and user
```text
show databases;

use graylog;

db.createUser(
  {
    user: "admin",
    pwd: "admin_pass",
    roles: [ { role: "root", db: "admin" } ]
  }
)

exit
```
