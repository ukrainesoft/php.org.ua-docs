Читає частину потоку, що залишилася, в рядок

-   [« stream\_filter\_remove](function.stream-filter-remove.html)
    
-   [stream\_get\_filters »](function.stream-get-filters.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Читає частину потоку, що залишилася, в рядок
    

# streamgetcontents

(PHP 5, PHP 7, PHP 8)

streamgetcontents — Читає частину потоку, що залишилася, в рядок

### Опис

```methodsynopsis
stream_get_contents(resource $stream, ?int $length = null, int $offset = -1): string|false
```

Схожа на функцію [file\_get\_contents()](function.file-get-contents.html), за винятком того, що **streamgetcontents()** працює з уже відкритим ресурсом потоку і повертає решту вмісту в рядок розміром до `length` байт і починаючи із зазначеного зміщення `offset`

### Список параметрів

`stream` (Resource)

Ресурс потоку (наприклад, отриманий за допомогою функції [fopen()](function.fopen.html)

`length` (int)

Максимальна кількість байт для читання. За замовчуванням **`null`** (прочитати весь буфер, що залишився).

`offset` (int)

Перейти до зазначеного усунення перед читанням. Якщо це число негативне, перехід не відбудеться і читання почнеться з поточної позиції.

### Значення, що повертаються

Повертає рядок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `length` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **streamgetcontents()****

```php
<?php

if ($stream = fopen('http://www.example.com', 'r')) {
    // вывести всю страницу начиная со смещения 10
    echo stream_get_contents($stream, -1, 10);

    fclose($stream);
}


if ($stream = fopen('http://www.example.net', 'r')) {
    // вывести первые 5 байт
    echo stream_get_contents($stream, 5);

    fclose($stream);
}

?>
```

### Примітки

> **Зауваження**: Ця функція безпечна для обробки даних у двійковій формі.

### Дивіться також

-   [fgets()](function.fgets.html) - Читає рядок із файлу
-   [fread()](function.fread.html) - Бінарно-безпечне читання файлу
-   [fpassthru()](function.fpassthru.html) - Виводить всі дані з файлового покажчика, що залишилися.