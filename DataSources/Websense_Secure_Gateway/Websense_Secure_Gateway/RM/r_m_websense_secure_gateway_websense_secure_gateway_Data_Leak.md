Vendor: Websense Secure Gateway
===============================
### Product: [Websense Secure Gateway](../ds_websense_secure_gateway_websense_secure_gateway.md)
### Use-Case: [Data Leak](../../../../UseCases/uc_data_leak.md)

| Rules | Models | MITRE TTPs | Event Types | Parsers |
|:-----:|:------:|:----------:|:-----------:|:-------:|
|   3   |   1    |     3      |      1      |    1    |

| Event Type           | Rules                                                                                                                                                                                                                                                                                                                                                                        | Models                                                                          |
| -------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------- |
| web-activity-allowed | <b>T1030 - Data Transfer Size Limits</b><br> ↳ <b>A-WEB-EXFIL-ASSET</b>: Large amount of data exfiltrated from host<br> ↳ <b>WEB-New-File-20</b>: User with no web activity history has uploaded 20MB or more<br><br><b>T1071.001 - Application Layer Protocol: Web Protocols</b><br> ↳ <b>WEB-OUa-Browser-F</b>: First activity using this web browser for the organization |  • <b>WEB-OUa-Browser-New</b>: Top web browsers being used in this organization |