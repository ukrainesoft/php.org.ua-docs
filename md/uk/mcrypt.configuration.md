---
navigation:
  - mcrypt.installation.md: « Встановлення
  - mcrypt.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - mcrypt.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Mcrypt**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mcrypt.algorithms\_dir](mcrypt.configuration.md#ini.mcrypt.algorithms-dir) | **`null`** | **`INI_ALL`** |  |
| [mcrypt.modes\_dir](mcrypt.configuration.md#ini.mcrypt.modes-dir) | **`null`** | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`mcrypt.algorithms_dir`string

Директорія, яка містить алгоритми. За замовчуванням відповідає директоріям, скомпільованим разом з libmcrypt, зазвичай */usr/local/lib/libmcrypt*Смотрите[mcrypt\_list\_algorithms()](function.mcrypt-list-algorithms.md) для додаткової інформації.

`mcrypt.modes_dir`string

Директорія з режимами. За замовчуванням відповідає директоріям, скомпільованим разом з libmcrypt, зазвичай */usr/local/lib/libmcrypt*Смотрите[mcrypt\_list\_modes()](function.mcrypt-list-modes.md) для додаткової інформації.
