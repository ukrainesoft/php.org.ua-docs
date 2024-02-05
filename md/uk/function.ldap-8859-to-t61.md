---
navigation:
  - ref.ldap.md: « Функції LDAP
  - function.ldap-add-ext.md: ldap\_add\_ext »
  - index.md: PHP Manual
  - ref.ldap.md: Функції LDAP
title: ldap\_8859\_to\_t61
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ldap\_8859\_to\_t61

(PHP 4 >= 4.0.2, PHP 5, PHP 7, PHP 8)

ldap\_8859\_to\_t61 — Переводить символи з кодування ISO-8859 до t61

### Опис

```methodsynopsis
ldap_8859_to_t61(string $value): string|false
```

Перекладає символи з кодування `ISO-8859`в`t61`

Ця функція корисна, якщо потрібно працювати зі застарілим сервером `LDAPv2`

### Список параметрів

`value`

Текст, який має бути переведений.

### Значення, що повертаються

Повертає кодований у `t61`параметр`value`или\*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ldap\_t61\_to\_8859()](function.ldap-t61-to-8859.md) \- Перекладає символи з кодування t61 ISO-8859
