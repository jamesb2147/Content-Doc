#### Parser Content
```Java
{
Name = sangfor-web-activity
  Vendor = Sangfor
  Product = NGAF
  Lms = Direct
  DataType = "web-activity"
  IsHVF = true
  TimeFormat = "yyyy-MM-dd HH:mm:ssZ"
  Conditions = [ """type: website browsing""", """<Identifier>ZC01_NTTDHK-FWL-002</Identifier>""" ]
  Fields = [
    """({time}\d\d\d\d-\d\d-\d\d \d\d:\d\d:\d\d[\+\-]\d{1,100}:\d{1,100})\s{1,100}\S+\s{1,100}fwlog:""",
    """<Identifier>ZC01_({host}[\w\-.]{1,2000})<\/Identifier>""",
    """user:\s{0,100}\((null|({user}[^\s\)]{1,2000}))\)""",
    """policy name:\s{0,100}({policy}[^,"]{1,2000})""",
    """Src IP:\s{0,100}({src_ip}[A-Fa-f:\d.]{1,2000})""",
    """Dst IP:\s{0,100}({dest_ip}[A-Fa-f:\d.]{1,2000})""",
    """application:\s{0,100}({categories}({category}[^;,"]{1,2000})[^,]{0,2000})""",
    """action:\s{0,100}({action}[^,"]{1,2000})""",
    """URL:\s{0,100}(-|({full_url}(({protocol}[^:\\\/\s,"]{1,2000}):[\\\/]{1,2000})?({web_domain}[^\\\/\s:,"]{1,2000})(:({dest_port}\d{1,100}))?({uri_path}\/[^\s\?",]{0,2000})?({uri_query}\?[^"\s]{0,2000})?))"""",
  ]
  DupFields = [ "action->outcome" ]
}
```