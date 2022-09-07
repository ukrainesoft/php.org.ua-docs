---
navigation:
  - function.ldap-rename.md: « ldaprename
  - function.ldap-search.md: ldapsearch »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapsaslbind
---
# ldapsaslbind

(PHP 5, PHP 7, PHP 8)

ldapsaslbind — Прив'язати до LDAP директорії за допомогою SASL

### Опис

```methodsynopsis
ldap_sasl_bind(    LDAP\Connection $ldap,    ?string $dn = null,    ?string $password = null,    ?string $mech = null,    ?string $realm = null,    ?string $authc_id = null,    ?string $authz_id = null,    ?string $props = null): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `dn` `password` `mech` `realm` `authc_id` `authz_id` and `props` тепер допускають значення null. |

### Примітки

> **Зауваження** **Вимога**  
> **ldapsaslbind()** вимагає підтримки SASL (sasl.h). Перевірте, що ви використовували `--with-ldap-sasl` при конфігуруванні PHP, інакше ця функція не буде визначена.
