# Microsoft Exchange 2016

## Installing Cumulative Updates

The process for installation is as follows:

1. Perform the Active Directory schema changes and updates. This is performed once for the entire Active Directory environment. You do not need to repeat this for each server being upgraded.

2.  Upgrade servers. For each server in turn:
    - Place the server into maintenance mode.
    - Install the update.
    - Perform testing.
    - Take the server out of maintenance mode.
3. Perform post-installation tasks:
   - Rebalance database availability groups.
   - Restore customizations.
   - Perform a health check of the environment.

```powershell
[PS] C:\>Set-ServerComponentState SERVER –Component ServerWideOffline –State Active –Requester Maintenance

[PS] C:\>Resume-ClusterNode –Name SERVER

Name        ID      State
----        --      -----
SERVER      1       Up

[PS] C:\>Set-MailboxServer SERVER –DatabaseCopyAutoActivationPolicy Unrestricted

[PS] C:\>Set-MailboxServer SERVER –DatabaseCopyActivationDisabledAndMoveNow $false

[PS] C:\>Set-ServerComponentState SERVER –Component HubTransport –State Active –Requester Maintenance

[PS] C:\>cd $exscripts

[PS] C:\Program Files\Microsoft\Exchange Server\V15\scripts\>.\RedistributeActiveDatabases.ps1 -DagName DAGNAME -BalanceDbsByActivationPreference
```