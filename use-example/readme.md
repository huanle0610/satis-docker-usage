```bash
HOST_IP=`ip -4 addr show scope global dev docker0 | grep inet | awk '{print \$2}' | cut -d / -f 1`
export HOST_IP=$HOST_IP && docker-compose run php7.1.18 ping amtf.org
export HOST_IP=$HOST_IP && docker-compose run php7.1.18 composer install
```