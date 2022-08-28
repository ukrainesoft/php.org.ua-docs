Налаштування під час виконання

-   [« Установка](filter.installation.html)
    
-   [Типы ресурсов »](filter.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Установка и настройка](filter.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Параметри конфігурації Filter**

| Имя                                                                         | По умолчанию | Место изменения | Список изменений                          |
|-----------------------------------------------------------------------------|--------------|-----------------|-------------------------------------------|
| [filter.default](filter.configuration.html#ini.filter.default)              | "unsaferaw"  | PHPINIPERDIR    | Параметр застарів, починаючи з PHP 8.1.0. |
| [filter.default\_flags](filter.configuration.html#ini.filter.default-flags) | NULL         | PHPINIPERDIR    |                                           |

Для детального опису констант PHPINI, зверніться до розділу [Где могут быть установлены параметры конфигурации](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`filter.default` string

Фільтрує всі дані [$\_GET](reserved.variables.get.html) [$\_POST](reserved.variables.post.html) [$\_COOKIE](reserved.variables.cookies.html) [$\_REQUEST](reserved.variables.request.html) і [$\_SERVER](reserved.variables.server.html) цим фільтром. Вихідні дані можуть бути отримані за допомогою [filter\_input()](function.filter-input.html)

Приймає ім'я вказаного фільтра як значення за промовчанням. Імена фільтрів можна знайти в [списке существующих фильтров](filter.filters.html)

> **Зауваження**
> 
> Будьте уважні з прапорами за промовчанням для стандартних фільтрів. Слід явно встановлювати їх у значення, яке вам необхідно. Наприклад, для установки фільтра за умовчанням, який буде працювати точнісінько аналогічно функції [htmlspecialchars()](function.htmlspecialchars.html)Вам потрібно встановити прапори за промовчанням в 0 так, як показано нижче.
> 
> **Приклад #1 Налаштування стандартного фільтра для роботи аналогічно функції htmlspecialchars**
> 
> ```php
> filter.default = full_special_chars
> filter.default_flags = 0
> ```

`filter.default_flags` int

Прапори за промовчанням, які застосовуються, коли встановлено стандартний фільтр. За замовчуванням встановлено **`FILTER_FLAG_NO_ENCODE_QUOTES`** з метою збереження зворотної сумісності. Дивіться [список существующих флагов](filter.filters.flags.html) для ознайомлення зі списком усіх імен прапорів.