# Powershell cmdlet To Bitlocker

[BitLocker PowerShell Doku](https://learn.microsoft.com/en-us/powershell/module/bitlocker/?view=windowsserver2025-ps)

```powershell
Get-BitLockerVolume -MountPoint C:
```

Backup Bitlocker Wiederherstellungskey to Active Directory
```powershell
$BLV = Get-BitLockerVolume -MountPoint C:
Backup-BitLockerKeyProtector -MountPoint C: -KeyProtectorId $BLV.KeyProtector[1].KeyProtectorId
```

Backup Bitlocker Wiederherstellungskey to Azure Active Directory
```powershell
$BLV = Get-BitLockerVolume -MountPoint C:
BackupToAAD-BitLockerKeyProtector -MountPoint C: -KeyProtectorId $BLV.KeyProtector[1].KeyProtectorId
```