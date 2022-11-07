# Install Company Portal

## Commandline: Installing the msi from github url:

```Powershell

# Download Company Portal and run msi with msiexec silently
#  --------------------------------------------------------------------------------------------------------
$url = 'https://github.com/brathen/pub/raw/main/CompanyPortal/Microsoft.CompanyPortal.11.1.523.0.x86.msi'
$Filename = $url.Split('/')[-1]
Invoke-WebRequest -UseBasicParsing -Uri $URL -OutFile "$env:TEMP\$Filename" -ErrorAction SilentlyContinue
Start-Process -FilePath 'msiexec' -ArgumentList "/i `"$env:TEMP\$Filename`" /qb!" -Wait
#  --------------------------------------------------------------------------------------------------------

```

## Commandline: Uninstall

```Powershell

# Download Company Portal and run msi with msiexec silently
#  --------------------------------------------------------------------------------------------------------
Start-Process -FilePath 'msiexec' -ArgumentList "/x `"Microsoft.CompanyPortal.11.1.523.0.x86.msi`" /qb!" -Wait
#  --------------------------------------------------------------------------------------------------------

```