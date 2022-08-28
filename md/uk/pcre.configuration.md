Налаштування під час виконання

-   [« Установка](pcre.installation.html)
    
-   [Типы ресурсов »](pcre.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](pcre.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Опції конфігурації PCRE**

| Имя                                                                       | По умолчанию | Место изменения | Список изменений |
|---------------------------------------------------------------------------|--------------|-----------------|------------------|
| [pcre.backtrack\_limit](pcre.configuration.html#ini.pcre.backtrack-limit) | "1000000"    | PHPINIALL       |                  |
| [pcre.recursion\_limit](pcre.configuration.html#ini.pcre.recursion-limit) | "100000"     | PHPINIALL       |                  |
| [pcre.jit](pcre.configuration.html#ini.pcre.jit)                          | "1"          | PHPINIALL       |                  |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`pcre.backtrack_limit` int

Ліміт зворотних посилань PCRE. Для PHP < 5.3.7 значення за промовчанням 100000.

`pcre.recursion_limit` int

Ліміт на рекурсію. Не забувайте про те, що якщо ви встановите досить високе значення, PCRE може перевищити розмір стека (встановлений операційною системою) і врешті-решт викликає падіння PHP.

`pcre.jit` bool

Чи використовуватиметься JIT-компіляція PCRE.