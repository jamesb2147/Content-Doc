#### Parser Content
```Java
{
Name = cef-infowatch-web-activity-1
  Vendor = InfoWatch
  Product = InfoWatch
  Lms = ArcSight
  DataType = "web-activity"
  TimeFormat = "epoch"
  Conditions = [ """CEF:""", """|Mail in Browser|""", """|DLP|DLP TM""" ]
  Fields = [
    """\Wact=({action}.+?)(\s{1,100}[\w\.]{1,2000}=|\s{0,100}$)""",
    """\Wrt=({time}\d{1,100})""",
    """\Wsrc=({src_ip}[a-fA-F\d.:]{1,2000})""",
    """\Wsntdom=({user_email}.+?)(\s{1,100}[\w\.]{1,2000}=|\s{0,100}$)""",
    """\Wduser=({web_domain}.+?)(\s{1,100}[\w\.]{1,2000}=|\s{0,100}$)""",
    """\Wrequest=({full_url}(\w+:\/\/)?[^\/]{1,2000}?({uri_path}\/[^\?\s]{0,2000}?)({uri_query}\?.*?)?)(\s{1,100}[\w\.]{1,2000}=|\s{0,100}$)""",
    """\Wdvchost=({host}.+?)(\s{1,100}[\w\.]{1,2000}=|\s{0,100}$)""",
    """\Wdvc=({host}.+?)(\s{1,100}[\w\.]{1,2000}=|\s{0,100}$)""",   
  ]
}
```