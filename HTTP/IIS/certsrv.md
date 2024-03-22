En ocasiones, si tenemos acceso al Microsoft Active Directory Certificate Services y tenemos credenciales válidas para autenticarnos, podemos aprovecharnos para obtener un certificado y poder obtener por ejemplo una shell por WinRM en caso de que no nos fuese permitido antes.
Para ello, sabiendo que tenemos un diccionario especifico de IIS, veremos si tenemos acceso para autenticarnos en http://ip/certsrv.

Una vez tengamos acceso, nos vamos a dirigir a _Request a Certificate_ -> _Advanced Certificate Request_.
Vemos que tenemos que subir un certificate request. Para ello vamos a crearlo junto a la private key del certificado. Para ello:

```zsh
openssl req -newkey rsa:2048 -nodes -keyout amanda.key -out amanda.csr
```

Ahora tenemos dos archivos, una clave privada y un certificate request. Este último vamos a copiarlo y pegarlo en la web y nos va a dar un archivo .cer, que es el que vamos a usar junto a la clave privada para autenticarnos por WinRM.

Para ello usaremos la herramienta _Evil-WinRM_. Si intentamos autenticarnos mediante usuario y contraseña (sabiendo que están en el grupo de Remote Management Users) pero nos da error, vamos a usar el certificado y la clave privada para autenticarnos:

`evil-winrm -S -c certnew.cer -k amanda.key -i 10.10.10.103 -u 'amanda' -p 'Ashare1972'`

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/866e54d6-ba41-4d57-a891-06559853c349)

