---
navigation:
  - function.oci-pconnect.md: « oci\_pconnect
  - function.oci-result.md: oci\_result »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_register\_taf\_callback
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_register\_taf\_callback

(PHP 7.0 >= 7.0.21, PHP 8, PHP 7 >= 7.1.7, PHP 8, PECL OCI8 >= 2.1.7)

oci\_register\_taf\_callback — Реєструє функцію зворотного дзвінка для Oracle Database TAF

### Опис

```methodsynopsis
oci_register_taf_callback(resource $connection, ?callable $callback): bool
```

Реєструє користувальницьку функцію зворотного дзвінка для з'єднання `connection`. Якщо з'єднання `connection` обірвалося через проблеми з БД або мережею, буде здійснено кілька запусків зареєстрованої функції у процесі відновлення. Детальніше читайте [OCI8 Transparent Application Failover (TAF) Support](oci8.taf.md)

Кожен новий виклик **oci\_register\_taf\_callback()** затиратиме попередні реєстрації.

Для явного видалення реєстрації використовуйте функцію [oci\_unregister\_taf\_callback()](function.oci-unregister-taf-callback.md)

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [oci\_unregister\_taf\_callback()](function.oci-unregister-taf-callback.md) \- Видалити реєстрацію користувача callback-функції для Oracle Database TAF
