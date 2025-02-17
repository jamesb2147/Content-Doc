#### Parser Content
```Java
{
Name = cisco-wsa-squid-proxy
    Vendor = Cisco
    Product = Cisco Secure Web Appliance
    Lms = Splunk
    DataType = "web-activity"
    IsHVF = true
    TimeFormat = "epoch_sec"
    Conditions = [ """cisco:wsa:squid"""]
    Fields = [
		"""({time}\d{10})\.\d{3}""",
		"""exabeam_host=({host}[^\s]{1,2000})""",
		"""\s{1,100}({host}[^\s:]{1,2000}):?\s{1,100}Info:""",
		"""\d{10}\.\d{3}\s{1,100}[^\s]{1,2000}\s(?:-|({src_ip}[^\s]{1,2000}))""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){2}(?:-|({proxy_action}.+?)(\/(?:-|({result_code}\d{1,100})))?)\s{1,100}""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){4}(?:-|({method}[^\s]{1,2000}))""",
        """\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){5}(?:-|({full_url}(({protocol}[^:]{1,2000}):\/+)?[^\s:\/]{1,2000}(:({dest_port}\d{1,100}))?\/(?:-|({uri_path}[^?\s]{1,2000}))?({uri_query}\?[^\s]{1,2000})?))""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){6}"{1,20}(?:-|({domain}[^\\]{1,2000})\\+({user}[^@"]{1,2000}))""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){5}(\w+:\/+)?({web_domain}(?:({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})|[^\s\/:]{1,2000}))""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){9}(?:-|({action}[^\s-]{1,2000}))""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){8}(?:-|({mime}[^\s]{1,2000}))""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){10}.*?"\s{1,100}({dest_ip}\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3})\s{1,100}"""",
		"""\s{1,100}<.+?>.+?\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}\s{1,100}".+?"\s{1,100}"({category}[^"]{1,2000})""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){9}[^\s]{1,2000}\s{1,100}<(?:-|nc|({category}[^,>]{1,2000}))""",
		"""\d{10}\.\d{3}\s{1,100}([^\s]{1,2000}\s){9}[^\s]{1,2000}\s{1,100}<[^>]{1,2000}>\s{1,100}[^\s]{1,2000}\s{1,100}"{1,20}(?:[\s-]|({user_agent}[^"]{1,2000}))""",
    ]
  }
```