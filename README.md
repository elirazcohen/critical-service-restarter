# Critical Service Restarter

A PowerShell automation script that monitors important Windows services, logs their status, and automatically restarts critical services when they stop.

Built as a self-taught sysadmin / IT automation project focused on service monitoring, logging, and recovery handling.

---

## Features

* Monitors multiple Windows services
* Automatically restarts stopped services
* Special handling for `CryptSvc`
* Timestamped logging system
* Error handling with `try/catch`
* Separate logs for critical services
* Lightweight and easy to customize

---

## Monitored Services

Default services included:

* `CryptSvc`
* `wuauserv`
* `BITS`
* `WinRM`

You can also pass your own services into the function.

---

## How It Works

The script:

1. Scans selected Windows services
2. Checks whether each service exists
3. Detects whether the service is running
4. Automatically restarts non-running services
5. Logs all events with timestamps
6. Applies special handling rules for `CryptSvc`

---

## Usage

### Run with default services

```powershell
scan-services
```

### Run with custom services

```powershell
scan-services -services "Spooler", "Dnscache"
```

---

## Log Files

The script generates log files inside the script directory:

| Log File           | Purpose                                     |
| ------------------ | ------------------------------------------- |
| `service_log.txt`  | General service monitoring and restart logs |
| `Cryptsvc_log.txt` | Dedicated logs for CryptSvc monitoring      |

---

## Example Output

```powershell
wuauserv restarted
BITS is running
WARNING: CryptSvc is stopped. Manual intervention recommended.
```

---

## Skills Demonstrated

* PowerShell scripting
* Windows service management
* Automation logic
* Error handling
* Logging systems
* Conditional workflows
* IT / Sysadmin troubleshooting

---

## Future Improvements

* Email or Discord alert integration
* Scheduled monitoring loop
* Config file support
* Windows Event Log integration
* Export logs to CSV
* Service dependency checks

---

## GitHub Description

> PowerShell script that monitors critical Windows services, automatically restarts failed services, and logs system events with timestamped tracking.

---

## Suggested GitHub Topics

```text
powershell windows automation sysadmin monitoring services logging cybersecurity windows-services
```
