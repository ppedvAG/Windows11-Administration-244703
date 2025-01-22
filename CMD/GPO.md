# GPO Befehle
Zum erzwungen update der Gruppenrichtlinien

```cmd
gpupdate /force
```

Abfrage der User Richtlinien, wenn der User Admin ist wird auch die Computerrrichtlinie angezeigt
```cmd
gpresult /r
```
Abfrage der Computer Richtlinie falls man mit einem anderen User die Elevated Shell öffnen muss.
```cmd
gpresult /r /scope:computer
```