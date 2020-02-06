# MISCONF Redis is configured to save RDB snapshots... error

vi /etc/redis.conf   
```
stop-writes-on-bgsave-error no
```
systemctl restart redis

または   
redis-cliで   
```config set stop-writes-on-bgsave-error no```
と打つ。ただし、永久措置ではない。
