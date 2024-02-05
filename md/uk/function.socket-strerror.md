---
navigation:
  - function.socket-shutdown.md: « socket\_shutdown
  - function.socket-write.md: socket\_write »
  - index.md: PHP Manual
  - ref.sockets.md: Опції сокету
title: socket\_strerror
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# socket\_strerror

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

socket\_strerror — Повертає рядок, що описує помилку сокету

### Опис

```methodsynopsis
socket_strerror(int $error_code): string
```

**socket\_strerror()** отримує як параметр `error_code` код помилки сокета, що повертається функцією [socket\_last\_error()](function.socket-last-error.md) та повертає відповідний текст із роз'ясненням.

> **Зауваження** :
> 
> Хоча повідомлення про помилки, створені модулем socket, англійською мовою, системні повідомлення, що отримуються цією функцією, з'являтимуться залежно від поточної локалі (**`LC_MESSAGES`**

### Список параметрів

`error_code`

Допустимий код помилки сокету, швидше за все, повернутий функцією [socket\_last\_error()](function.socket-last-error.md)

### Значення, що повертаються

Повертає повідомлення про помилку, пов'язане з параметром `error_code`

### Приклади

**Пример #1 Пример использования**socket\_strerror()\*\*\*\*

```php
<?php
if (false == ($socket = @socket_create(AF_INET, SOCK_STREAM, SOL_TCP))) {
   echo "socket_create() не выполнена: причина: " . socket_strerror(socket_last_error()) . "\n";
}

if (false == (@socket_bind($socket, '127.0.0.1', 80))) {
   echo "socket_bind() не выполнена: причина: " . socket_strerror(socket_last_error($socket)) . "\n";
}
?>
```

Очікуваний висновок з прикладу вище (мається на увазі, що скрипт не запущений з привілеями суперкористувача root):

```
socket_bind() не выполнена: причина: Доступ запрещён
```

### Дивіться також

-   [socket\_accept()](function.socket-accept.md) \- приймає з'єднання на сокеті
-   [socket\_bind()](function.socket-bind.md) \- Прив'язує ім'я до сокету
-   [socket\_connect()](function.socket-connect.md) \- Починає з'єднання із сокетом
-   [socket\_listen()](function.socket-listen.md) \- Прослуховує вхідні з'єднання на сокеті
-   [socket\_create()](function.socket-create.md) \- створює сокет (кінцеву точку для обміну інформацією)
