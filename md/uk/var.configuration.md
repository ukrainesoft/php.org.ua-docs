---
navigation:
  - var.installation.md: « Встановлення
  - var.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - var.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації змінних**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [unserialize\_callback\_func](var.configuration.md#ini.unserialize-callback-func) | **`null`** | **`INI_ALL`** |  |
| [unserialize\_max\_depth](var.configuration.md#ini.unserialize-max-depth) | "4096" | **`INI_ALL`** | Доступно з PHP 7.4.0. |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`unserialize_callback_func`string

Якщо в процесі десеріалізації через [unserialize()](function.unserialize.md) буде виявлено невизначений клас, то буде викликана певна callback-функція. Якщо зазначена callback-функція не визначена чи може визначити відсутній клас, буде виведено попередження.

Смотрите также[unserialize()](function.unserialize.md) та розділ [автозавантаження класів](language.oop5.autoload.md)

`unserialize_max_depth`int

Максимальна глибина структур дозволена при десеріалізації при використанні функції [unserialize()](function.unserialize.md) і призначена для запобігання переповненню стека. Це можна вимкнути, встановивши `unserialize_max_depth=0`

Смотрите также[unserialize()](function.unserialize.md) та розділ [автозавантаження класів](language.oop5.autoload.md)
