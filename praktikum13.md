Selles praktikumis tegelesime skriptimisega Windowsis. Pidin kirjutama skripti, mis teeb mitmeid asju arvutis, sealhulgas näiteks võrgu konfigureerimine ja muu info otsimine


# Skript testarvuti kohta info kogumiseks ja salvestamiseks

# Masina nimi, PowerShell versioon ja Windowsi versioon
$hostname = hostname
$psVersion = $PSVersionTable.PSVersion.ToString()
$windowsVersion = (Get-WmiObject -class Win32_OperatingSystem).Caption

# Võrgu konfiguratsioon
$networkConfig = Get-WmiObject -Class Win32_NetworkAdapterConfiguration -Filter "IPEnabled = TRUE"
$ipAddress = $networkConfig.IPAddress[0]
$subnetMask = $networkConfig.IPSubnet[0]
$defaultGateway = $networkConfig.DefaultIPGateway[0]
$dhcpEnabled = $networkConfig.DHCPEnabled
$macAddress = $networkConfig.MACAddress

# Protsessori ja RAM info
$system = Get-WmiObject -Class Win32_ComputerSystem
$cpu = (Get-WmiObject -Class Win32_Processor).Name
$ram = $system.TotalPhysicalMemory / 1GB

# Graafikakaardi info
$gpu = Get-WmiObject -Class Win32_VideoController
$gpuName = $gpu.Name
$driverVersion = $gpu.DriverVersion
$driverDate = $gpu.DriverDate
$screenResolution = "$($gpu.VideoModeDescription)"

# Kõvaketta info
$disk = Get-WmiObject -Class Win32_LogicalDisk -Filter "DeviceID = 'C:'"
$diskSize = $disk.Size / 1GB
$freeSpace = $disk.FreeSpace / 1GB

# PCI-siinil olevate seadmete draiverite info
$pciDevices = Get-WmiObject -Class Win32_PnPSignedDriver | Where-Object { $_.DeviceClass -eq "PCI" }

# Arvutis olevad kasutajad
$users = Get-WmiObject -Class Win32_UserAccount

# Käimasolevate protsesside arv
$processCount = (Get-Process).Count

# 10 viimasena käivitatud protsessi
$recentProcesses = Get-Process | Sort-Object StartTime -Descending | Select-Object -First 10 Name, Id, StartTime

# Arvuti kuupäev ja kellaaeg
$dateTime = Get-Date

# Info faili kirjutamine
$outputPath = "C:\SystemInfo.txt"
$output = @"
Masina nimi: $hostname
PowerShell versioon: $psVersion
Windowsi versioon: $windowsVersion

IP-aadress: $ipAddress
Võrgumask: $subnetMask
Gateway: $defaultGateway
DHCP lubatud: $dhcpEnabled
MAC-aadress: $macAddress

Protsessor: $cpu
RAM (GB): $ram

Graafikakaart: $gpuName
Draiveri versioon: $driverVersion
Draiveri kuupäev: $driverDate
Ekraani lahutus: $screenResolution

Kõvaketta suurus (GB): $diskSize
Vaba ruum (GB): $freeSpace

PCI seadmed:
$($pciDevices | Format-Table Description, Manufacturer, DriverVersion -AutoSize | Out-String)

Kasutajad:
$($users | Format-Table Name, Description, LocalAccount, Disabled -AutoSize | Out-String)

Käimasolevate protsesside arv: $processCount

10 viimasena käivitatud protsessi:
$($recentProcesses | Format-Table Name, Id, StartTime -AutoSize | Out-String)

Kuupäev ja kellaaeg: $dateTime
"@

$output | Out-File -FilePath $outputPath
Write-Host "Info salvestatud: $outputPath"
