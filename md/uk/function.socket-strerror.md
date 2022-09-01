---
navigation:
  - function.socket-shutdown.html: « socketshutdown
  - function.socket-write.html: socketwrite »
  - index.html: PHP Manual
  - ref.sockets.html: Функции сокета
title: socketstrerror
---
# socketstrerror

(PHP 4> = 4.1.0, PHP 5, PHP 7, PHP 8)

socketstrerror — Повертає рядок, що описує помилку сокету

### Опис

```methodsynopsis
socket_strerror(int $error_code): string
```

**socketstrerror()** отримує як параметр `error_code` код помилки сокета, що повертається функцією [socketlasterror()](function.socket-last-error.html) та повертає відповідний текст із роз'ясненням.

> **Зауваження**
> 
> Хоча повідомлення про помилки, створені модулем socket, англійською мовою, системні повідомлення, що отримуються цією функцією, будуть з'являтися залежно від поточної локалі (**`LC_MESSAGES`**

### Список параметрів

`error_code`

Допустимий код помилки сокету, швидше за все, повернутий функцією [socketlasterror()](function.socket-last-error.html)

### Значення, що повертаються

Повертає повідомлення про помилку, пов'язане з параметром `error_code`

### Приклади

**Приклад #1 Приклад використання **socketstrerror()****

```php
<?php
if (false == ($socket = @socket_create(AF_INET, SOCK_STREAM, SOL_TCP))) {
   echo "socket_create() не выполнена: причина: " . socket_strerror(socket_last_error()) . "\n";
}

if (false == (@socket_bind($socket, '127.0.0.1', 80))) {
   echo "socket_bind() не выполнена: причина: " . socket_strerror(socket_last_error($socket)) . "\n";
}
?>
```

Очікуваний висновок з прикладу вище (мається на увазі, що скрипт не запущений з привілеями суперкористувача root):

```
socket_bind() не выполнена: причина: Доступ запрещён
```

### Дивіться також

-   [socketaccept()](function.socket-accept.html) - приймає з'єднання на сокеті
-   [socketbind()](function.socket-bind.html) - Прив'язує ім'я до сокету
-   [socketconnect()](function.socket-connect.html) - Починає з'єднання із сокетом
-   [socketlisten()](function.socket-listen.html) - Прослуховує вхідні з'єднання на сокеті
-   [socketcreate()](function.socket-create.html) - створює сокет (кінцеву точку для обміну інформацією)
