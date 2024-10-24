# Get serial number of device

```ps1
cls
#Get S/N Tag 
$serial = (Get-CimInstance Win32_BIOS).SerialNumber
$name = "$serial"

#Join de domain with de previus SN TAG as Hostname
Add-Computer -DomainName "yourdomain.local" -NewName $name -Credential domain\user.name -Restart
```
