---
navigation:
  - function.stream-set-timeout.md: « stream\_set\_timeout
  - function.stream-socket-accept.md: stream\_socket\_accept »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_set\_write\_buffer
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_set\_write\_buffer

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

stream\_set\_write\_buffer — Встановлює буферизацію файлу під час запису у вказаний потік

### Опис

```methodsynopsis
stream_set_write_buffer(resource $stream, int $size): int
```

Устанавливает буферизацию для операций записи на заданном потоке`stream` до числа `size`байт.

### Список параметрів

`stream`

Файловий покажчик.

`size`

Число байт для буферизации. Если аргумент`size` дорівнює 0, то операції запису не буферизуються. Це гарантує, що всі операції запису з використанням функції [fwrite()](function.fwrite.md) будуть завершені перед тим, як іншим процесам буде дозволено записувати потік виведення.

### Значення, що повертаються

Повертає 0 у разі успішного виконання, або інше значення, якщо запит не може бути виконаний.

### Приклади

**Пример #1 Пример использования**stream\_set\_write\_buffer()\*\*\*\*

Следующий пример демонстрирует использование функции**stream\_set\_write\_buffer()** для створення потоку, що не буферизується.

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

-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [fwrite()](function.fwrite.md) \- Бінарно-безпечний запис у файл
