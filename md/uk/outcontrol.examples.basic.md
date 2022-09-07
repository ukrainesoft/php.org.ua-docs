---
navigation:
  - outcontrol.examples.md: « Приклади
  - outcontrol.examples.rewrite.md: Використання перезапису виводу »
  - index.md: PHP Manual
  - outcontrol.examples.md: Приклади
title: Базове використання
---
## Базове використання

**Приклад #1 Приклад контролю виведення**

```php
<?php

ob_start();
echo "Привет\n";

setcookie("cookiename", "cookiedata");

ob_end_flush();

?>
```

У наведеному вище прикладі висновок з [echo](function.echo.md) буде зберігатись у буфері виводу до виклику [проendflush()](function.ob-end-flush.md). Водночас виклик [setcookie()](function.setcookie.md) успішно збережеться в cookie браузера, не викликаючи помилки (заголовки не можуть бути відправлені до браузера після того, як дані вже були надіслані).
