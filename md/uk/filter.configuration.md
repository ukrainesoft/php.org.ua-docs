Налаштування під час виконання

-   [« Установка](filter.installation.md)
    
-   [Типи ресурсів »](filter.resources.md)
    
-   [PHP Manual](index.md)
    
-   [Встановлення та налаштування](filter.setup.md)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації Filter**

| Имя | По умолчанию | Место изменения | Список изменений |
| --- | --- | --- | --- |
| [filter.default](filter.configuration.html#ini.filter.default) | "unsaferaw" | PHPINIPERDIR | Параметр застарів, починаючи з PHP 8.1.0. |
| [filter.defaultflags](filter.configuration.html#ini.filter.default-flags) | NULL | PHPINIPERDIR |  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.md)

Коротке пояснення конфігураційних директив.

`filter.default` string

Фільтрує всі дані [GET](reserved.variables.get.md) [POST](reserved.variables.post.md) [COOKIE](reserved.variables.cookies.md) [REQUEST](reserved.variables.request.md) і [SERVER](reserved.variables.server.md) цим фільтром. Вихідні дані можуть бути отримані за допомогою [filterinput()](function.filter-input.html)

Приймає ім'я вказаного фільтра як значення за промовчанням. Імена фільтрів можна знайти в [списку існуючих фільтрів](filter.filters.md)

> **Зауваження**
> 
> Будьте уважні з прапорами за промовчанням для стандартних фільтрів. Слід явно встановлювати їх у значення, яке вам необхідно. Наприклад, для установки фільтра за умовчанням, який буде працювати точнісінько аналогічно функції [htmlspecialchars()](function.htmlspecialchars.md)Вам потрібно встановити прапори за промовчанням в 0 так, як показано нижче.
> 
> **Приклад #1 Налаштування стандартного фільтра для роботи аналогічно функції htmlspecialchars**
> 
> ```php
> filter.default = full_special_chars
> filter.default_flags = 0
> ```

`filter.default_flags` int

Прапори за промовчанням, які застосовуються, коли встановлено стандартний фільтр. За замовчуванням встановлено **`FILTER_FLAG_NO_ENCODE_QUOTES`** з метою збереження зворотної сумісності. Дивіться [список існуючих прапорів](filter.filters.flags.md) для ознайомлення зі списком усіх імен прапорів.