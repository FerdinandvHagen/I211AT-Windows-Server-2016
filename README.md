# I211AT-Windows-Server-2016
Install Drivers for I211AT on Windows Server 2016


Follow https://blog.citrix24.com/install-windows-server-2016-core-intel-nuc/


Short:
```
bcdedit /set LOADOPTIONS DISABLE_INTEGRITY_CHECKS
bcdedit /set TESTSIGNING ON
bcdedit /set NOINTEGRITYCHECKS ON

# put all files on USB stick or something like that in a folder
pnputil -i -a D:\driver\*.inf

# accept prompt

# revert
bcdedit /set LOADOPTIONS ENABLE_INTEGRITY_CHECKS
bcdedit /set TESTSIGNING OFF
bcdedit /set NOINTEGRITYCHECKS OFF
```
