---
navigation:
  - xhprof.installation.md: « Встановлення
  - xhprof.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - xhprof.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Xhprof**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [xhprof.output\_dir](xhprof.configuration.md#ini.xhprof.output-dir) | "" | **`INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`xhprof.output_dir`string

Директорія, що використовується реалізацією інтерфейсу XHProf Runs за умовчанням (клас XHProf Runs\_Default) для збереження результатів профілювання.
