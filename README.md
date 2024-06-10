# Comandi Utili

Questo repository raccoglie una serie di comandi utili per vari sistemi operativi come Windows e Linux.

## Indice

- [Windows](#windows)
- [Linux](#linux)
- [MacOS](#macos)
- [Multi](#multi)

## Windows

### 1. Stampare il valore di una env (es. USERPROFILE)
```cmd
echo $env:USERPROFILE
```

### 2. Creare un task nello scheduler (es. script eseguito ogni 5 minuti)
```cmd
schtasks /create /sc minute /mo 5 /tn "RunPowerShellScript" /tr "powershell.exe -File %USERPROFILE%\scripts\your_script.ps1" /f
```

### 2. Controllare lo stato di una porta
```cmd
netstat -ano | wsl grep "80"
```


## Linux

### 1. Cercare una stringa in diverse cartelle
```bash
find . -name "file.txt" -exec grep -H "string" {} \;
```


## MacOS

### 1. Gestire gli hostname
```bash
sudo scutil --set ComputerName "system"
sudo scutil --set HostName "system"
sudo scutil --set LocalHostName "system"
```

## Multi

```cmd
terraform apply -refresh-only    # Aggiornare lo state
terraform force-unlock 1db462f1-b2be-c5f4-2238-8604f079hdcg    # Fare Unlock di uno stato
openssl s_client -connect server_hostname:port -tls1_2    # Check connettività TLS
az ad sp create-for-rbac --name terraform --role Contributor --scopes /subscriptions/<subscription_id>    # Crea un Service Principal
```

