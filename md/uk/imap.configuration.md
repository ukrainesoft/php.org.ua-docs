- [« Установка](imap.installation.md)
- [Типи ресурсів»](imap.resources.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](imap.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                                          | Місце зміни | Список змін    |
| ------------------------------------------------------------------------------ | ----------- | -------------- |
| [imap.enable_insecure_rsh](imap.configuration.md#ini.imap.enable-insecure-rsh) | "0"         | PHP_INI_SYSTEM | Доступно з PHP 7.1.25, 7.2.13 та 7.3.0. Раніше був неявно увімкнений.

**Опції налаштування IMAP**

Для детального опису констант PHP_INI\_\*, зверніться до розділу [Де
можуть бути встановлені параметри конфігурації](configuration.changes.modes.md).

Коротке пояснення конфігураційних директив.

`imap.enable_insecure_rsh` bool
Встановлення з'єднання з сервером може запустити команду **rsh** або
**ssh**, якщо ця опція не відключена в `php.ini`.

**Увага**
Ні PHP ні бібліотека IMAP не фільтрують імена поштових скриньок при
передачі їх командам **rsh** або **ssh**. Таким чином, передача
неперевірених даних у цю функцію, без відключення цієї опції в
`php.ini` *небезпечна*.
