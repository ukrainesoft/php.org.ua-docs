---
navigation:
  - function.eio-fdatasync.md: « eio\_fdatasync
  - function.eio-fstatvfs.md: eio\_fstatvfs »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_fstat
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_fstat

(PECL eio >= 0.0.1dev)

eio\_fstat — Повертає статус файлу

### Опис

```methodsynopsis
eio_fstat(    mixed $fd,    int $pri,    callable $callback,    mixed $data = ?): resource
```

**eio\_fstat()** повертає інформацію про стан файлу в `result`аргументе`callback`

### Список параметрів

`fd`

Потік, покажчик на сокет або числовий дескриптор файлу.

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

Произвольная переменная, передаваемая в`callback`\-функцію.

### Значення, що повертаються

[eio\_busy()](function.eio-busy.md) повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад использования[eio\_lstat()](function.eio-lstat.md)**

```php
<?php
// Создание временного файла
$tmp_filename = dirname(__FILE__) ."/eio-file.tmp";
touch($tmp_filename);

/* Вызывается после завершения eio_fstat() */
function my_res_cb($data, $result) {
 // Выводит массив с информацией о состоянии файла
 var_dump($result);

 if ($data['fd']) {
  // Закрывает временный файл
  eio_close($data['fd']);
  eio_event_loop();
 }
 // Удаляет временный файл
 @unlink($data['file']);
}

/* Вызывается после завершения eio_open() */
function my_open_cb($data, $result) {
 // Подготовка данных для callback
 $d = array(
  'fd'  => $result,
  'file'=> $data
 );
 // Получение информации о файле
 eio_fstat($result, EIO_PRI_DEFAULT, "my_res_cb", $d);
 // Выполнение запросов
 eio_event_loop();
}

// Открытие временного файла
eio_open($tmp_filename, EIO_O_RDONLY, NULL, EIO_PRI_DEFAULT,
  "my_open_cb", $tmp_filename);
eio_event_loop();
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(12) {
 ["st_dev"]=>
  int(2050)
  ["st_ino"]=>
  int(2489159)
  ["st_mode"]=>
  int(33188)
  ["st_nlink"]=>
  int(1)
  ["st_uid"]=>
  int(1000)
  ["st_gid"]=>
  int(100)
  ["st_rdev"]=>
  int(0)
  ["st_blksize"]=>
  int(4096)
  ["st_blocks"]=>
  int(0)
  ["st_atime"]=>
  int(1318239506)
  ["st_mtime"]=>
  int(1318239506)
  ["st_ctime"]=>
  int(1318239506)
}
```

### Дивіться також

-   [eio\_lstat()](function.eio-lstat.md) \- Повертає статус файлу
-   [eio\_stat()](function.eio-stat.md) \- Повертає статус файлу
