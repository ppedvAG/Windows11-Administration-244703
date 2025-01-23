# Powershell cmdlet To Bitlocker

[BitLocker PowerShell Doku](https://learn.microsoft.com/en-us/powershell/module/bitlocker/?view=windowsserver2025-ps)

```powershell
# Dieser Befehl zeigt Informationen über das BitLocker-Volume auf Laufwerk C: an.
Get-BitLockerVolume -MountPoint C:
```

```powershell
# Dieser Befehl speichert die BitLocker-Schlüsselprotektoren für das Volume auf Laufwerk C: in einer Variablen.
$BLV = Get-BitLockerVolume -MountPoint C:
# Dieser Befehl sichert den BitLocker-Schlüsselprotektor für das Volume auf Laufwerk C: in einem Backup.
Backup-BitLockerKeyProtector -MountPoint C: -KeyProtectorId $BLV.KeyProtector[1].KeyProtectorId
```

```powershell
# Dieser Befehl speichert die BitLocker-Schlüsselprotektoren für das Volume auf Laufwerk C: in einer Variablen.
$BLV = Get-BitLockerVolume -MountPoint C:
# Dieser Befehl sichert den BitLocker-Schlüsselprotektor für das Volume auf Laufwerk C: in Azure Active Directory.
BackupToAAD-BitLockerKeyProtector -MountPoint C: -KeyProtectorId $BLV.KeyProtector[1].KeyProtectorId
```