#### Parser Content
```Java
{
Name = ibm-web-activity
  Vendor = IBM
  Product = IBM Security Access Manager
  Lms = Direct
  DataType = "web-activity"
  TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
  Conditions = ["""webseald""" ]
  Fields = [
    """exabeam_host=({host}[\w.\-]{1,2000})""",
    """({time}\d\d\d\d-\d\d-\d\dT\d\d:\d\d:\d\d)-\d\d:\d\d\s({host}[^\s]{1,2000})\s""",
    """webseald\s\d{1,100}\s(.*?\s){4}(-|({user}[^\s]{1,2000}))""",
    """"({request}({method}[^\s]{1,2000})\sHTTPS*:\/\/({full_url}[^\s]{1,2000}))\s({protocol}[^\/]{1,2000}).*?"\s({result_code}\d{1,100})\s(-|\d{1,100})\s.*?\s(-|({src_ip}\d{1,3}.\d{1,3}.\d{1,3}.\d{1,3}))"""
  ]
}
```