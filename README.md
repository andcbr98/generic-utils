# Comandi Utili

Questo repository raccoglie una serie di comandi utili per vari sistemi operativi come Windows e Linux.

## Indice

- [Windows](#windows)
- [Linux](#linux)
- [MacOS](#macos)
- [Altri Sistemi](#altri-sistemi)

## Windows

### 1. Stampare il valore di una env (es. USERPROFILE)
```cmd
echo $env:USERPROFILE
```

### 2. Creare un task nello scheduler (es. script eseguito ogni 5 minuti)
```cmd
schtasks /create /sc minute /mo 5 /tn "RunPowerShellScript" /tr "powershell.exe -File %USERPROFILE%\scripts\your_script.ps1" /f
```

## Linux

### 1. Cercare una stringa in diverse cartelle
```bash
find . -name "file.txt" -exec grep -H "string" {} \;
```


## MacOS


## Altri Sistemi

```cmd
terraform apply -refresh-only
terraform force-unlock 1db462f1-b2be-c5f4-2238-8604f079hdcg
```

