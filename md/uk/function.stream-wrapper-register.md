Реєструє обгортку URL, реалізовану у вигляді PHP-класу

-   [« streamsupportslock](function.stream-supports-lock.html)
    
-   [streamwrapperrestore »](function.stream-wrapper-restore.html)
    
-   [PHP Manual](index.md)
    
-   [Функції для роботи з потоками](ref.stream.md)
    
-   Реєструє обгортку URL, реалізовану у вигляді PHP-класу
    

# streamwrapperregister

(PHP 4> = 4.3.2, PHP 5, PHP 7, PHP 8)

streamwrapperregister - Реєструє обгортку URL, реалізовану у вигляді PHP-класу

### Опис

```methodsynopsis
stream_wrapper_register(string $protocol, string $class, int $flags = 0): bool
```

Дозволяє вам реалізувати власні обробники протоколів і потоків для використання з усіма іншими функціями файлової системи (такими як [fopen()](function.fopen.md) [fread()](function.fread.md) і т.д.).

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

-   Клас-прототип [streamWrapper](class.streamwrapper.md)
-   [Приклад класу, зареєстрованого як обгортка потоку](stream.streamwrapper.example-1.html)
-   [streamwrapperunregister()](function.stream-wrapper-unregister.html) - Скасує реєстрацію обгортки URL
-   [streamwrapperrestore()](function.stream-wrapper-restore.html) - Відновлює скасовану раніше вбудовану обгортку
-   [streamgetwrappers()](function.stream-get-wrappers.html) - Отримати список зареєстрованих потоків