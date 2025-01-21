
Zum suchen von Befehlen
```powershell
Get-Command
```


Dieser Befehel kann verwendet werden das Gerät der Domäne "ppedv.test" zu joinen und gleichzeitig umzubennen. Als DomainCredential empfiehlt sich immer die Domäne mit anzugeben.
```powershell
Add-Computer -DomainName ppedv.test -NewName Client1 -DomainCredential ppedv\Administrator
```

Dieser Befehl kann verwendet das Gerät umzubennen.

```powershell
Rename-Computer -NewName Client1
```