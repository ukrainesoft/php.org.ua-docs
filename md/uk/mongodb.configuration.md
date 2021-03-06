- [« Складання драйвера PHP MongoDB з вихідного коду](mongodb.installation.manual.md)
- [Предвизначені константи »](mongodb.constants.md)

- [PHP Manual](index.md)
- [Встановлення та налаштування](mongodb.setup.md)
- Налаштування під час виконання

# Налаштування під час виконання

Поведінка цих функцій залежить від установок `php.ini`.

| Ім'я За замовчуванням                                       | Місце зміни | Список змін |
| ----------------------------------------------------------- | ----------- | ----------- |
| [mongodb.debug](mongodb.configuration.md#ini.mongodb.debug) | ""          | PHP_INI_ALL |

**Опції налаштування mongodb**

Коротке пояснення конфігураційних директив.

`mongodb.debug` string
Цей параметр можна використовувати для увімкнення або вимкнення ведення
журналу налагодження на рівні трасування в драйвері (і libmongoc).

Вкажіть порожній рядок, ``0'`, ``off'', ``no'' або ``false”`, щоб
відключити ведення журналу.

Вкажіть `stderr` або `stdout`, щоб вести журнал в `stderr` або
`stdout`, відповідно.

Вкажіть ''1'', 'on', 'yes' або true для ведення журналу в новий
тимчасовий файл у системному тимчасовому каталозі за промовчанням (тобто.
[sys_get_temp_dir()](function.sys-get-temp-dir.md)).

Вкажіть будь-який інший рядок для ведення журналу в новий тимчасовий файл
цьому каталозі. Якщо каталог не може бути використаний, замість нього буде
використовуватись системний тимчасовий каталог за замовчуванням.

> **Примітка**:
>
> Зверніть увагу, що журнал налагодження може містити конфіденційну
> інформацію, таку як облікові дані на сервері MongoDB та повні
> документи, записані чи прочитані із сервера. Будь ласка,
> перегляньте всі журнали налагодження, перш ніж ділитися ними з іншими
> людьми.
