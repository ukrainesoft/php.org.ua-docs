---
navigation:
  - function.ldap-set-option.html: « ldapsetoption
  - function.ldap-sort.html: ldapsort »
  - index.html: PHP Manual
  - ref.ldap.html: Функції LDAP
title: ldapsetrebindproc
---
# ldapsetrebindproc

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

ldapsetrebindproc — Встановити функцію зворотного дзвінка для повторного зв'язування під час посилального пошуку

### Опис

```methodsynopsis
ldap_set_rebind_proc(LDAP\Connection $ldap, ?callable $callback): bool
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `ldap` тепер чекає екземпляр [LDAPConnection](class.ldap-connection.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `callback` тепер допускає значення null. |
