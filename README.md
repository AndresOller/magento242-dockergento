# Magento 2.4.2 Dockergento example for vuestorefront 2

This is a fork of https://github.com/ModestCoders/magento2-dockergento 🤟 created to test vuestorefront 2 with Magento 2.4.2.

---

## Prerequisites

Install dockergento. Instructions in https://github.com/ModestCoders/magento2-dockergento#installation

---

## Installation

Clone repo
```bash
git clone https://github.com/AndresOller/magento242-dockergento.git
```

Enter to project folder
```bash
cd magento242-dockergento
```

Start dockergento
```bash
dockergento start
```

Install modules
```bash
dockergento composer install
```

Get user and password in https://marketplace.magento.com/customer/accessKeys/


Dump of Magento 2.4.2 dockergento to test vuestorefront with data is in:

File path: 
```bash
./dump.sql
```

Import dump
```bash
cat dump.sql | dockergento docker-compose exec -T db mysql -uroot -ppassword magento
```

Copy env.php
```bash
cp --force app/etc/env.dev.php.template app/etc/env.php
```

🚀 By default run in http://localhost/