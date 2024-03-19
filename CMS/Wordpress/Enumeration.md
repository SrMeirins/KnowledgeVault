## Plugin Fuzzing Wordpress with WFUZZ
```zsh
wfuzz -c --hc=404 -w /usr/share/seclists/Discovery/Web-Content/CMS/wp-plugins.fuzz.txt -u http://tenten.htb/FUZZ -t 200
```
