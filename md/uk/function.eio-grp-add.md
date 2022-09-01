---
navigation:
  - function.eio-get-last-error.html: « eiogetlasterror
  - function.eio-grp-cancel.html: eiogrpcancel »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiogrpadd
---
# eiogrpadd

(PECL eio >= 0.0.1dev)

eiogrpadd — Додає запит до групи запитів

### Опис

```methodsynopsis
eio_grp_add(resource $grp, resource $req): void
```

**eiogrpadd()** додає запит до групи запитів.

### Список параметрів

`grp`

Вказівник на групу запитів, повернутий [eiogrp()](function.eio-grp.md)

`req`

Покажчик на ресурс

### Значення, що повертаються

Функція не повертає значення після виконання.

### Приклади

**Приклад #1 Створення групи запитів**

```php
<?php
/*
 * Создание группы запросов для открытия, чтения и закрытия файла
 */

//Создание временного файла и запись в него нескольких байт
$temp_filename = dirname(__FILE__) ."/eio-file.tmp";
$fp = fopen($temp_filename, "w");
fwrite($fp, "some data");
fclose($fp);

/* Вызывается, когда группа запросов будет выполнена */
function my_grp_done($data, $result) {
 var_dump($result == 0);
 @unlink($data);
}

/* Вызывается после выполнения eio_open() */
function my_grp_file_opened_callback($data, $result) {
 global $grp;

 // $result должен содержать дескриптор файла
 var_dump($result > 0);

 // Создание запроса eio_read() и добавление в группу
 // Дескриптор файла передаётся в callback-функцию
 $req = eio_read($result, 4, 0,
   EIO_PRI_DEFAULT, "my_grp_file_read_callback", $result);
 eio_grp_add($grp, $req);
}

/* Вызывается после выполнения eio_read() */
function my_grp_file_read_callback($data, $result) {
 global $grp;

 // Чтение байтов
 var_dump($result);

 // Создание запроса eio_close() и добавление в группу
 // $data должна содержать дескриптор файла
 $req = eio_close($data);
 eio_grp_add($grp, $req);
}

// Создание группу запросов
$grp = eio_grp("my_grp_done", $temp_filename);
var_dump($grp);

// Создание запроса eio_open() и добавление в группу
$req = eio_open($temp_filename, EIO_O_RDWR | EIO_O_APPEND , NULL,
  EIO_PRI_DEFAULT, "my_grp_file_opened_callback", NULL);
eio_grp_add($grp, $req);

// Выполнение запросов
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
resource(6) of type (EIO Group Descriptor)
bool(true)
string(4) "some"
bool(true)
```

### Дивіться також

-   [eiogrp()](function.eio-grp.md) - Створює групу запитів
-   [eiogrpcancel()](function.eio-grp-cancel.md) - Скасує групу запитів
-   [eiogrplimit()](function.eio-grp-limit.md) - Встановлює граничну кількість запитів у групі
