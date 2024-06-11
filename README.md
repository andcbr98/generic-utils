echo $env:USERPROFILE

schtasks /create /sc minute /mo 5 /tn "RunPowerShellScript" /tr "powershell.exe -File %USERPROFILE%\scripts\your_script.ps1" /f

netstat -ano | wsl grep "80"

find . -name "file.txt" -exec grep -H "string" {} \;

sudo scutil --set ComputerName "system"
sudo scutil --set HostName "system"
sudo scutil --set LocalHostName "system"

terraform apply -refresh-only
terraform force-unlock 1db462f1-b2be-c5f4-2238-8604f079hdcg   
openssl s_client -connect server_hostname:port -tls1_2
az ad sp create-for-rbac --name terraform --role Contributor --scopes /subscriptions/<subscription_id>  
