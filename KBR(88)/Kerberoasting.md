El Kerberoasting es un ataque contra Kerberos que trata, a partir de un usuario sin privilegios, de obtener las contraseñas vinculadas a una cuenta de servicio del Directorio Activo.

Cuando un usuario desea autenticarse ante un servicio, el KDC le devuelve un ticket TGS el cual contiene datos cifrados con una clave derivada de la contraseña de la cuenta del servicio.
Por lo tanto, es posible intentar crackear estos tickets para descubrir la contraseña de la cuenta de servicio. 
Este ataque puede resultar exitoso cuando el servicio está configurado con una cuenta de usuario normal (a diferencia de una cuenta gestionada o de máquina) ya que la complejidad y rotación de la contraseña recae exclusivamente sobre la persona.

Además, no es extraño que estas cuentas de servicio presenten privilegios elevados, por lo que es una técnica que puede dar muy buenos resultados como posible vía de elevación de privilegios. 
Sin embargo, en la actualidad cada vez existe mayor concienciación y por lo tanto es más común encontrar mitigaciones para eliminar el riesgo de este posible vector, así como formas de detección como puede ser el uso de cuentas señuelo.

## impacket-GetUserSPNs

`impacket-GetUserSPNs domain/user:password -request`

Una vez tenemos un TGS, podemos guardarlo en un archivo e intentar crackear la contraseña con John.
