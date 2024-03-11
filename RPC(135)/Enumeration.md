```zsh
rpcclient -U "user%password" <ip> # Conexión con usuario y contraseña
rpcclient -U "" <ip> -N # Conexión usando una NULL Session

rpcclient -U "user%password" <ip> -c 'enumdomusers' # Enumeración de usuarios del dominio
rpcclient -U "user%password" <ip> -c 'enumdomgroups' # Enumeración de grupos del dominio
rpcclient -U "user%password" <ip> -c 'querygroupmem rid' # Enumeración de usuarios que forman parte de un grupo
rpcclient -U "user%password" <ip> -c 'queryuser rid' # Enumeración de information del usuario
rpcclient -U "user%password" <ip> -c 'querydispinfo' # Enumeración de descripciones de usuario del dominio
```
