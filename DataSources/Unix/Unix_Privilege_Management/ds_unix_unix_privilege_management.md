Vendor: Unix
============
Product: Unix Privilege Management
----------------------------------
| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|  10   |   7    |     4      |      1      |    1    |

|    Use-Case    | Event Types/Parsers    | MITRE TTP    | Content    |
|:----:| ---- | ---- | ---- |
| [Abnormal Authentication & Access](../../../UseCases/uc_abnormal_authentication_&_access.md) |  account-switch<br> ↳[upm-account-switch](Ps/pC_upmaccountswitch.md)<br> | T1078 - Valid Accounts<br>    | [<ul><li>1 Rules</li></ul><ul><li>1 Models</li></ul>](RM/r_m_unix_unix_privilege_management_Abnormal_Authentication_&_Access.md) |
|    [Brute Force Attack](../../../UseCases/uc_brute_force_attack.md)    |  account-switch<br> ↳[upm-account-switch](Ps/pC_upmaccountswitch.md)<br> | T1003 - OS Credential Dumping<br>T1078 - Valid Accounts<br>T1098 - Account Manipulation<br> | [<ul><li>5 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_unix_unix_privilege_management_Brute_Force_Attack.md)    |
|    [Malware](../../../UseCases/uc_malware.md)    |  account-switch<br> ↳[upm-account-switch](Ps/pC_upmaccountswitch.md)<br> | T1204 - User Execution<br>    | [<ul><li>4 Rules</li></ul><ul><li>2 Models</li></ul>](RM/r_m_unix_unix_privilege_management_Malware.md)    |
|    [Privilege Escalation](../../../UseCases/uc_privilege_escalation.md)    |  account-switch<br> ↳[upm-account-switch](Ps/pC_upmaccountswitch.md)<br> | T1003 - OS Credential Dumping<br>T1078 - Valid Accounts<br>T1098 - Account Manipulation<br> | [<ul><li>5 Rules</li></ul><ul><li>4 Models</li></ul>](RM/r_m_unix_unix_privilege_management_Privilege_Escalation.md)    |

ATT&CK Matrix for Enterprise
----------------------------
| Initial Access                                                      | Execution                                                           | Persistence                                                                                                                                  | Privilege Escalation                                                | Defense Evasion                                                     | Credential Access                                                          | Discovery | Lateral Movement | Collection | Command and Control | Exfiltration | Impact |
| ------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------- | --------- | ---------------- | ---------- | ------------------- | ------------ | ------ |
| [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [User Execution](https://attack.mitre.org/techniques/T1204)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br>[Account Manipulation](https://attack.mitre.org/techniques/T1098)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [Valid Accounts](https://attack.mitre.org/techniques/T1078)<br><br> | [OS Credential Dumping](https://attack.mitre.org/techniques/T1003)<br><br> |           |                  |            |                     |              |        |