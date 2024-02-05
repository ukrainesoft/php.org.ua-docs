---
navigation:
  - function.header.md: « header
  - function.headers-sent.md: headers\_sent »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: headers\_list
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# headers\_list

(PHP 5, PHP 7, PHP 8)

headers\_list — Повертає список переданих заголовків (або готових до надсилання)

### Опис

```methodsynopsis
headers_list(): array
```

Функция**headers\_list()** повертає список заголовків, що передаються браузеру/клієнту. Для того, щоб визначити, чи вже передані заголовки, використовуйте функцію [headers\_sent()](function.headers-sent.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає нумерований масив заголовків.

### Приклади

**Пример #1 Пример использования**headers\_list()\*\*\*\*

```php
<?php

/* Функция setcookie() добавит заголовок сама по себе */
setcookie('foo', 'bar');

/* Определение пользовательского заголовка
   Это будет проигнорировано большинством клиентов */
header("Example-Test: foo");

/* Передача простого текстового контента */
header('Content-Type: text/plain; charset=UTF-8');

/* Какие заголовки будут отправлены? */
var_dump(headers_list());

?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  string(19) "Set-Cookie: foo=bar"
  [1]=>
  string(17) "Example-Test: foo"
  [2]=>
  string(39) "Content-Type: text/plain; charset=UTF-8"
}
```

### Примітки

> **Зауваження** :
> 
> Доступ до заголовків та їх висновок здійснюватиметься лише у випадку, якщо у SAPI є їх підтримка.

### Дивіться також

-   [headers\_sent()](function.headers-sent.md) \- Перевіряє, чи були надіслані заголовки
-   [header()](function.header.md) \- Надсилає необроблений (сирий) HTTP-заголовок
-   [setcookie()](function.setcookie.md) \- Надсилає cookie
-   [apache\_response\_headers()](function.apache-response-headers.md) \- Повертає список усіх HTTP-заголовків відповіді Apache
-   [http\_response\_code()](function.http-response-code.md) \- Отримує або встановлює код відповіді HTTP
