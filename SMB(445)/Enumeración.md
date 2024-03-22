## Enumeración 

```zsh
smbclient -L <ip> -N # Listar haciendo uso de una NULL Session.
smbclient "//10.10.10.103/Department Shares" -N # Con una NULL Session acceder a la carpeta escogida.
```
```zsh
nxc smb <ip>
nxc smb <ip> -u 'user' -p 'password' # Verificar si credenciales son correctas
nxc smb <ip> -u 'user' -p 'password' --shares # Ver shares disponibles para el usuario y permisos
```
```zsh
smbmap -H <ip>
smbmap -H <ip> -u 'guest' # Acceder como usuario invitado cuando no nos lista nada
smbmap -H <ip> -r <recurso> # Listar de manera recursiva
smbmap -H <ip> --download <recurso> # Descargar recurso
```
