# Install Company Portal

## Commandline: Installing the msi from github url:

```Powershell

# Download Company Portal and run msi with msiexec silently
#  --------------------------------------------------------------------------------------------------------
$url = 'https://github.com/brathen/pub/raw/main/CompanyPortal/latest/Microsoft.CompanyPortal'
$Filename = $url.Split('/')[-1]
Invoke-WebRequest -UseBasicParsing -Uri $URL -OutFile "$env:TEMP\$Filename" -ErrorAction SilentlyContinue
Start-Process -FilePath 'msiexec' -ArgumentList "/i `"$env:TEMP\$Filename`" /qb!-" -Wait
#  --------------------------------------------------------------------------------------------------------

```

## Commandline: Uninstall

```Powershell

# Download Company Portal and run msi with msiexec silently
#  --------------------------------------------------------------------------------------------------------
Start-Process -FilePath 'msiexec' -ArgumentList "/x `"{E9986D93-2AFB-4323-8B43-77FB3DB99AF8}`" /qb!-" -Wait
#  --------------------------------------------------------------------------------------------------------

```