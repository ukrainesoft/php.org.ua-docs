Викликає функцію заголовка

-   [« getservbyport](function.getservbyport.html)
    
-   [headerremove »](function.header-remove.html)
    
-   [PHP Manual](index.html)
    
-   [Мережеві функції](ref.network.html)
    
-   Викликає функцію заголовка
    

# headerregistercallback

(PHP 5> = 5.4.0, PHP 7, PHP 8)

headerregistercallback — Викликає функцію заголовка

### Опис

```methodsynopsis
header_register_callback(callable $callback): bool
```

Реєструє функцію, яка буде викликана, коли PHP почне відправляти висновок.

Параметр `callback` запускається відразу після того, як PHP були підготовлені всі заголовки, що відправляються, і перед відправкою будь-якого іншого висновку, створюючи можливість для управління вихідними заголовками перед відправкою.

### Список параметрів

`callback`

Функція викликається безпосередньо перед відправкою заголовків, не отримує параметрів і значення, що повертається, ігнорується.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **headerregistercallback()****

```php
<?php

header('Content-Type: text/plain');
header('X-Test: foo');

function foo() {
 foreach (headers_list() as $header) {
   if (strpos($header, 'X-Powered-By:') !== false) {
     header_remove('X-Powered-By');
   }
   header_remove('X-Test');
 }
}

$result = header_register_callback('foo');
echo "a";
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Content-Type: text/plain

a
```

### Примітки

Функція **headerregistercallback()** запускається по готовності відправлення заголовків, так що будь-який висновок із цієї функції може перервати висновок.

> **Зауваження**
> 
> Доступ до заголовків та їх висновок здійснюватиметься лише у випадку, якщо у SAPI є їх підтримка.

### Дивіться також

-   [headerslist()](function.headers-list.html) - Повертає список переданих заголовків (або готових до відправлення)
-   [headerremove()](function.header-remove.html) - Видаляє раніше встановлені заголовки
-   [header()](function.header.html) - Надсилання HTTP-заголовка