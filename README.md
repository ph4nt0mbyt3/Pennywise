# Pennywise

This is a c# tinny version of Blackout: https://github.com/ZeroMemoryEx/Blackout

# Steps

1) Load and start the driver:

```
sc create Pennywise binPath="c:\path\to\driver.sys" type= kernel start= demand
sc start Pennywise
```
