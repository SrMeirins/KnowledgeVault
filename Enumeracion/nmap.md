## SYN Connect Scan for Linux

```zsh
nmap -p- --open -T5 -n -v -Pn {IP} -oN allPorts
```

## SYN Connect Scan for Windows
Hay ocasiones que demora, asi que podemos usar un SYN Connect Scan aportando un Min Rate.

```zsh
nmap -p- --open -sS --min-rate 5000 -n -vvv -Pn {IP} -oN allPorts
```

## UDP Scan
Tarda muchisimo, una barbaridad. Hay que limitar los puertos todo lo posible, ya sea de forma manual o top ports que elijamos.

```zsh
nmap --top-ports 100 --open -sU -v -T5 -n {IP} -oG allPortsUDP
```

## XML to HTML Output
Si tenemos muchos puertos y queremos reportarlos de manera mas limpia en forma de archivo HTML, tenemos que exportarlo a XML y luego transformarlo con la herramienta xsltproc.

```zsh
-oX targetedXML # En el comando de NMAP
xsltproc targetedXML > targetedHTML
php -S 0.0.0.0:80 # Para montarnos un servidor Web local
```
