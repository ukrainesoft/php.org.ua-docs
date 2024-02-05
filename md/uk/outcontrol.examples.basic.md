---
navigation:
  - outcontrol.examples.md: « Приклади
  - outcontrol.examples.rewrite.md: Перезапис виводу »
  - index.md: PHP Manual
  - outcontrol.examples.md: Приклади
title: Основи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Основи

**Приклад #1 Приклад контролю виведення**

```php
<?php

ob_start();
echo "Привет\n";

setcookie("cookiename", "cookiedata");

ob_end_flush();

?>
```

У наведеному прикладі висновок мовної конструкції [echo](function.echo.md) буде зберігатись у буфері виводу до виклику функції [ob\_end\_flush()](function.ob-end-flush.md). Тим часом виклик функції [setcookie()](function.setcookie.md) успішно збережеться в cookie браузера, не викликаючи помилки (заголовки не вийде відправити в браузер, коли дані вже відправлені).
