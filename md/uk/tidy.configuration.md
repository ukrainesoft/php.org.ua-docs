---
navigation:
  - tidy.installation.md: « Встановлення
  - tidy.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - tidy.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації Tidy**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [tidy.default\_config](tidy.configuration.md#ini.tidy.default-config) | "" | **`INI_SYSTEM`** |  |
| [tidy.clean\_output](tidy.configuration.md#ini.tidy.clean-output) | "0" | **`INI_USER`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`tidy.default_config`string

Шлях за промовчанням до конфігураційного файлу Tidy.

`tidy.clean_output`bool

Вмикає/вимикає відновлення потоку виведення засобами Tidy.

**Увага**

Не слід вмикати `tidy.clean_output` у разі створення контенту, відмінного від html, такого як динамічні зображення.
