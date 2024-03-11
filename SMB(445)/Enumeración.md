## Enumeración 

```zsh
smbclient -L <ip> -N 
```
```zsh
nxc smb <ip>
```
```zsh
smbmap -H <ip>
smbmap -H <ip> -r <recurso> # Listar de manera recursiva
smbmap -H <ip> --download <recurso> # Descargar recurso
```
