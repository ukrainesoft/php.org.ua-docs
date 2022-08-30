Базове використання

-   [« Приклади](outcontrol.examples.md)
    
-   [Використання перезапису виводу »](outcontrol.examples.rewrite.md)
    
-   [PHP Manual](index.md)
    
-   [Приклади](outcontrol.examples.md)
    
-   Базове використання
    

## Базове використання

**Приклад #1 Приклад контролю виведення**

```php
<?php

ob_start();
echo "Привет\n";

setcookie("cookiename", "cookiedata");

ob_end_flush();

?>
```

У наведеному вище прикладі висновок з [echo](function.echo.md) буде зберігатись у буфері виводу до виклику [проendflush()](function.ob-end-flush.html). Водночас виклик [setcookie()](function.setcookie.md) успішно збережеться в cookie браузера, не викликаючи помилки (заголовки не можуть бути відправлені до браузера після того, як дані вже були надіслані).