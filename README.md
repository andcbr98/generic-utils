## Windows

```powershell
echo $env:USERPROFILE

schtasks /create /sc minute /mo 5 /tn "RunPowerShellScript" /tr "powershell.exe -File %USERPROFILE%\scripts\your_script.ps1" /f

netstat -ano | wsl grep "80"
```

## Linux (All distros)

```sh
find . -name "file.txt" -exec grep -H "string" {} \;  

strace -p <pid>   

rsync -avz -e ssh /source/directory user@remote_host:/destination/directory
```

### Arch

```sh
sudo pacman -Sy archlinux-keyring

sudo pacman-key --init

sudo pacman-key --populate archlinux

sudo pacman-key --list-keys
```
## MacOS

```sh
sudo scutil --set ComputerName "system"

sudo scutil --set HostName "system"

sudo scutil --set LocalHostName "system"
```

## Terraform

```sh
terraform apply -refresh-only

terraform fmt -recursive

terraform force-unlock 1db462f1-b2be-c5f4-2238-8604f079hdcg   

az ad sp create-for-rbac --name terraform --role Contributor --scopes /subscriptions/<subscription_id>  
```

## OpenSSL

```sh
openssl s_client -connect server_hostname:port -tls1_2
```

## K8S on Linux/WSL

```sh
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64

sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

curl -fsSL https://get.docker.com -o get-docker.sh

sh get-docker.sh

sudo usermod -aG docker $USER
```

## Git

```sh
git config credential.helper store
```
