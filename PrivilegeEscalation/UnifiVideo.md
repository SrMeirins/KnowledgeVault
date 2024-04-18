Basicamente, si una versión vulnerable de este servicio está corriendo en la máquina víctima, podemos cargar un archivo .exe malicioso con el nombre de taskkill.exe dentro de la carpeta del servicio, y al parar o iniciar el servicio se va a ejecutar.
Para ello necesitamos un usuario no privilegiado en la máquina y transferirnos el exe malicioso. Este exe malicioso podemos crearlo con msfvenom y ofuscarlo con ebowla para evitar el defender.

Mas información en el exploit: [Link](https://www.exploit-db.com/exploits/43390)
