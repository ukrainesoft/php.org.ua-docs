---
navigation:
  - mcrypt.installation.md: « Установка
  - mcrypt.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - mcrypt.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції налаштування Mcrypt**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [mcrypt.algorithmsdir](mcrypt.configuration.md#ini.mcrypt.algorithms-dir) | **`null`** | PHPINIALL |  |
| [mcrypt.modesdir](mcrypt.configuration.md#ini.mcrypt.modes-dir) | **`null`** | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`mcrypt.algorithms_dir` string

Директорія, яка містить алгоритми. За замовчуванням відповідає директоріям, скомпільованим разом з libmcrypt, зазвичай */usr/local/lib/libmcrypt*. Дивіться [mcryptlistalgorithms()](function.mcrypt-list-algorithms.md) для додаткової інформації.

`mcrypt.modes_dir` string

Директорія з режимами. За замовчуванням відповідає директоріям, скомпільованим разом з libmcrypt, зазвичай */usr/local/lib/libmcrypt*. Дивіться [mcryptlistmodes()](function.mcrypt-list-modes.md) для додаткової інформації.
