---
navigation:
  - var.installation.md: « Установка
  - var.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - var.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації змінних**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [unserializecallbackfunc](var.configuration.md#ini.unserialize-callback-func) | **`null`** | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`unserialize_callback_func` string

Якщо в процесі десеріалізації через [unserialize()](function.unserialize.md) буде виявлено невизначений клас, то буде викликана певна callback-функція. Якщо зазначена callback-функція не визначена чи може визначити відсутній клас, буде виведено попередження.

Дивіться також [unserialize()](function.unserialize.md) та розділ [автозавантаження об'єктів](language.oop5.autoload.md)
