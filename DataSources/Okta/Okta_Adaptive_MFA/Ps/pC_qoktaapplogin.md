#### Parser Content
```Java
{
Name = q-okta-app-login
    Vendor = Okta
    Product = Okta Adaptive MFA
    Lms = QRadar
    DataType = "app-login"
    TimeFormat = "yyyy-MM-dd'T'HH:mm:ss"
    Conditions = [ """"Sign-in successful,""", """,published"""", """,action"""" ]
    Fields=[
    """exabeam_host=([^=]{1,2000}@\s{0,100})?({host}[^\s]{1,2000})""",
    """\Wpublished"\s{0,100}:\s{0,100}"({time}\d\d\d\d\-\d\d\-\d\dT\d\d:\d\d:\d\d)""",
    """\WipAddress"\s{0,100}:\s{0,100}"({src_ip}[\da-fA-F\.:]{1,2000})""",
    """\Wmessage"\s{0,100}:\s{0,100}"({outcome}[^",]{1,2000})""",
    """"targets"\s{0,100}:\s{0,100}\[\{[^\]]{0,2000}?\WdisplayName"\s{0,100}:\s{0,100}"({user_fullname}[^",]{1,2000})""",
    """"targets"\s{0,100}:\s{0,100}\[\{[^\}]{0,2000}?\Wlogin"\s{0,100}:\s{0,100}"({user_email}[^",]{1,2000})""",
    """({app}Okta)""",
    """"actors":\[[^\]]{0,2000}?"id":"({user_agent}[^"]{1,2000}?),displayName[^\}]{0,2000}?objectType":"Client"""",
    """"actors":\[[^\]]{0,2000}?objectType":"Client"[^\}]{0,2000}?"id":"({user_agent}[^"]{1,2000}?),displayName""",
    #""""actors":\[.*?\{("?[^"]{1,2000}"\s{0,100}:\s{0,100}"([^"\\]|(\\\\)*\\"|\\)+"?,?)*"?objectType"\s{0,100}:\s{0,100}"Client",?("?[^"]{1,2000}"\s{0,100}:\s{0,100}([^"\\]|(\\\\)*\\"|\\)+",?)*"?id"\s{0,100}:\s{0,100}"({user_agent}[^"]{1,2000})"?,("?[^"]{1,2000}"\s{0,100}:\s{0,100}"([^"\\]|(\\\\)*\\"|\\)+"?,?)*\}\]""",
    #""""actors":\[.*?\{("?[^"]{1,2000}"\s{0,100}:\s{0,100}"([^"\\]|(\\\\)*\\"|\\)+"?,?)*"?id"\s{0,100}:\s{0,100}"({user_agent}[^"]{1,2000})"?,("?[^"]{1,2000}"\s{0,100}:\s{0,100}"([^"\\]|(\\\\)*\\"|\\)+"?,?)*"?objectType"\s{0,100}:\s{0,100}"Client",?("?[^"]{1,2000}"\s{0,100}:\s{0,100}"([^"\\]|(\\\\)*\\"|\\)+",?)*\}\]""",
  ]
  DupFields = [ "host->dest_host" ]
}
```