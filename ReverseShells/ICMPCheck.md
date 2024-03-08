Como método de comprobar si recibimos una conexión externa (paso anterior a entablarnos una reverse shell), nos vamos a poner a la escucha con la herramient `tcpdump` de trazas ICMP por la interfaz de red que estemos usando:
```zsh
tcpdump -i tun0 icmp -n 
```

`-i` : Interfaz
`-n` : No convierte direcciones a nombres (evitar resolucion DNS)
