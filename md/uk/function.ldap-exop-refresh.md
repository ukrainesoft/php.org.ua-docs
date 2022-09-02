---
navigation:
  - function.ldap-exop-passwd.md: « ldapexoppasswd
  - function.ldap-exop-whoami.md: ldapexopwhoami »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapexoprefresh
---
# ldapexoprefresh

(PHP 7> = 7.3.0, PHP 8)

ldapexoprefresh — Обгортка для розширеної операції Refresh

### Опис

```methodsynopsis
ldap_exop_refresh(LDAP\Connection $ldap, string $dn, int $ttl): int|false
```

Виконує розширену операцію Performs та повертає результат.

### Список параметрів

`ldap`

Екземпляр [LDAPConnection](class.ldap-connection.md), що повертається функцією [ldapconnect()](function.ldap-connect.md)

`dn`

Унікальне ім'я (DN) запису для якого виконується операція.

`ttl`

Час у секундах (від 1 до 31557600) існування запису в каталозі, запрошеному клієнтом. Після цього часу вона буде автоматично видалена.

### Значення, що повертаються

З RFC: Поле responseTtl містить час у секундах, що вважається сервером часом життя запису. Воно не може бути менше за запитане клієнтом, але може бути більше. Однак, щоб дозволити серверам підтримувати каталог у відносно консистентному стані та для запобігання зловживання клієнтами постійним продовженням, серверу дозволено зменшувати запитане клієнтом значення до, але не менше ніж 86400 секунд (один день). У разі виникнення помилки поверне **`false`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Дивіться також

-   [ldapexop()](function.ldap-exop.md) - Виконує розширену операцію
