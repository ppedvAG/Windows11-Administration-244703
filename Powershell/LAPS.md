# LAPS cmdlet

Local Administrator Password Solution

Erweitern des Ad Schemas auf dem Schemamaster
```powershell
Update-LapsADSchema
```
Setzen der Berechtigung das das Computerkonto das Password in sein eigenes Objekt schreiben darf
```powershell
Set-LapsADComputerSelfPermission -Identity "OU=Struktur,DC=ppedv,DC=test"
```
Finden vielleicht bereits bestehender Berechtigungen
```powershell
Find-LapsADExtendedRights -Identity "OU=Struktur,DC=ppedv,DC=test"
```
Setzen der Read Permission auf eine Domänen lokale Gruppe, um zb einem Helpdesk das Recht zu geben die lokalen Admin Kennwörter auszulesen, ohne das der Helpdesk selber lokale AdminRechte benötigt.
```powershell
Set-LapsADReadPasswordPermission -Identity "OU=Struktur,DC=ppedv,DC=test" -AllowedPrincipals "ppedv\DL-LAPS-R"
```