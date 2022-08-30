callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart

-   [« obgetstatus](function.ob-get-status.html)
    
-   [проimplicitflush »](function.ob-implicit-flush.html)
    
-   [PHP Manual](index.html)
    
-   [Функції контролю виведення](ref.outcontrol.html)
    
-   callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart
    

# проgzhandler

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

проgzhandler - callback-функція, що використовується для gzip-стиснення буфера виводу при виклику obstart

### Опис

```methodsynopsis
ob_gzhandler(string $data, int $flags): string|false
```

Функція **проgzhandler()** призначена для використання як callback-функції для [проstart()](function.ob-start.html), щоб полегшити надсилання gz-кодованих даних браузерам, які підтримують стиснення веб-сторінок. Перш ніж **проgzhandler()** відправить стислі дані, вона визначає, який тип кодування вмісту зможе прийняти браузер ("gzip", "deflate" або взагалі ніякий) і поверне його вміст відповідним чином. Підтримуються всі браузери, які надсилають коректні заголовки про те, що вони беруть стислі веб-сторінки. Якщо браузер не підтримує стиснення сторінок, ця функція поверне **`false`**

### Список параметрів

`data`

`flags`

### Значення, що повертаються

### Приклади

**Приклад #1 Приклад використання функції **проgzhandler()****

```php
<?php

ob_start("ob_gzhandler");

?>
<html>
<body>
<p>Это должно быть сжатой страницей.</p>
</body>
</html>
```

### Примітки

> **Зауваження**
> 
> **проgzhandler()** вимагає наявність модуля [zlib](ref.zlib.html)

> **Зауваження**
> 
> Ви не можете використовувати одночасно **проgzhandler()** і [zlib.outputcompression](zlib.configuration.html#ini.zlib.output-compression). Також зверніть увагу, що використання [zlib.outputcompression](zlib.configuration.html#ini.zlib.output-compression) краще, ніж **проgzhandler()**

### Дивіться також

-   [проstart()](function.ob-start.html) - Включення буферизації виводу
-   [проendflush()](function.ob-end-flush.html) - Скинути (відправити) буфер виведення та вимкнути буферизацію виводу