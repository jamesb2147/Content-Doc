#### Parser Content
```Java
{
Name = asa-web-activity-716003
  Vendor = Cisco
  Product = Cisco Adaptive Security Appliance
  Lms = Direct
  DataType = "web-activity"
  IsHVF = true
  TimeFormat = "MMM dd yyyy HH:mm:ss"
  Conditions = [ """%ASA-""", """-716003""", """WebVPN access GRANTED""" ]
  Fields = [
    """({time}\w+ \d\d \d\d\d\d \d\d:\d\d:\d\d) ({host}[\w\-.]{1,2000}) : %ASA-\d{1,100}-({event_code}\d{1,100}): .+? User <({user_email}[^>]{1,2000})> IP <({src_ip}[A-Fa-f:\d.]{1,2000})> ({event_name}WebVPN access ({action}[^:]{1,2000})):\s{0,100}(-|({full_url}({protocol}[^:\\\/]{1,2000}):[\\\/]{1,2000}({web_domain}[^\\\/:]{1,2000})({uri_path}\/[^\s\?]{0,2000})?({uri_query}\?[^\s]{1,2000})?))""",
   ]
}
```