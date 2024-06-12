## Windows

echo $env:USERPROFILE

schtasks /create /sc minute /mo 5 /tn "RunPowerShellScript" /tr "powershell.exe -File %USERPROFILE%\scripts\your_script.ps1" /f

netstat -ano | wsl grep "80"

## Linux

find . -name "file.txt" -exec grep -H "string" {} \;

## MacOS

sudo scutil --set ComputerName "system"
sudo scutil --set HostName "system"
sudo scutil --set LocalHostName "system"

## Terraform

terraform apply -refresh-only
terraform force-unlock 1db462f1-b2be-c5f4-2238-8604f079hdcg   

az ad sp create-for-rbac --name terraform --role Contributor --scopes /subscriptions/<subscription_id>  

## OpenSSL

openssl s_client -connect server_hostname:port -tls1_2

## K8S on Linux/WSL

curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube-linux-amd64
sudo install minikube-linux-amd64 /usr/local/bin/minikube && rm minikube-linux-amd64

curl https://raw.githubusercontent.com/helm/helm/main/scripts/get-helm-3 | bash

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"
sudo install -o root -g root -m 0755 kubectl /usr/local/bin/kubectl

curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh
sudo usermod -aG docker $USER
