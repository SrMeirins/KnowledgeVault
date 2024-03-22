## Gobuster

```zsh
gobuster -u http://10.10.10.103/ -w /usr/share/wordlists/dirbuster/directory-list-2.3-small.txt -x asp,aspx,txt,html
```

`-u` : URL 
`-w` : Diccionario
`-x` : Extensiones a Fuzzear
