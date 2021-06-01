# Git
  
  before start talking about Git, we should first know what is **Version Control**

  ## Version Control## 
    Version Control is a system that has been designated to give the users the ability check and revisit different versions of their own files. This system is working on recording every single modification could happen to the files. So, this records become available to be reverted to previous version, can be tracked to see what had been modified, and the changes on the files become able to be compared. As a result, these abilities will become easily correctable in case if any mistake happend before.

  ## Local Version Control (LVCS)
    Local VCS contains one database on your hard disk that stores changes to files.

  ## Centralized Version Control (CVCS)
    CVCS contains single server storing all modifications and decument versions, and it can be accessed by various clients.
    This type of Version Control System allows you to see the acctivities done by your team members.

  ## Distributed Version Control (DVCS) ##
    DVCS addresses the major vulnerability of the CVS, that is the server failure. And that is done by allowing the clients to create mirrored repositories, which is a data backups that can be easily placed on the server to replace any lost information.

Now let's talk about Git:

## Git ##

   * Git is a DVCS that uses a file system made by snapshots to store data. whenever you trying to save a modified version of your project, Git stores a referance to it using snapshote.

   * Because most important data can be found in the local resources, Git most depends on local operations.

   * Git track any changes could be done to any file.

   * A really good specification for Git, is that it makes it really hard for snapshot of your file that is stored to be lost.
