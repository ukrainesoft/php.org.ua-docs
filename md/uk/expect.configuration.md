---
navigation:
  - expect.installation.md: « Встановлення
  - expect.resources.md: Типи ресурсів »
  - index.md: PHP Manual
  - expect.setup.md: Встановлення та налаштування
title: Налаштування під час виконання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

Для налаштування модуля використовуйте наведені нижче опції [конфігураційного файлу](configuration.file.md)php.ini.

**Опції налаштування Expect**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [expect.timeout](expect.configuration.md#ini.expect.timeout) | "10" | **`INI_ALL`** |  |
| [expect.loguser](expect.configuration.md#ini.expect.loguser) | "1" | **`INI_ALL`** |  |
| [expect.logfile](expect.configuration.md#ini.expect.logfile) | "" | **`INI_ALL`** |  |
| [expect.match\_max](expect.configuration.md#ini.expect.match-max) | "" | **`INI_ALL`** |  |

Додаткова інформація та опис режимів INI\_\* дано у розділі «[Місця встановлення параметрів конфігурації](configuration.changes.modes.md)».

Коротке пояснення конфігураційних директив.

`expect.timeout`int

Максимальний час очікування даних під час використання функції [expect\_expectl()](function.expect-expectl.md)

Значення "-1" задає вічне очікування.

> **Зауваження** :
> 
> Значення "0" означає, що функція [expect\_expectl()](function.expect-expectl.md)завершится сразу.

`expect.loguser`bool

Визначає, чи породжений процес робитиме висновок у потік stdout. Так як інтерактивні програми зазвичай дублюють введення користувача, зазвичай потрібно вирішувати цю опцію, щоб взаємодія була усвідомленою.

`expect.logfile`string

Ім'я файлу, куди писатиметься висновок породженого процесу. Якщо файл не існує, його буде створено.

> **Зауваження** :
> 
> Якщо цій опції надано якесь не порожнє значення, то висновок писатиметься у файл незалежно від налаштування [expect.loguser](expect.configuration.md#ini.expect.loguser)

`expect.match_max`int

Змінює розмір буфера (за замовчуванням 2000 байт), який використовується для пошуку символу зірочки в шаблонах.
