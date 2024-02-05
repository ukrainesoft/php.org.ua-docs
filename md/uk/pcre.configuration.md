---
navigation:
  - pcre.installation.md: « Встановлення
  - pcre.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - pcre.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції конфігурації PCRE**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [pcre.backtrack\_limit](pcre.configuration.md#ini.pcre.backtrack-limit) | "1000000" | **`INI_ALL`** |  |
| [pcre.recursion\_limit](pcre.configuration.md#ini.pcre.recursion-limit) | "100000" | **`INI_ALL`** |  |
| [pcre.jit](pcre.configuration.md#ini.pcre.jit) | "1" | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`pcre.backtrack_limit`int

Ліміт зворотних посилань PCRE. Для PHP < 5.3.7 значення за промовчанням 100000.

`pcre.recursion_limit`int

Ліміт на рекурсію. Не забувайте про те, що якщо ви встановите досить високе значення, то PCRE може перевищити розмір стека (встановлений операційною системою) і зрештою викличе падіння PHP.

`pcre.jit`bool

Чи використовуватиметься JIT-компіляція PCRE.
