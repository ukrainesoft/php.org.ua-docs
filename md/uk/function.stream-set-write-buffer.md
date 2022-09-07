---
navigation:
  - function.stream-set-timeout.md: « streamsettimeout
  - function.stream-socket-accept.md: streamsocketaccept »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: streamsetwritebuffer
---
# streamsetwritebuffer

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

streamsetwritebuffer — Встановлює буферизацію файлу під час запису у вказаний потік

### Опис

```methodsynopsis
stream_set_write_buffer(resource $stream, int $size): int
```

Встановлює буферизацію операцій запису на заданому потоці `stream` до числа `size` байт.

### Список параметрів

`stream`

Файловий покажчик.

`size`

Число байт для буферизації. Якщо аргумент `size` дорівнює 0, то операції запису не буферизуються. Це гарантує, що всі операції запису з використанням функції [fwrite()](function.fwrite.md) будуть завершені перед тим, як іншим процесам буде дозволено записувати потік виведення.

### Значення, що повертаються

Повертає 0 у разі успішного виконання, або інше значення, якщо запит не може бути виконаний.

### Приклади

**Приклад #1 Приклад використання **streamsetwritebuffer()****

Наступний приклад демонструє використання функції **streamsetwritebuffer()** для створення потоку, що не буферизується.

```php
<?php
$fp = fopen($file, "w");
if ($fp) {
   if (stream_set_write_buffer($fp, 0) !== 0) {
      // не удалось внести изменение
  }
  fwrite($fp, $output);
  fclose($fp);
}
?>
```

### Дивіться також

-   [fopen()](function.fopen.md) - Відкриває файл або URL
-   [fwrite()](function.fwrite.md) - Бінарно-безпечний запис у файл
