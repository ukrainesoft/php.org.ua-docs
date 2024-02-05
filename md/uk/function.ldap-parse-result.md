---
navigation:
  - function.ldap-parse-reference.md: « ldap\_parse\_reference
  - function.ldap-read.md: ldap\_read »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_parse\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_parse\_result

(PHP 4 >= 4.0.5, PHP 5, PHP 7, PHP 8)

ldap\_parse\_result — Витягти інформацію з результату

### Опис

```methodsynopsis
ldap_parse_result(    LDAP\Connection $ldap,    LDAP\Result $result,    int &$error_code,    string &$matched_dn = null,    string &$error_message = null,    array &$referrals = null,    array &$controls = null): bool
```

Обробляє результат пошуку LDAP.

### Список параметрів

`ldap`

Екземпляр [LDAP\\Connection](class.ldap-connection.md), що повертається функцією [ldap\_connect()](function.ldap-connect.md)

`result`

Екземпляр [LDAP\\Result](class.ldap-result.md), що повертається [ldap\_list()](function.ldap-list.md) або [ldap\_search()](function.ldap-search.md)

`error_code`

Посилання на змінну, якій надається код помилки LDAP, або якщо немає помилки.

`matched_dn`

Посилання на змінну, якій надається знайдений DN, якщо він визначається в запиті, інакше присвоюється **`null`**

`error_message`

Посилання на змінну, якій надається повідомлення про помилку LDAP, або порожній рядок, якщо немає помилки.

`referrals`

Посилання на змінну, якій присвоюється масив (array) з усіма посиланнями (referral) як рядків, чи порожній масив, якщо вони повернули.

`controls`

Масив (array) LDAP Controls, які були відправлені замість відповіді.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result` |
| 7.3.0 | Додано підтримку параметра `controls` |

### Приклади

**Пример #1 Пример использования**ldap\_parse\_result()\*\*\*\*

```php
<?php
$result = ldap_search($ldap, "cn=userref,dc=my-domain,dc=com", "(cn=user*)");
$errcode = $dn = $errmsg = $refs =  null;
if (ldap_parse_result($ldap, $result, $errcode, $dn, $errmsg, $refs)) {
    // различные операции с $errcode, $dn, $errmsg и $refs
}
?>
```
