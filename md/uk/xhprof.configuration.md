---
navigation:
  - xhprof.installation.md: « Установка
  - xhprof.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - xhprof.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Xhprof**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [xhprof.outputdir](xhprof.configuration.html#ini.xhprof.output-dir) | "" | **`PHP_INI_ALL`** |  |

Коротке пояснення конфігураційних директив.

`xhprof.output_dir` string

Директорія, що використовується реалізацією інтерфейсу XHProf Runs за умовчанням (клас XHProf RunsDefault) для збереження результатів профілювання.
