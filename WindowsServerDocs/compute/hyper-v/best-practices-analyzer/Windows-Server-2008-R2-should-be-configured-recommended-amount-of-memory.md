---
title: Windows Server 2008 R2 should be configured with the recommended amount of memory
description: " "
ms.prod: windows-server-threshold
ms.service: na
manager: timlt
ms.technology: compute-hyper-v
ms.author: kathydav
ms.topic: article
ms.assetid: 26872519-ccf0-4757-827f-8df2a7a2b9f9
author: KBDAzure
ms.date: 8/16/2016
---
# Windows Server 2008 R2 should be configured with the recommended amount of memory

>Applies To: Windows Server Technical Preview

[This information is preliminary and subject to change.]  
  
For more information about best practices and scans, see [Best Practices Analyzer](http://go.microsoft.com/fwlink/?LinkId=122786).  
  
|Property|Details|  
|-|-|  
|**Operating System**|Windows Server 2016 Technical Preview|  
|**Product/Feature**|Hyper-V|  
|**Severity**|Warning|  
|**Category**|Configuration|  
  
In the following sections, italics indicates UI text that appears in the Best Practices Analyzer tool for this issue.  
  
## Issue  
  
*A virtual machine running Windows Server 2008 R2 is configured with less than the recommended amount of RAM, which is 2 GB.*  
  
## Impact  
  
*The guest operating system and applications might not perform well. There might not be enough memory to run multiple applications at once. This impacts the following virtual machines:*  
  
\<list of virtual machine names>  
  
## Resolution  
  
*Use Hyper-V Manager to increase the memory allocated to this virtual machine to at least 2 GB.*  
  
### To increase the memory using Hyper-V Manager  
  
1.  Open Hyper-V Manager. Click **Start**, point to **Administrative Tools**, and then click **Hyper-V Manager**.  
  
2.  In the results pane, under **Virtual Machines**, select the virtual machine that you want to configure. The state of the virtual machine should be listed as **Off**. If it is not, right-click the virtual machine and then click **Shut Down**.  
  
3.  In the **Action** pane, under the virtual machine name, click **Settings**.  
  
4.  In the navigation pane, click **Memory**.  
  
5.  On the **Memory** page, set the **Startup RAM** to at least 2 GB and then click **OK**.  
  
### Increase the memory using Windows PowerShell  
  
1.  Open Windows PowerShell. (From the desktop, click **Start** and start typing **Windows PowerShell**.)  
  
2.  Right-click **Windows PowerShell** and click **Run as administrator**.  
  
3.  Run this command after replacing \<MyVM> with the name  of your virtual machine:  
  
```  
Set-VMMemory <MyVM> -StartupBytes 2GB  
```  
  
## See Also  
[Set-VMMemory](https://technet.microsoft.com/library/hh848572.aspx)  
  

