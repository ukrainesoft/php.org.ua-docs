Встановити розмір фрагмента даних потоку

-   [« stream\_set\_blocking](function.stream-set-blocking.html)
    
-   [stream\_set\_read\_buffer »](function.stream-set-read-buffer.html)
    
-   [PHP Manual](index.html)
    
-   [Функции для работы с потоками](ref.stream.html)
    
-   Встановити розмір фрагмента даних потоку
    

# streamsetchunksize

(PHP 5> = 5.4.0, PHP 7, PHP 8)

streamsetchunksize — Встановити розмір фрагмента даних потоку

### Опис

```methodsynopsis
stream_set_chunk_size(resource $stream, int $size): int
```

Встановити розмір фрагмента даних потоку.

### Список параметрів

`stream`

Потік.

`size`

Бажаний розмір фрагмента.

### Значення, що повертаються

Повертає попередній розмір фрагмента у разі успішного виконання.

Поверне **`false`**, якщо `size` менше 1 або більше **`PHP_INT_MAX`**

### Помилки

Викликає помилку рівня **`E_WARNING`**, якщо `size` менше 1 або більше **`PHP_INT_MAX`**