### timezone変更
```
# date  
Tue Dec 17 10:07:12 UTC 2019  

# strings /etc/localtime  
TZif2  
TZif2  
UTC0  
```
UTCになってる  

JSTに変更  
```ln -sf  /usr/share/zoneinfo/Asia/Tokyo /etc/localtime```  

```
# strings /etc/localtime
TZif2
TZif2
JST-9

# date  
Tue Dec 17 19:11:44 JST 2019
```
JSTになってる

```
# vi /etc/sysconfig/clock
ZONE="UTC"
UTC=true
```
このままでは再起動したらUTCに戻るので、falseにする

あと、crondも再起動しないといけない  
```systemctl restart crond```
