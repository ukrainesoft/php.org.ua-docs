Реєструє обгортку URL, реалізовану у вигляді PHP-класу

-   [« stream\_supports\_lock](function.stream-supports-lock.html)
    
-   [stream\_wrapper\_restore »](function.stream-wrapper-restore.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Реєструє обгортку URL, реалізовану у вигляді PHP-класу
    

# streamwrapperregister

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamwrapperregister - Реєструє обгортку URL, реалізовану у вигляді PHP-класу

### Опис

```methodsynopsis
stream_wrapper_register(string $protocol, string $class, int $flags = 0): bool
```

Дозволяє вам реалізувати власні обробники протоколів і потоків для використання з усіма іншими функціями файлової системи (такими як [fopen()](function.fopen.html) [fread()](function.fread.html) і т.д.).

### Список параметрів

`protocol`

Назва обгортки, що реєструється. Допустимі імена протоколів повинні містити лише літери, цифри, точки (.), плюси (+) або дефіси (-).

`class`

Назва класу, що реалізує протокол `protocol`

`flags`

Повинно бути встановлене в **`STREAM_IS_URL`**, якщо параметр `protocol` є протоколом URL. Типово 0, локальний потік.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

**streamwrapperregister()** повертатиме **`false`**, якщо протокол `protocol` вже має оброблювач.

### Приклади

**Приклад #1 Як зареєструвати обгортку потоку**

```php
<?php
$existed = in_array("var", stream_get_wrappers());
if ($existed) {
    stream_wrapper_unregister("var");
}
stream_wrapper_register("var", "VariableStream");
$myvar = "";

$fp = fopen("var://myvar", "r+");

fwrite($fp, "line1\n");
fwrite($fp, "line2\n");
fwrite($fp, "line3\n");

rewind($fp);
while (!feof($fp)) {
    echo fgets($fp);
}
fclose($fp);
var_dump($myvar);

if ($existed) {
    stream_wrapper_restore("var");
}

?>
```

Результат виконання цього прикладу:

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

-   Клас-прототип [streamWrapper](class.streamwrapper.html)
-   [Пример класса, зарегистрированного в качестве обёртки потока](stream.streamwrapper.example-1.html)
-   [stream\_wrapper\_unregister()](function.stream-wrapper-unregister.html) - Скасує реєстрацію обгортки URL
-   [stream\_wrapper\_restore()](function.stream-wrapper-restore.html) - Відновлює скасовану раніше вбудовану обгортку
-   [stream\_get\_wrappers()](function.stream-get-wrappers.html) - Отримати список зареєстрованих потоків