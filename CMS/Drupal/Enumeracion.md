##### DB Password and Credentials**
Si tenemos acceso a los archivos de configuración de Drupal, normalmente las credenciales de BBDD están alojadas en la ruta: `sitename/sites/default/settings.php`

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/c30354a1-acf4-4219-8ff1-c70c0ec1c929)

Podemos filtrar desde la carpeta de Drupal por la palabra password: 
```zsh
grep -r "password" | less -S
```
