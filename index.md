## AZ-500 Notes: Microsoft Azure Security Technologies

## Useful Links
[Microsoft Certified: Azure Security Engineer Associate](https://docs.microsoft.com/en-us/learn/certifications/azure-security-engineer/)

Microsoft Learn Study Labs: [https://microsoftlearning.github.io/AZ500-AzureSecurityTechnologies/](https://microsoftlearning.github.io/AZ500-AzureSecurityTechnologies/)

ESI Study Guide: [https://aka.ms/ESIStudyGuide_AZ-500](https://aka.ms/ESIStudyGuide_AZ-500)

### Other Links
Check on Microsoft Learn latest trophies and badges to see current learning path.

[https://docs.microsoft.com/en-us/users/lucilyntangian-1724/](https://docs.microsoft.com/en-us/users/lucilyntangian-1724/)

## Notes
### Part 1: [Manage Identity and Access](https://docs.microsoft.com/en-us/learn/paths/manage-identity-access/)

I'm already in the middle of part 2 when creating this page. So, here's the pdf file: [AZ500new-notes1.pdf](AZ500new-notes1.pdf) for the notes with some phrases highlighted, screenshots, and knowledge checks.

### Part 2: [Implement platform protection](https://docs.microsoft.com/en-us/learn/paths/implement-platform-protection/)

This topic discusses perimeter, network, host, and container security. I just grabbed a jpeg to review on the OSI model. Here's a jpeg file I got from [https://www.networkcorner.co.uk/wp-content/uploads/2020/02/OSI_Model.jpeg](https://doragonoblesse.github.io/AZ-500-Notes/OSI_Model.jpeg)

First 2 modules: [AZ500new-notes2.pdf](AZ500new-notes2.pdf)

#### On doing the lab...

[Lab 07: Network Security Groups and Application Security Groups
Student lab manual](https://microsoftlearning.github.io/AZ500-AzureSecurityTechnologies/Instructions/Labs/LAB_07_NSGs.html#exercise-2-deploy-virtual-machines-and-test-network-filters)

Just follow the steps as instructed, they're pretty easily to follow. 

Take note that there's no need to remote login to the myVMWeb virtual machine to enable IIS.
Step 5. On the myVMWeb blade, in the Operations section, click Run command and then click RunPowerShellScript. 6. On the Run Command Script pane, run the following to install the Web server role on myVmWeb:

```markdown
Install-WindowsFeature -name Web-Server -IncludeManagementTools
```
It takes a while for it to finish.

Once finished, proceed to the next steps.

#### Clean up resources

Run this powershell command in the cloud shell to clean up resources.

```markdown
Remove-AzResourceGroup -Name "AZ500LAB07" -Force -AsJob
```




