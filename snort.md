# Snort

**Running snort on a pcap** (rules have to be defined in the conf file):
```
snort -r file.pcap -c snort.conf
```

**Basic rule example**:
```
alert tcp any any -> $HOME_NET 22 (content:"/bin/sh"; msg:"Possible SSH buffer overflow"; )
```

**Example of rule with PCRE** (pcre: "/regex/flags"):
```
alert tcp any any -> any any(msg:"PDF is being downloaded"; pcre:"/.*site\/year\d\d\d\d.pdf/i"; sid: 100003; rev:3;)
```

**Help** :
* Hex encoding in content : `content:"|5c 00|P|00|I|00|P|00|E|00 5c|";`
* Characters ", | and ; must be escaped inside a content option with \ or hex encoding

**Performance rules**:
* Flow matters: `flow:to_client,established;` or `flow:to_server,established;`
* Use content to prefilter if you use PCRE


