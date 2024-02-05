---
navigation:
  - function.ldap-get-option.md: « ldap\_get\_option
  - function.ldap-get-values.md: ldap\_get\_values »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_get\_values\_len
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_get\_values\_len

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_get\_values\_len — Отримати всі бінарні значення із запису результату

### Опис

```methodsynopsis
ldap_get_values_len(LDAP\Connection $ldap, LDAP\ResultEntry $entry, string $attribute): array|false
```

Читає всі значення атрибута запису результату.

Ця функція використовується так само як і [ldap\_get\_values()](function.ldap-get-values.md) за винятком того, що обробляє двійкові дані, а не рядкові.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`entry`

Екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md)

`attribute`

### Значення, що повертаються

Повертає масив значень для атрибуту у разі успішного виконання та **`false`** у разі виникнення помилки. Окремі значення доступні за цілим індексом в масиві. Перший індекс 0. Число значень може бути знайдено за індексом "count" у результуючому масиві.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`entry` тепер чекає екземпляр [LDAP\\ResultEntry](class.ldap-result-entry.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result entry` |

### Дивіться також

-   [ldap\_get\_values()](function.ldap-get-values.md) \- Отримує всі значення із запису результату
