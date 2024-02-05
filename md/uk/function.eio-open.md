---
navigation:
  - function.eio-nthreads.md: « eio\_nthreads
  - function.eio-poll.md: eio\_poll »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_open
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_open

(PECL eio >= 0.0.1dev)

eio\_open — Відкриває файл

### Опис

```methodsynopsis
eio_open(    string $path,    int $flags,    int $mode,    int $pri,    callable $callback,    mixed $data = NULL): resource
```

**eio\_open()** відкриває файл по заданому шляху `path`в режиме доступа`mode`

### Список параметрів

`path`

Шлях до файлу, що відкривається.

**Увага**

У деяких SAPI (як, наприклад, *PHP-FPM*) необхідно вказувати повний шлях. В іншому випадку відмова в роботі функції.

`flags`

Комбінація з однієї або кількох констант *EIO\_O\_\**. Сенс констант *EIO\_O\_\** той самий, що й у відповідних їм констант *O\_\**, визначених у заголовному файлі С `fnctl.h`По умолчанию принимается константа\*\*`EIO_O_RDWR`\*\*

`mode`

Комбінація з однієї або кількох констант *EIO\_S\_I\** (через побітове АБО). Сенс констант той самий, що й у відповідних їм констант *S\_I\**, визначених у заголовному файлі С [» sys/stat.h](http://pubs.opengroup.org/onlinepubs/9699919799/basedefs/sys_stat.h.md). Параметр обов'язковий, якщо створюється новий файл. В іншому випадку параметр ігнорується.

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

Дані, які будуть передаватися до `callback`\-функцію.

### Значення, що повертаються

**eio\_open()** повертає дескриптор файлу через аргумент `result`callback-функции`callback`В случае возникновения ошибки`result` дорівнюватиме **`-1`**

### Приклади

**Пример #1 Пример использования**eio\_open()\*\*\*\*

```php
<?php
$temp_filename = "eio-temp-file.tmp";

/* Будет вызываться после завершения работы eio_close() */
function my_close_cb($data, $result) {
 // Ноль указывает на успех операции
    var_dump($result == 0);
 @unlink($data);
}

/* Будет вызываться после завершения работы eio_open() */
function my_file_opened_callback($data, $result) {
 // $result должен содержать дескриптор файла
    var_dump($result > 0);

    if ($result > 0) {
  // закрываем файл
        eio_close($result, EIO_PRI_DEFAULT, "my_close_cb", $data);
        eio_event_loop();
    }
}

// создаём файл для чтения и записи
// запрещаем группе и другим пользователям делать что-либо с файлом
eio_open($temp_filename, EIO_O_CREAT | EIO_O_RDWR, EIO_S_IRUSR | EIO_S_IWUSR,
  EIO_PRI_DEFAULT, "my_file_opened_callback", $temp_filename);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
bool(true)
bool(true)
```

### Дивіться також

-   [eio\_mknod()](function.eio-mknod.md) \- Створює спеціальний чи звичайний файл
