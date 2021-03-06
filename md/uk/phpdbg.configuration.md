- [« Встановлення та налаштування](phpdbg.setup.md)
- [Предвизначені константи »](phpdbg.constants.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](phpdbg.setup.md)
- Налаштування під час виконання

## Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                  | Місце зміни | Список змін |
| ------------------------------------------------------ | ----------- | ----------- |
| [phpdbg.eol](phpdbg.configuration.md#ini.phpdbg.eol)   | 2           | PHP_INI_ALL | Видалено з PHP 8.1.0
| [phpdbg.path](phpdbg.configuration.md#ini.phpdbg.path) |             | 6           | Видалено з PHP 8.1.0

**phpdbg Опції налаштування**

Коротке пояснення конфігураційних директив.

`phpdbg.eol` [mixed](language.types.declarations.md#language.types.declarations.mixed)
Тип закінчення рядка, який використовується для виведення. Для встановлення значення
необхідно використовувати один із псевдонімів рядків.

| int Значення | string Псевдонім             |
| ------------ | ---------------------------- |
| 0            | 'CRLF', 'crlf', 'DOS', 'dos' |                            
| 1            | LF, lf, UNIX, unix           |
| 2            | 'CR', 'cr', 'MAC', 'mac'     |

`phpdbg.path` string
