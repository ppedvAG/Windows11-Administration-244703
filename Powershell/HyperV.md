# Hyper V PowerShell Befehle


Zum aktivieren der Hyper V Prozessor Features der VM
```powershell
Set-VMProcessor -VMName Client1 -ExposeVirtualizationExtensions $true
```