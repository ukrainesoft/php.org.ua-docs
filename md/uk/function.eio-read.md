---
navigation:
  - function.eio-poll.md: « eio\_poll
  - function.eio-readahead.md: eio\_readahead »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_read

(PECL eio >= 0.0.1dev)

eio\_read — Читає дані з файлу, починаючи із заданого усунення

### Опис

```methodsynopsis
eio_read(    mixed $fd,    int $length,    int $offset,    int $pri,    callable $callback,    mixed $data = NULL): resource
```

**eio\_read()** зчитує `length`байт из файла с описателем`fd`, начиная с байта`offset`. Прочитані дані передаються через параметр `result` у функцію `callback`

### Список параметрів

`fd`

Потік, ресурс сокету чи числовий файловий описувач.

`length`

Максимальне число байт, що зчитується.

`offset`

Зміщення у файлі.

`pri`

Пріоритет запитів: **`EIO_PRI_DEFAULT`** **`EIO_PRI_MIN`** **`EIO_PRI_MAX`**, или\*\*`null`**. Якщо передано **`null`**, то`pri`устанавливается в**`EIO_PRI_DEFAULT`\*\*

`callback`

Функция`callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eio\_get\_last\_error()](function.eio-get-last-error.md)

`data`

Дані, які потрібно передати у функцію `callback`

### Значення, що повертаються

**eio\_read()** передає лічені дані через параметр `result` у функцію `callback`

### Приклади

**Пример #1 Пример использования**eio\_read()\*\*\*\*

```php
<?php
// Открываем временный файл и пишем в него какие-либо данные
$temp_filename = "eio-temp-file.tmp";
$fp = fopen($temp_filename, "w");
fwrite($fp, "1234567890");
fclose($fp);

/* Вызывается, когда eio_read() завершает работу */
function my_read_cb($data, $result) {
    global $temp_filename;

 // Выводим прочитанные данные
    var_dump($result);

 // закрываем файл
    eio_close($data);
    eio_event_loop();

 // Удаляем временный файл
    @unlink($temp_filename);
}

/* Вызывается, когда eio_open() завершает работу */
function my_file_opened_callback($data, $result) {
 // $result должен содержать файловый описатель
    if ($result > 0) {
  // Прочитаем 5 байт, начиная с третьего
        eio_read($result, 5, 2, EIO_PRI_DEFAULT, "my_read_cb", $result);
        eio_event_loop();
    } else {
  // eio_open() завершила работу отказом
        unlink($data);
    }
}

// открываем файл для чтения и записи
eio_open($temp_filename, EIO_O_RDWR, NULL,
    EIO_PRI_DEFAULT, "my_file_opened_callback", $temp_filename);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
string(5) "34567"
```

### Дивіться також

-   [eio\_open()](function.eio-open.md) \- Відкриває файл
-   [eio\_write()](function.eio-write.md) \- Запис у файл
-   [eio\_close()](function.eio-close.md) \- Закрити файл
-   [eio\_event\_loop()](function.eio-event-loop.md) \- Взаємодіє з libeio, поки всі запити не будуть виконані
