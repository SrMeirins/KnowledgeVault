**ADMIN** ES NECESARIO! -> Necesitamos privilegios para cambiar configuración del Drupal.

Lo primero es irnos una vez que tenemos acceso al panel de administración de Drupal a "_Modules_" y ahí marcamos la casilla de PHP FILTER

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/3572a764-907d-40d8-82bc-d47cba0874c2)

A continuación, nos dirigimos a crear un nuevo articulo (Content--> Add Content --> Article) y en php nos entablamos una reverse shell hacia nuestro servidor local. Para testear, vamos a correr un comando y vemos el output por pantalla al previsualizar el articulo.

**Es importante verificar que hemos habilitado la entrada de código PHP**:

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/1afd7bee-f75b-45b7-98c2-ecc24fe8e61e)

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/358e8219-ee32-4b83-ba5f-25bf92ada1bf)

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/45dc3fcf-4334-415c-a788-da72fd0efb04)

