Реєструє функцію зворотного виклику для Oracle Database TAF

-   [« oci\_pconnect](function.oci-pconnect.html)
    
-   [oci\_result »](function.oci-result.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Реєструє функцію зворотного виклику для Oracle Database TAF
    

# ociregistertafcallback

(PHP 7.0 >= 7.0.21, PHP 8, PHP 7 >= 7.1.7, PHP 8, PECL OCI8 >= 2.1.7)

ociregistertafcallback — Реєструє функцію зворотного дзвінка для Oracle Database TAF

### Опис

```methodsynopsis
oci_register_taf_callback(resource $connection, ?callable $callback): bool
```

Реєструє користувальницьку функцію зворотного дзвінка для з'єднання `connection`. Якщо з'єднання `connection` обірвалося через проблеми з БД або мережею, буде здійснено кілька запусків зареєстрованої функції у процесі відновлення. Детальніше читайте [OCI8 Transparent Application Failover (TAF) Support](oci8.taf.html)

Кожен новий виклик **ociregistertafcallback()** затиратиме попередні реєстрації.

Для явного видалення реєстрації використовуйте функцію [oci\_unregister\_taf\_callback()](function.oci-unregister-taf-callback.html)

Реєстрація функції зворотного дзвінка НЕ ​​зберігається для постійних з'єднань, отже, при кожному новому постійному з'єднанні її необхідно перереєструвати.

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle.

`callback`

Функція реєстрації для Oracle TAF. Можливо як рядком з ім'ям функції, і замиканням (анонімною функцією).

Інтерфейс функції наступний:

```methodsynopsis
userCallbackFn(resource $connection, int $event, int $type): int
```

Опис параметрів та приклади дивіться на сторінці [OCI8 Transparent Application Failover (TAF) Support](oci8.taf.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [oci\_unregister\_taf\_callback()](function.oci-unregister-taf-callback.html) - Видалити реєстрацію користувача callback-функції для Oracle Database TAF