---
navigation:
  - function.stream-supports-lock.md: « stream\_supports\_lock
  - function.stream-wrapper-restore.md: stream\_wrapper\_restore »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_wrapper\_register
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_wrapper\_register

(PHP 4 >= 4.3.2, PHP 5, PHP 7, PHP 8)

stream\_wrapper\_register - Реєструє обгортку URL, реалізовану у вигляді PHP-класу

### Опис

```methodsynopsis
stream_wrapper_register(string $protocol, string $class, int $flags = 0): bool
```

Дозволяє вам реалізувати власні обробники протоколів і потоків для використання з усіма іншими функціями файлової системи (такими як [fopen()](function.fopen.md) [fread()](function.fread.md)и т.д.).

### Список параметрів

`protocol`

Назва обгортки, що реєструється. Допустимі імена протоколів повинні містити лише літери, цифри, точки (.), плюси (+) або дефіси (-).

`class`

Назва класу, що реалізує протокол `protocol`

`flags`

Повинно бути встановлене в **`STREAM_IS_URL`**, якщо параметр `protocol` є протоколом URL. Типово 0, локальний потік.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

**stream\_wrapper\_register()** повертатиме **`false`**, якщо протокол `protocol`уже имеет обработчик.

### Приклади

**Приклад #1 Як зареєструвати обгортку потоку**

```php
<?php
$existed = in_array("var", stream_get_wrappers());
if ($existed) {
    stream_wrapper_unregister("var");
}
stream_wrapper_register("var", "VariableStream");
$myvar = "";

$fp = fopen("var://myvar", "r+");

fwrite($fp, "line1\n");
fwrite($fp, "line2\n");
fwrite($fp, "line3\n");

rewind($fp);
while (!feof($fp)) {
    echo fgets($fp);
}
fclose($fp);
var_dump($myvar);

if ($existed) {
    stream_wrapper_restore("var");
}

?>
```

Результат виконання наведеного прикладу:

```
line1
line2
line3
string(18) "line1
line2
line3
"
```

### Дивіться також

-   Клас-прототип[streamWrapper](class.streamwrapper.md)
-   [Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.md)
-   [stream\_wrapper\_unregister()](function.stream-wrapper-unregister.md) \- Скасує реєстрацію обгортки URL
-   [stream\_wrapper\_restore()](function.stream-wrapper-restore.md) \- Відновлює скасовану раніше вбудовану обгортку
-   [stream\_get\_wrappers()](function.stream-get-wrappers.md) \- Отримати список зареєстрованих потоків
