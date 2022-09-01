---
navigation:
  - function.oci-pconnect.html: « ocipconnect
  - function.oci-result.html: ociresult »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ociregistertafcallback
---
# ociregistertafcallback

(PHP 7.0 >= 7.0.21, PHP 8, PHP 7 >= 7.1.7, PHP 8, PECL OCI8 >= 2.1.7)

ociregistertafcallback — Реєструє функцію зворотного дзвінка для Oracle Database TAF

### Опис

```methodsynopsis
oci_register_taf_callback(resource $connection, ?callable $callback): bool
```

Реєструє користувальницьку функцію зворотного дзвінка для з'єднання `connection`. Якщо з'єднання `connection` обірвалося через проблеми з БД або мережею, буде здійснено кілька запусків зареєстрованої функції у процесі відновлення. Детальніше читайте [OCI8 Transparent Application Failover (TAF) Support](oci8.taf.md)

Кожен новий виклик **ociregistertafcallback()** затиратиме попередні реєстрації.

Для явного видалення реєстрації використовуйте функцію [ociunregistertafcallback()](function.oci-unregister-taf-callback.md)

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

Опис параметрів та приклади дивіться на сторінці [OCI8 Transparent Application Failover (TAF) Support](oci8.taf.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ociunregistertafcallback()](function.oci-unregister-taf-callback.md) - Видалити реєстрацію користувача callback-функції для Oracle Database TAF
