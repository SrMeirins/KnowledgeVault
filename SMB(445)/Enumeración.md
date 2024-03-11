## Enumeración 

```zsh
smbclient -L <ip> -N 
```
```zsh
nxc smb <ip>
nxc smb <ip> -u 'user' -p 'password' # Verificar si credenciales son correctas
nxc smb <ip> -u 'user' -p 'password' --shares # Ver shares disponibles para el usuario y permisos
```
```zsh
smbmap -H <ip>
smbmap -H <ip> -r <recurso> # Listar de manera recursiva
smbmap -H <ip> --download <recurso> # Descargar recurso
```
