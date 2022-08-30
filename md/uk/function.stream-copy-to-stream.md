Копіює дані з одного потоку до іншого

-   [« streamcontextsetparams](function.stream-context-set-params.html)
    
-   [streamfilterappend »](function.stream-filter-append.html)
    
-   [PHP Manual](index.html)
    
-   [Функції для роботи з потоками](ref.stream.html)
    
-   Копіює дані з одного потоку до іншого
    

# streamcopyтоstream

(PHP 5, PHP 7, PHP 8)

streamcopyтоstream — Копіює дані з одного потоку до іншого

### Опис

```methodsynopsis
stream_copy_to_stream(    resource $from,    resource $to,    ?int $length = null,    int $offset = 0): int|false
```

Робить копію до `length` байт даних від поточної позиції (або від позиції `offset`, якщо вказано) потоку `from` у потік `to`. Якщо `length` дорівнює **`null`**, буде скопійовано весь вміст, що залишився з `from`

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

Повертає загальну кількість скопійованих байт або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `length` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **streamcopyтоstream()****

```php
<?php
$src = fopen('http://www.example.com', 'r');
$dest1 = fopen('first1k.txt', 'w');
$dest2 = fopen('remainder.txt', 'w');

echo stream_copy_to_stream($src, $dest1, 1024) . " байт скопировано в first1k.txt\n";
echo stream_copy_to_stream($src, $dest2) . " байт скопировано в remainder.txt\n";

?>
```

### Дивіться також

-   [copy()](function.copy.html) - Копіює файл