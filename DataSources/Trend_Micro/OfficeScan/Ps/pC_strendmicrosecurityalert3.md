#### Parser Content
```Java
{
Name = s-trendmicro-security-alert-3
  Vendor = Trend Micro
  Product = OfficeScan
  Lms = Splunk
  DataType = "alert"
  TimeFormat = "M/dd/yyyy HH:mm:ss"
  Conditions = [ """TMCM:EVT_URL_CONTENT_FILTERING""" ]
  Fields = [
    """\sEvent time \(local\)="({time}\d{1,100}\/\d{1,100}\/\d\d\d\d \d\d:\d\d:\d\d)""",
    """({host}[\w.\-]{1,2000})\s{1,100}TMCM:({alert_type}\w+)""",
    """\sURL="({malware_url}[^"]{1,2000})""",
    """\sDestination IP="({dest_ip}[^"]{1,2000})""",
    """\sDomain="({domain}[^"]{1,2000})""",
    """\sClient host name="({src_host}[^"]{1,2000})""",
    """\sSource IP="({src_ip}[^"]{1,2000})""", 
  ]
  DupFields = [ "alert_type->alert_name" ]
}
```