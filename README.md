Standard Storage Azure VM preconfigured for max storage performance
===================================================================

            

This script sample demonstrates how to utilize Azure PowerShell to deploy a Windows based virtual machine from the Azure image gallery and configure Storage Spaces to get the highest storage performance currently available.


Script functionality:


  *  Checks to make sure you have the proper version of Azure PowerShell installed (greater than or equal to 0.8.14)

  *  Launches secure user interface to authenticate with an Azure account 
  *  Presents option to choose an Azure Subscription 
  *  Presents option to select an Azure datacenter for virtual machine to reside 
  *  Automates building of unique [locally redundant](http://msdn.microsoft.com/en-us/library/azure/dn133149.aspx) storage account for selected virtual machine per [best practices](http://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/#storagelimits) (Do not place more than 40 highly used VHDs in an account to avoid the 20,000 IOPS limit.)

  *  Automates username and password creation for virtual machine 
  *  Presents option to choose a VM size which permits higher I/O loads 
  *  Presents option to select from latest virtual machine images available in the Azure image gallery

  *  Attaches the maximum number of one terabyte data disks allowable for selected virtual machine size ([See Azure storage pricing details](http://azure.microsoft.com/en-us/pricing/details/storage/) for more information.  Storage
 is charged on a per-usage basis) 
  *  Connects to the newly created VM and automates the creation and configuration of a Storage Space for
[maximum performance](http://social.technet.microsoft.com/wiki/contents/articles/15200.storage-spaces-designing-for-performance.aspx)

  *  Configures the number of columns that match number of attached data disks 

  *  Configures the Interleave and Allocation Unit Size 





Recommendations to follow:


[Set up monitoring for storage account throttling](http://blogs.msdn.com/b/wats/archive/2014/08/02/how-to-monitor-for-storage-account-throttling.aspx)
[Insure that that you follow best practices for SQL Server in Azure virtual machines](http://msdn.microsoft.com/en-us/library/azure/dn133149.aspx)


 


* Update 10/1/14


Added D-series VM creation options. [D-Series Virtual Machine](http://azure.microsoft.com/blog/2014/09/22/new-d-series-virtual-machine-sizes/) sizes have a solid-state drive (SSD) for the temporary disk.


* Update 2/23/15


Allows for any supported Virtual Machine size based on selected Azure region
Allows for any Windows based Virtual Machine deployed from Azure gallery based on selected Azure region


* Update 3/18/15


Allows for selection of storage spaces stripe value.


** If you choose download the file right-click on the Azure_High_IO.ps1 from File Explorer and choose Properties. On the General tab, change the security setting to “unblock”.

 
 
 
 

 
 



Standard_D14



        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
