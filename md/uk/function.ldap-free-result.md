---
navigation:
  - function.ldap-first-reference.html: « ldapfirstreference
  - function.ldap-get-attributes.html: ldapgetattributes »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldapfreeresult
---
# ldapfreeresult

(PHP 4, PHP 5, PHP 7, PHP 8)

ldapfreeresult — Звільнити пам'ять результату

### Опис

```methodsynopsis
ldap_free_result(LDAP\Result $result): bool
```

Звільняє пам'ять, внутрішньо виділену зберігання результату. Вся пам'ять результату буде автоматично звільнена після завершення сценарію.

Зазвичай вся пам'ять, виділена для результату LDAP, звільняється наприкінці сценарію. У випадку, якщо сценарій робить послідовні операції пошуку, які повертають великі набори результатів, **ldapfreeresult()** може бути викликана, щоб зберегти невелике використання пам'яті під час сценарію.

### Список параметрів

`result`

Екземпляр [LDAPResult](class.ldap-result.html), що повертається [ldaplist()](function.ldap-list.html) або [ldapsearch()](function.ldap-search.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [LDAPResult](class.ldap-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |
