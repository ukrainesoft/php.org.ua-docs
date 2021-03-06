- [« Установка](yaconf.installation.md)
- [Типи ресурсів»](yaconf.resources.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](yaconf.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                                | Місце зміни | Список змін    |
| -------------------------------------------------------------------- | ----------- | -------------- |
| [yaconf.check_delay](yaconf.configuration.md#ini.yaconf.check-delay) | 300         | PHP_INI_SYSTEM |
| [yaconf.directory](yaconf.configuration.md#ini.yaconf.directory)     | /tmp/conf/  | PHP_INI_SYSTEM |

**Опції налаштування Yaconf**

Коротке пояснення конфігураційних директив.

`yaconf.check_delay` int
Інтервал часу, протягом якого Yaconf визначатиме зміну
файлу ini (за часом зміни директорії), якщо встановлено нуль,
потрібний перезапуск PHP для перезавантаження конфігурацій.

`yaconf.directory` string
Шлях до директорії, де знаходяться всі файли конфігурації INI.
