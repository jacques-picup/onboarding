## Executing powershell scripts

By Default Windows 11 blocks execution of powershell scripts.
You need to do the following to get this working correctly:

`Set-ExecutionPolicy -ExecutionPolicy Unrestricted -Scope CurrentUser`