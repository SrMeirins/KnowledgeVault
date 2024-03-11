En ocasiones, si tenemos acceso a SYSVOL podemos obtener contraseñas cifradas las cuales podemos obtener el texto claro ya que Microsoft publicó la clave privada en su día.
Se encuentran un archivo llamado groups.xml, dentro del directorio 'Preferences' en las Group Policies

Ej: `replication/active.htb/Policies/{31B2F340-016D-11D2-945F-00C04FB984F9}/MACHINE/Preferences/Groups/groups.xml`

Podemos obtener la contraseña mediante la herramienta `gpp-decrypt`
