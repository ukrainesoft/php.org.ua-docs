---
navigation:
  - function.inflate-init.md: « inflate\_init
  - function.readgzfile.md: readgzfile »
  - index.md: PHP Manual
  - ref.zlib.md: Функції Zlib
title: ob\_gzhandler
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ob\_gzhandler

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

ob\_gzhandler — стискає буфер виводу в gzip, діючи як callback-функція — параметр функції ob\_start

### Опис

```methodsynopsis
ob_gzhandler(string $data, int $flags): string|false
```

Функция**ob\_gzhandler()** виступає в ролі callback-функції – параметра функції [ob\_start()](function.ob-start.md), щоб спростити надсилання gz-кодованих даних для веб-браузерів, які підтримують обробку стислих веб-сторінок. Перед тим як функція **ob\_gzhandler()** відправить стислі дані, визначить прийнятий браузером тип кодування вмісту (gzip, deflate або взагалі ніякий), і поверне свій висновок. Підтримуються всі браузери, оскільки браузер сам надсилає правильний заголовок, який повідомляє, що він приймає стислі веб-сторінки. Якщо браузер не підтримує стиснення сторінок, ця функція поверне **`false`**

### Список параметрів

`data`

`flags`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад использования функции**ob\_gzhandler()\*\*\*\*

```php
<?php

ob_start("ob_gzhandler");

?>
<html>
<body>
<p>Это должно быть сжатой страницей.</p>
</body>
</html>
```

### Примітки

> **Зауваження** :
> 
> Функції \*\*ob\_gzhandler()\*\*нужен модуль[zlib](ref.zlib.md)

> **Зауваження** :
> 
> Не можна одночасно викликати функцію **ob\_gzhandler()** та включати налаштування [zlib.output\_compression](zlib.configuration.md#ini.zlib.output-compression)Обратите также внимание, включение опции[zlib.output\_compression](zlib.configuration.md#ini.zlib.output-compression) пріоритетніший за виклик функції **ob\_gzhandler()**

### Дивіться також

-   [ob\_start()](function.ob-start.md) \- Включає буферизацію виводу
-   [ob\_end\_flush()](function.ob-end-flush.md) \- Скидає (відправляє) значення активного оброблювача виводу, що повертається, і відключає активний буфер виводу
