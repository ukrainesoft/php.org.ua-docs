---
navigation:
  - function.getservbyport.md: « getservbyport
  - function.header-remove.md: header\_remove »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: header\_register\_callback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# header\_register\_callback

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

header\_register\_callback — Викликає функцію заголовка

### Опис

```methodsynopsis
header_register_callback(callable $callback): bool
```

Реєструє функцію, яка буде викликана, коли PHP почне відправляти висновок.

Параметр`callback` запускається відразу після того, як PHP були підготовлені всі заголовки, що відправляються, і перед відправкою будь-якого іншого висновку, створюючи можливість для управління вихідними заголовками перед відправкою.

### Список параметрів

`callback`

Функція викликається безпосередньо перед відправкою заголовків, не отримує параметрів і значення, що повертається, ігнорується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**header\_register\_callback()\*\*\*\*

```php
<?php

header('Content-Type: text/plain');
header('X-Test: foo');

function foo() {
 foreach (headers_list() as $header) {
   if (strpos($header, 'X-Powered-By:') !== false) {
     header_remove('X-Powered-By');
   }
   header_remove('X-Test');
 }
}

$result = header_register_callback('foo');
echo "a";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Content-Type: text/plain

a
```

### Примітки

Функция**header\_register\_callback()** запускається по готовності відправки заголовків, так що будь-який висновок із цієї функції може перервати висновок.

> **Зауваження** :
> 
> Доступ до заголовків та їх висновок здійснюватиметься лише у випадку, якщо у SAPI є їх підтримка.

### Дивіться також

-   [headers\_list()](function.headers-list.md) \- Повертає список переданих заголовків (або готових до відправлення)
-   [header\_remove()](function.header-remove.md) \- Видаляє раніше встановлені заголовки
-   [header()](function.header.md) \- Надсилає необроблений (сирий) HTTP-заголовок
