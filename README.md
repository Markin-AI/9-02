# Домашнее задание к занятию "`Система мониторинга Zabbix`" - `Маркин Алексей`

### Задание 1

Установите Zabbix Server с веб-интерфейсом.

### Решение 1

![Скриншот 1](https://github.com/Markin-AI/9-02/blob/main/img/1-1.png)

# wget https://repo.zabbix.com/zabbix/7.0/ubuntu/pool/main/z/zabbix-release/zabbix-release_7.0-2+ubuntu22.04_all.deb
# dpkg -i zabbix-release_7.0-2+ubuntu22.04_all.deb
# apt update
# apt install zabbix-server-pgsql zabbix-frontend-php php8.1-pgsql zabbix-apache-conf zabbix-sql-scripts
# sudo -u postgres createuser --pwprompt zabbix
# sudo -u postgres createdb -O zabbix zabbix
# zcat /usr/share/zabbix-sql-scripts/postgresql/server.sql.gz | sudo -u zabbix psql zabbix

---

### Задание 2

Установите Zabbix Agent на два хоста.

### Решение 2

![Скриншот 1](https://github.com/Markin-AI/9-02/blob/main/img/2-1.png)

![Скриншот 2](https://github.com/Markin-AI/9-02/blob/main/img/2-2.png)

![Скриншот 3](https://github.com/Markin-AI/9-02/blob/main/img/2-3.png)

![Скриншот 4](https://github.com/Markin-AI/9-02/blob/main/img/2-4.png)

# apt install zabbix-agent
# systemctl enable zabbix-agent
# systemctl restart zabbix-agent

---
