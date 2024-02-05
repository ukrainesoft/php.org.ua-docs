---
navigation:
  - function.eio-grp-limit.md: « eio\_grp\_limit
  - function.eio-init.md: eio\_init »
  - index.md: PHP Manual
  - ref.eio.md: Eio Функції
title: eio\_grp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# eio\_grp

(PECL eio >= 0.0.1dev)

eio\_grp — Створює групу запитів

### Опис

```methodsynopsis
eio_grp(callable $callback, string $data = NULL): resource
```

**eio\_grp()** створює групу запитів.

### Список параметрів

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

**eio\_grp()** повертає покажчик на запит у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**eio\_grp()\*\*\*\*

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

Висновок наведеного прикладу буде схожим на:

```
string(4) "some"
```

### Дивіться також

-   [eio\_grp\_cancel()](function.eio-grp-cancel.md) \- Скасує групу запитів
-   [eio\_grp\_add()](function.eio-grp-add.md) \- Додає запит до групи запитів
