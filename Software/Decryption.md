Cuando tenemos permisos de administrador y acceso a la consola de scripts, podemos obtener credenciales cifradas alojadas en el servidor mediante el inspector de código del navegador y el mismo Script Console no lo va a descifrar y nos va a dar el resultado en texto claro.
Para ello primero nos vamos a credenciales y elegimos uno cualquiera. En este caso se tratará de una clave privada de SSH.
Tenemos que intentar hacer un update de la credencial y vamos a ver el valor por el inspector del navegador:

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/42e2b7f9-0eab-48b5-9f5a-781f079330c0)

Nos copiamos el valor y nos vamos a la consola para usar las siguientes funciones:

`println hudson.util.Secret.decrypt("{value}")`

El resultado sería la clave en texto claro:

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/1a82713c-d942-4026-b55c-1ce07fc0abe8)
