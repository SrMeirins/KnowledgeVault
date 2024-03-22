Para montarnos un directorio compartido, vamos primero a crearnos un directorio en `/mnt/mount`

A continuación vamos a hacer uso del comando _mount_ para hacernos una montura de tipo CIFS de todo el recurso en el directorio que acabamos de crear.

`mount -t cifs "//10.10.10.103/Department Shares" /mnt/montura`

_*Si nos pide contraseá unicamente le damos a Enter en caso de ser una NULL Session_
_Es también importante tener el paquete cifs-utils instalado, si no nos dará error_

Para desmontarlo, usamos el comando _umount_:

`umount /mnt/montura/`
