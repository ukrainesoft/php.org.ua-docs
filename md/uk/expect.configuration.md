Налаштування під час виконання

-   [« Установка](expect.installation.md)
    
-   [Типи ресурсів »](expect.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](expect.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

Для налаштування модуля використовуйте наведені нижче опції [конфигурационного файла](configuration.file.md) php.ini.

**Опції налаштування Expect**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [expect.timeout](expect.configuration.html#ini.expect.timeout) | "10" | PHPINIALL |  |
| [expect.loguser](expect.configuration.html#ini.expect.loguser) | "1" | PHPINIALL |  |
| [expect.logfile](expect.configuration.html#ini.expect.logfile) | "" | PHPINIALL |  |
| [expect.matchmax](expect.configuration.html#ini.expect.match-max) | "" | PHPINIALL |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`expect.timeout` int

Максимальний час очікування даних під час використання функції [expectexpectl()](function.expect-expectl.html)

Значення "-1" задає вічне очікування.

> **Зауваження**
> 
> Значення "0" означає, що функція [expectexpectl()](function.expect-expectl.html) завершиться одразу.

`expect.loguser` bool

Визначає, чи породжений процес робитиме висновок у потік stdout. Так як інтерактивні програми зазвичай дублюють введення користувача, зазвичай потрібно вирішувати цю опцію, щоб взаємодія була усвідомленою.

`expect.logfile` string

Ім'я файлу, куди писатиметься висновок породженого процесу. Якщо файл не існує, його буде створено.

> **Зауваження**
> 
> Якщо цій опції надано якесь не порожнє значення, то висновок писатиметься у файл незалежно від налаштування [expect.loguser](expect.configuration.html#ini.expect.loguser)

`expect.match_max` int

Змінює розмір буфера (за замовчуванням 2000 байт), який використовується для пошуку символу зірочки в шаблонах.