---
navigation:
  - ldap.installation.md: « Встановлення
  - ldap.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - ldap.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції конфігурації LDAP**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [ldap.max\_links](ldap.configuration.md#ini.ldap.max_links) | "-1" | **`INI_SYSTEM`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`ldap.max_links`int

Максимальна кількість з'єднань LDAP на процес.
