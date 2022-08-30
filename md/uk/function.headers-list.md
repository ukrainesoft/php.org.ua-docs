Повертає список переданих заголовків (або готових до відправлення)

-   [« header](function.header.html)
    
-   [headerssent »](function.headers-sent.html)
    
-   [PHP Manual](index.html)
    
-   [Мережеві функції](ref.network.html)
    
-   Повертає список переданих заголовків (або готових до відправлення)
    

# headerslist

(PHP 5, PHP 7, PHP 8)

headerslist — Повертає список переданих заголовків (або готових до надсилання)

### Опис

```methodsynopsis
headers_list(): array
```

Функція **headerslist()** повертає список заголовків, що передаються браузеру/клієнту. Для того, щоб визначити, чи вже передані заголовки, використовуйте функцію [headerssent()](function.headers-sent.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає нумерований масив заголовків.

### Приклади

**Приклад #1 Приклад використання **headerslist()****

```php
<?php

/* Функция setcookie() добавит заголовок сама по себе */
setcookie('foo', 'bar');

/* Определение пользовательского заголовка
   Это будет проигнорировано большинством клиентов */
header("Example-Test: foo");

/* Передача простого текстового контента */
header('Content-Type: text/plain; charset=UTF-8');

/* Какие заголовки будут отправлены? */
var_dump(headers_list());

?>
```

Результатом виконання цього прикладу буде щось подібне:

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

> **Зауваження**
> 
> Доступ до заголовків та їх висновок здійснюватиметься лише у випадку, якщо у SAPI є їх підтримка.

### Дивіться також

-   [headerssent()](function.headers-sent.html) - Перевіряє, чи були надіслані заголовки
-   [header()](function.header.html) - Надсилання HTTP-заголовка
-   [setcookie()](function.setcookie.html) - Надсилає cookie
-   [apacheresponseheaders()](function.apache-response-headers.html) - Повертає список усіх HTTP-заголовків відповіді Apache
-   [httpresponsecode()](function.http-response-code.html) - Отримує або встановлює код відповіді HTTP