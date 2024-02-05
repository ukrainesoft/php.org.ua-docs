---
navigation:
  - function.ldap-exop-passwd.md: « ldap\_exop\_passwd
  - function.ldap-exop-sync.md: ldap\_exop\_sync »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_exop\_refresh
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_exop\_refresh

(PHP 7 >= 7.3.0, PHP 8)

ldap\_exop\_refresh — Обгортка для розширеної операції Refresh

### Опис

```methodsynopsis
ldap_exop_refresh(LDAP\Connection $ldap, string $dn, int $ttl): int|false
```

Виконує розширену операцію Performs та повертає результат.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`dn`

Унікальне ім'я (DN) запису для якого виконується операція.

`ttl`

Час у секундах (від 1 до 31557600) існування запису в каталозі, запрошеному клієнтом. Після цього часу вона буде автоматично видалена.

### Значення, що повертаються

З RFC: Поле responseTtl містить час у секундах, що вважається сервером часом життя запису. Воно не може бути менше за запитане клієнтом, але може бути більше. Однак, щоб дозволити серверам підтримувати каталог у відносно консистентному стані та для запобігання зловживання клієнтами постійним продовженням, серверу дозволено зменшувати запитане клієнтом значення до, але не менше ніж 86400 секунд (один день). У разі виникнення помилки поверне **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |

### Дивіться також

-   [ldap\_exop()](function.ldap-exop.md) \- Виконує розширену операцію
