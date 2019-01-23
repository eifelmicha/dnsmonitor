# dnsmonitor
Nagios/Icinga plugin to monitor for unauthorized changes in domain names.

Example config:
```json
{
  "gmail.com": {
    "A": ["216.58.211.133"],
    "AAAA": ["2a00:1450:400f:808::2005"],
    "MX": {
      "5" : ["gmail-smtp-in.l.google.com."],
      "10": ["alt1.gmail-smtp-in.l.google.com."],
      "20": ["alt2.gmail-smtp-in.l.google.com."],
      "30": ["alt3.gmail-smtp-in.l.google.com."],
      "40": ["alt4.gmail-smtp-in.l.google.com."]
    }
  }
}
```
Execution:
```
./dnsmonitor.py example.json
OK - 1 domains checked
```
