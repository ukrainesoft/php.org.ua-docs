---
navigation:
  - function.ldap-rename.md: « ldap\_rename
  - function.ldap-search.md: ldap\_search »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_sasl\_bind
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_sasl\_bind

(PHP 5, PHP 7, PHP 8)

ldap\_sasl\_bind — Прив'язати до LDAP директорії за допомогою SASL

### Опис

```methodsynopsis
ldap_sasl_bind(    LDAP\Connection $ldap,    ?string $dn = null,    ?string $password = null,    ?string $mech = null,    ?string $realm = null,    ?string $authc_id = null,    ?string $authz_id = null,    ?string $props = null): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.0.0 | `dn` `password` `mech` `realm` `authc_id` `authz_id`and`props` тепер допускають значення null. |

### Примітки

> **Зауваження** **Вимога**  
> **ldap\_sasl\_bind()** вимагає підтримки SASL (sasl.h). Перевірте, що ви використовували `--with-ldap-sasl` при конфігуруванні PHP, інакше ця функція не буде визначена.
