Базове використання

-   [« Примеры](outcontrol.examples.html)
    
-   [Использование перезаписи вывода »](outcontrol.examples.rewrite.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](outcontrol.examples.html)
    
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

У наведеному вище прикладі висновок з [echo](function.echo.html) буде зберігатись у буфері виводу до виклику [ob\_end\_flush()](function.ob-end-flush.html). Водночас виклик [setcookie()](function.setcookie.html) успішно збережеться в cookie браузера, не викликаючи помилки (заголовки не можуть бути відправлені до браузера після того, як дані вже були надіслані).