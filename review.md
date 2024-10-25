
### 10.50.25.33 - Windows
### 10.50.30.239 - Linux

# Review
## Forms of Persistence

### Linux
- Cron
  - /etc/crontab
  - /var/spool/cron
  - /etc/cron.d
- /etc/init [^1]
- /etc/profile
- /etc/environment
- /etc/inittab [^1]
- /etc/rc.d/rc0.d/ [^1]
- /lib/systemd/systemd [^2]
- /usr/lib/systemd/system [^2]
- Services/Processes
  - ps -elf
  - top or htop
  - systemctl status <PID> [^2]
  
  [^1]: Only for SysV systems
  [^2]: Only for systemd systems

### Windows
- schtasks
- Registry Locations
- Powershell Profile
- `Test-Path -Path $profile.currentUsercurrentHost`
- Services/Processes
- `Get-Service`
- `Get-Process -id <PID>`
- `Get-CimInstance`
- win32_service
- Artifacts
    - BAM
    - Prefetch
    - Userassist
    - Registry Key
 
## Obfuscation
Ports that look weird:
- Repeating (4444)
- Sequential (1234)
Things attackers do to hide:
- Taking name of something legit ex: GoogleUpdate
- Abnormal for Govt device, ex: steam, netflix
- Mispellings of words
- C:\windows\system32
- C:\users\public\downloads\svchost.exe (for example)

net use * https://live.sysinternals.com

