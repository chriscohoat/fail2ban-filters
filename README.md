nginx-404.conf
=============

1) Add nginx-404.conf to /etc/fail2ban/filter.d

2) Add following to /etc/fail2ban/jail.conf

    [nginx-404]

    enabled = true
    port = http,https
    filter = nginx-404
    logpath = <NGINX_ACCESS_PATH>
    bantime = 600
    findtime = 600
    maxretry = 5

3) Adjust bantime/findtime/maxretry accordingly