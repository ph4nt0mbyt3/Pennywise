# Pennywise

This is a c# tinny version of Blackout: https://github.com/ZeroMemoryEx/Blackout

sample of vulnerable driver: https://www.loldrivers.io/drivers/7ce8fb06-46eb-4f4f-90d5-5518a6561f15/

Works with HVCI enabled: HVCI is designed to ensure the integrity of code executed in the kernel, but it cannot protect against all possible vulnerabilities or actions that can be performed through drivers or system interfaces.

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

# Recommendations

1) <a href="https://learn.microsoft.com/en-us/windows/security/threat-protection/windows-defender-application-control/microsoft-recommended-driver-block-rules">Windows recommended driver blocklist</a>
2) Enable HVCI to prevent code execution on kernel
3) Limit local privileges, audit and prevent privesc attacks.
