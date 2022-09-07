---
navigation:
  - function.eio-grp-limit.md: « eiogrplimit
  - function.eio-init.md: eioinit »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функции
title: eiogrp
---
# eiogrp

(PECL eio >= 0.0.1dev)

eiogrp — Створює групу запитів

### Опис

```methodsynopsis
eio_grp(callable $callback, string $data = NULL): resource
```

**eiogrp()** створює групу запитів.

### Список параметрів

`callback`

Функція `callback` викликається після завершення запиту. Вона повинна задовольняти наступний прототип:

```php
void callback(mixed $data, int $result[, resource $req]);
```

`data`

є даними користувача, переданими в запиті.

`result`

містить результуюче значення, що залежить від запиту; зазвичай це значення, яке повертається відповідним системним викликом.

`req`

є опціональним запитуваним ресурсом, який може використовуватися з такими функціями як [eiogetlasterror()](function.eio-get-last-error.md)

`data`

Довільна змінна, що передається в `callback`функцію.

### Значення, що повертаються

**eiogrp()** повертає покажчик на запит у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **eiogrp()****

```php
<?php
$temp_filename = dirname(__FILE__) ."/eio-file.tmp";
$fp = fopen($temp_filename, "w");
fwrite($fp, "some data");
fclose($fp);
$my_file_fd = NULL;

/* Вызывается, когда группа запросов будет выполнена */
function my_grp_done($data, $result) {
 // Если файл существует, удаляем
 @unlink($data);
}

/* Вызывается когда файл открыт */
function my_grp_file_opened_callback($data, $result) {
 global $my_file_fd, $grp;

 $my_file_fd = $result;

 $req = eio_read($my_file_fd, 4, 0,
   EIO_PRI_DEFAULT, "my_grp_file_read_callback");
 eio_grp_add($grp, $req);
}

/* Вызывается, когда файл прочтён */
function my_grp_file_read_callback($data, $result) {
 global $my_file_fd, $grp;

 var_dump($result);

 // Создание запроса на закрытие файла
 $req = eio_close($my_file_fd);

 // Добавление запроса в группу
 eio_grp_add($grp, $req);
}

// Создание группы
$grp = eio_grp("my_grp_done", $temp_filename);

// Создание запроса
$req = eio_open($temp_filename, EIO_O_RDWR | EIO_O_APPEND , NULL,
  EIO_PRI_DEFAULT, "my_grp_file_opened_callback", NULL);

// Добавление запроса в группу
eio_grp_add($grp, $req);

// Выполнение запросов
eio_event_loop();
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(4) "some"
```

### Дивіться також

-   [eiogrpcancel()](function.eio-grp-cancel.md) - Скасує групу запитів
-   [eiogrpadd()](function.eio-grp-add.md) - Додає запит до групи запитів
