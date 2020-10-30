# Powershell

**Ping scan:**

```powershell
1..1024 | % {echo ((New-Object Net.Sockets.TcpClient).Connect("<IP>", $_)) "Port
$_ is open!"} 2>$null
```
