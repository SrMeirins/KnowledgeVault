Si en BloodHound, tenemos un usuario con los permisos GetChanges y GetChangesAll sobre el dominio, podemos efectuar un DCSync attack.

El ataque DCSync simula el comportamiento de un Controlador de Dominio y solicita a otros Controladores de Dominio que repliquen información utilizando el Protocolo Remoto de Replicación de Directorio (MS-DRSR). Debido a que MS-DRSR es una función válida y necesaria de Active Directory, no se puede apagar ni desactivar.

Por defecto, solo los grupos de Domain Admins, Enterprise Admins, Administradores y Controladores de Dominio tienen los privilegios requeridos.

Si alguna contraseña de cuenta está almacenada con cifrado reversible, Mimikatz ofrece una opción para devolver la contraseña en texto claro.

## Mimikatz
`lsadump::dcsync /domain:testlab.local /user:Administrator`

## SecretsDump Impacket

`impacket-secretsdump htb.local/mrlky:Football#7@10.10.10.103`
