# MISCONF Redis is configured to save RDB snapshots... error

vi /etc/redis.conf   
```
stop-writes-on-bgsave-error no
```
redis-cli shutdown NOSAVE   
redis-server --protected-mode no   

または   
redis-cliで   
```config set stop-writes-on-bgsave-error no```
と打つ。ただし、永久措置ではない。

# DENIED Redis is running in protected mode because protected mode is enabled... ERROR
 
vi /etc/redis.conf
```
protected-mode no
```
redis-cli shutdown NOSAVE   
redis-server --protected-mode no   



