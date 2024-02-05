---
navigation:
  - function.ldap-first-reference.md: « ldap\_first\_reference
  - function.ldap-get-attributes.md: ldap\_get\_attributes »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_free\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_free\_result

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_free\_result — Звільнити пам'ять результату

### Опис

```methodsynopsis
ldap_free_result(LDAP\Result $result): bool
```

Звільняє пам'ять, внутрішньо виділену зберігання результату. Вся пам'ять результату буде автоматично звільнена після завершення сценарію.

Зазвичай вся пам'ять, виділена для результату LDAP, звільняється наприкінці сценарію. У випадку, якщо сценарій робить послідовні операції пошуку, які повертають великі набори результатів, **ldap\_free\_result()** може бути викликана, щоб зберегти невелике використання пам'яті під час сценарію.

### Список параметрів

`result`

Екземпляр [LDAP\\Result](class.ldap-result.md), що повертається [ldap\_list()](function.ldap-list.md) або [ldap\_search()](function.ldap-search.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [LDAP\\Result](class.ldap-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap result` |
