En el caso de que tengamos un archivo cifrado con OpenSSL (_openssl enc'd data with salted password, base64 encoded_), existe una herramienta en Python que sin saber la password ni el algoritmo de cifrado nos permite hacer un ataque de fuerza bruta y detectarlo.
La herramienta es la siguiente [Link](https://github.com/HrushikeshK/openssl-bruteforce) y se corre de la siguiente manera.

```zsh
python2 brute.py /usr/share/wordlists/rockyou.txt ciphers.txt ../../nmap/drupal.txt.enc 2>/dev/null
```

Si esperamos vemos que además de hacer un decrypt, nos muestra el output del archivo:

![image](https://github.com/SrMeirins/KnowledgeVault/assets/95763783/5b9ae380-d854-4909-8fc4-1e950763884f)
