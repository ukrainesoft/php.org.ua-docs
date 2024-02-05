---
navigation:
  - function.stream-context-set-params.md: « stream\_context\_set\_params
  - function.stream-filter-append.md: stream\_filter\_append »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_copy\_to\_stream
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_copy\_to\_stream

(PHP 5, PHP 7, PHP 8)

stream\_copy\_to\_stream — Копіює дані з одного потоку до іншого

### Опис

```methodsynopsis
stream_copy_to_stream(    resource $from,    resource $to,    ?int $length = null,    int $offset = 0): int|false
```

Робить копію до `length` байт даних від поточної позиції (або від позиції `offset`, якщо вказано) потоку `from` у потік `to`. Якщо `length`равен\*\*`null`\*\*, буде скопійовано весь вміст, що залишився з `from`

### Список параметрів

`from`

Вихідний потік.

`to`

Потік призначення.

`length`

Максимальна кількість байт для копіювання. За замовчуванням копіюються всі байти.

`offset`

Зміщення, з якого копіюватимуться дані.

### Значення, що повертаються

Повертає загальну кількість скопійованих байт або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Параметр`length` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** stream\_copy\_to\_stream()\*\*\*\*

```php
<?php
$src = fopen('http://www.example.com', 'r');
$dest1 = fopen('first1k.txt', 'w');
$dest2 = fopen('remainder.txt', 'w');

echo stream_copy_to_stream($src, $dest1, 1024) . " байт скопировано в first1k.txt\n";
echo stream_copy_to_stream($src, $dest2) . " байт скопировано в remainder.txt\n";

?>
```

### Дивіться також

-   [copy()](function.copy.md) \- Копіює файл
