---
navigation:
  - function.ldap-set-option.md: « ldap\_set\_option
  - function.ldap-sort.md: ldap\_sort »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_set\_rebind\_proc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_set\_rebind\_proc

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ldap\_set\_rebind\_proc — Встановити функцію зворотного дзвінка для повторного зв'язування під час посилального пошуку

### Опис

```methodsynopsis
ldap_set_rebind_proc(LDAP\Connection $ldap, ?callable $callback): bool
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`ldap` тепер чекає екземпляр [LDAP\\Connection](class.ldap-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) `ldap link` |
| 8.0.0 | `callback` тепер допускає значення null. |
