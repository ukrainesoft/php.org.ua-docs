---
navigation:
  - function.ldap-delete.md: « ldap\_delete
  - function.ldap-err2str.md: ldap\_err2str »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_dn2ufn
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_dn2ufn

(PHP 4, PHP 5, PHP 7, PHP 8)

ldap\_dn2ufn — Перетворити DN на зручний для користувача формат іменування

### Опис

```methodsynopsis
ldap_dn2ufn(string $dn): string|false
```

Перемикає вказаний `dn` більш зручну для користувача форму, знімаючи ізоляцію з імен типів.

### Список параметрів

`dn`

Відмінна назва об'єкта LDAP.

### Значення, що повертаються

Повертає зручне для користувача ім'я або \*\*`false`\*\*в случае возникновения ошибки.
