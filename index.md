## AZ-500 Notes: Microsoft Azure Security Technologies

## Useful Links

- [Microsoft Certified: Azure Security Engineer Associate](https://docs.microsoft.com/en-us/learn/certifications/azure-security-engineer/)

- Microsoft Learn Study Labs: [https://microsoftlearning.github.io/AZ500-AzureSecurityTechnologies/](https://microsoftlearning.github.io/AZ500-AzureSecurityTechnologies/)

- ESI Study Guide: [https://aka.ms/ESIStudyGuide_AZ-500](https://aka.ms/ESIStudyGuide_AZ-500)

### Other Links
- Check on Microsoft Learn latest trophies and badges to see current learning path.

  [https://docs.microsoft.com/en-us/users/lucilyntangian-1724/](https://docs.microsoft.com/en-us/users/lucilyntangian-1724/)

## Notes
### Part 1: [Manage Identity and Access](https://docs.microsoft.com/en-us/learn/paths/manage-identity-access/)

I'm already in the middle of part 2 when creating this page. So, here's the pdf file: [AZ500new-notes1.pdf](AZ500new-notes1.pdf) for the notes with some phrases highlighted, screenshots, and knowledge checks.

### Part 2: [Implement platform protection](https://docs.microsoft.com/en-us/learn/paths/implement-platform-protection/)

This topic discusses perimeter, network, host, and container security. I just grabbed a jpeg to review on the OSI model. Here's a jpeg file I got from [https://www.networkcorner.co.uk/wp-content/uploads/2020/02/OSI_Model.jpeg](https://doragonoblesse.github.io/AZ-500-Notes/OSI_Model.jpeg)

#### [Implement perimeter security](https://docs.microsoft.com/en-us/learn/modules/perimeter-security/) & [Configure network security](https://docs.microsoft.com/en-us/learn/modules/network-security/)
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
  Remove-AzResourceGroup -Name "`resource-group-name`" -Force -AsJob
  ```
#### [Configure and manage host security](https://docs.microsoft.com/en-us/learn/modules/host-security/)

  **Enable endpoint protection** -
  1. install antimalware; 
  2. integrate your antimalware solution with Azure Security Center to monitor the status of the antimalware protection.

  **Define a privileged access device strategy includes** -
  
  Hardware root-of-trust
  
   - Trusted Platform Module TPM 2.0
  
   - BitLocker Drive Encryption
    
   - UEFI Secure Boot
    
   - Drivers and Firmware Distributed through Windows Update
    
   - Virtualization and HVCI Enabled
    
   - Drivers and Apps HVCI-Ready
    
   - Windows Hello
    
   - DMA I/O Protection
    
   - System Guard
    
   - Modern Standby
   
  **Levels of device security** - [see image](https://github.com/doragonoblesse/AZ-500-Notes/blob/gh-pages/levels%20of%20device%20security.jpg)
   
  **Device security controls** - [see image](https://github.com/doragonoblesse/AZ-500-Notes/blob/gh-pages/Device%20security%20controls.jpg)
   
  **Privileged Access Workstations** -
   
  (PAW) is a hardened and locked down workstation designed to provide high security assurances for sensitive accounts and tasks. PAWs are recommended for administration of identity systems, cloud services, and private cloud fabric as well as sensitive business functions.
   
  Administrative Privileges - PAWs provide increased security for high impact IT administrative roles and tasks. This architecture can be applied to administration of many types of systems including Active Directory Domains and Forests, Microsoft Azure Active Directory tenants, Microsoft 365 tenants, Process Control Networks (PCN), Supervisory Control and Data Acquisition (SCADA) systems, Automated Teller Machines (ATMs), and Point of Sale (PoS) devices.

  High Sensitivity Information workers - The approach used in a PAW can also provide protection for highly sensitive information worker tasks and personnel such as those involving pre-announcement Merger and Acquisition activity, pre-release financial reports, organizational social media presence, executive communications, unpatented trade secrets, sensitive research, or other proprietary or sensitive data. This guidance does not discuss the configuration of these information worker scenarios in depth or include this scenario in the technical instructions.
   
  **Jump Box** -

  Administrative "Jump Box" architectures set up a small number administrative console servers and restrict personnel to using them for administrative tasks. This is typically based on remote desktop services, a 3rd-party presentation virtualization solution, or a Virtual Desktop Infrastructure (VDI) technology.

  This approach is frequently proposed to mitigate risk to administration and does provide some security assurances, but the jump box approach by itself is vulnerable to certain attacks because it violates the clean source principle. The clean source principle requires all security dependencies to be as trustworthy as the object being secured.
  
#### Creating Virtual Machine Templates
  
  **Resource Manager** -
  
  Here are some additional terms to know when using Resource Manager:

  - Resource provider. A service that supplies Azure resources. For example, a common resource provider is Microsoft.Compute, which supplies the VM resource. Microsoft.Storage is another common resource provider.

  - Resource Manager template. A JSON file that defines one or more resources to deploy to a resource group or subscription. You can use the template to consistently and repeatedly deploy the resources.

  - Declarative syntax. Syntax that lets you state, "Here’s what I intend to create" without having to write the sequence of programming commands to create it. The Resource Manager template is an example of declarative syntax. In the file, you define the properties for the infrastructure to deploy to Azure.

  !Important: When you deploy a template, Resource Manager converts the template into REST API operations.

#### Enable and secure remote access management

**Connect to a Windows VM** - by using Remote Desktop Protocol (RDP); If you are using PowerShell and have the Azure PowerShell module installed you may also connect using the `Get-AzRemoteDesktopFile` cmdlet.

**Connect to a Linux-based VM** - To connect the Linux-based VM, you need a secure shell protocol (SSH) client. The most used free tool is PuTTY SHH terminal. The following shows the PuTTY configuration dialog.
  



