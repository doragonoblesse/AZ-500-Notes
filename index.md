## AZ-500 Notes: Microsoft Azure Security Technologies

## Useful Links
[Microsoft Certified: Azure Security Engineer Associate](https://docs.microsoft.com/en-us/learn/certifications/azure-security-engineer/)

ESI Study Guide: [https://aka.ms/ESIStudyGuide_AZ-500](https://aka.ms/ESIStudyGuide_AZ-500)

### Other Links
Check on Microsoft Learn latest trophies and badges to see current learning path.

[https://docs.microsoft.com/en-us/users/lucilyntangian-1724/](https://docs.microsoft.com/en-us/users/lucilyntangian-1724/)

## Notes
### Part 1: [Manage Identity and Access](AZ500new-notes1.pdf)

I'm already in the middle of part 2 when creating this page. So, here's the pdf file: [AZ500new-notes1.pdf](AZ500new-notes1.pdf) for the notes with some phrases highlighted, screenshots, and knowledge checks.

### Part 2: [Implement platform protection](https://docs.microsoft.com/en-us/learn/paths/implement-platform-protection/)

This topic discusses perimeter, network, host, and container security. I just grabbed a jpeg to review on the OSI model. Here's a jpeg file I got from [https://www.networkcorner.co.uk/wp-content/uploads/2020/02/OSI_Model.jpeg](https://doragonoblesse.github.io/AZ-500-Notes/OSI_Model.jpeg)

First 2 modules: [AZ500new-notes2.pdf](AZ500new-notes2.pdf)

```markdown
Task 1 - Network security groups...(shortcut)
Configure an inbound rule to allow public access on port 80

1. Return to the Portal and the Networking blade.
2. Make a note of the virtual machines private IP address.
3. On the Inbound port rules tab, click Add inbound port rule. 
This rule will only allow certain IP address on port 80. 
As you go through the configuration settings be sure to discuss each one.
- Source: Service Tag
- Source service tag: Internet
- Destination: IP addresses
- Destination IP addresses/CIDR range: private_IP_address/32
- Destination port range: 80
- Protocol: TCP
- Action: Allow
- Name: Allow_Port_80
- Click Add

To test: http://public_IP_address/default.htm
```


