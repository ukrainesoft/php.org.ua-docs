---
navigation:
  - function.stream-filter-remove.md: « stream\_filter\_remove
  - function.stream-get-filters.md: stream\_get\_filters »
  - index.md: PHP Manual
  - ref.stream.md: Функції для роботи з потоками
title: stream\_get\_contents
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# stream\_get\_contents

(PHP 5, PHP 7, PHP 8)

stream\_get\_contents — Читає частину потоку, що залишилася, в рядок

### Опис

```methodsynopsis
stream_get_contents(resource $stream, ?int $length = null, int $offset = -1): string|false
```

Похожа на функцию[file\_get\_contents()](function.file-get-contents.md), за винятком того, що **stream\_get\_contents()** працює з уже відкритим ресурсом потоку і повертає решту вмісту в рядок розміром до `length` байт і починаючи із зазначеного зміщення `offset`

### Список параметрів

`stream`(resource)

Ресурс потоку (наприклад, отриманий за допомогою функції [fopen()](function.fopen.md)) .

`length`(int)

Максимальна кількість байт для читання. За замовчуванням **`null`** (прочитати весь буфер, що залишився).

`offset`(int)

Перейти до зазначеного усунення перед читанням. Якщо це число негативне, перехід не відбудеться і читання почнеться з поточної позиції.

### Значення, що повертаються

Повертає рядок або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `length` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** stream\_get\_contents()\*\*\*\*

```php
<?php

if ($stream = fopen('http://www.example.com', 'r')) {
    // вывести всю страницу начиная со смещения 10
    echo stream_get_contents($stream, -1, 10);

    fclose($stream);
}


if ($stream = fopen('http://www.example.net', 'r')) {
    // вывести первые 5 байт
    echo stream_get_contents($stream, 5);

    fclose($stream);
}

?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

> **Зауваження** :
> 
> При указании значения параметра`length`, відмінного від \*\*`null`\*\*ця функція негайно виділить внутрішній буфер такого розміру, навіть якщо фактичний вміст буде значно коротшим.

### Дивіться також

-   [fgets()](function.fgets.md) \- Читає рядок із файлу
-   [fread()](function.fread.md) \- Бінарно-безпечне читання файлу
-   [fpassthru()](function.fpassthru.md) \- Виводить всі дані з файлового покажчика, що залишилися.
