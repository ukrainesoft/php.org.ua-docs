Налаштування під час виконання

-   [« Установка](ibase.installation.html)
    
-   [Типи ресурсів »](ibase.resources.html)
    
-   [PHP Manual](index.html)
    
-   [Встановлення та налаштування](ibase.setup.html)
    
-   Налаштування під час виконання
    

## Налаштування під час виконання

Поведінка цих функцій залежить від установок у php.ini.

**Конфігураційні опції InterBase**

| Имя                                                                          | По умолчанию        | Место изменения | Список изменений |
|------------------------------------------------------------------------------|---------------------|-----------------|------------------|
| [ibase.allowpersistent](ibase.configuration.html#ini.ibase.allow-persistent) | "1"                 | PHPINISYSTEM    |                  |
| [ibase.maxpersistent](ibase.configuration.html#ini.ibase.max-persistent)     | "-1"                | PHPINISYSTEM    |                  |
| [ibase.maxlinks](ibase.configuration.html#ini.ibase.max-links)               | "-1"                | PHPINISYSTEM    |                  |
| [ibase.defaultдб](ibase.configuration.html#ini.ibase.default-db)             | NULL                | PHPINISYSTEM    |                  |
| [ibase.defaultuser](ibase.configuration.html#ini.ibase.default-user)         | NULL                | PHPINIALL       |                  |
| [ibase.defaultpassword](ibase.configuration.html#ini.ibase.default-password) | NULL                | PHPINIALL       |                  |
| [ibase.defaultcharset](ibase.configuration.html#ini.ibase.default-charset)   | NULL                | PHPINIALL       |                  |
| [ibase.timestampformat](ibase.configuration.html#ini.ibase.timestampformat)  | "%Y-%m-%d %H:%M:%S" | PHPINIALL       |                  |
| [ibase.dateformat](ibase.configuration.html#ini.ibase.dateformat)            | "%Y-%m-%d"          | PHPINIALL       |                  |
| [ibase.timeformat](ibase.configuration.html#ini.ibase.timeformat)            | "%H:%M:%S"          | PHPINIALL       |                  |

Для детального опису констант PHPINI, зверніться до розділу [Де можуть бути встановлені параметри конфігурації](configuration.changes.modes.html)

Коротке пояснення конфігураційних директив.

`ibase.allow_persistent` bool

Чи дозволено використовувати [постійні з'єднання](features.persistent-connections.html) до Firebird/InterBase.

`ibase.max_persistent` int

Максимальна кількість постійних з'єднань для процесу. Якщо це обмеження буде перевищено, то функція ibasepconnect() повертатиме непостійні з'єднання.

`ibase.max_links` int

Максимальна кількість з'єднань із Firebird/InterBase на процес, включаючи постійні.

`ibase.default_db` string

База даних за промовчанням. Якщо викликати ibaseпconnect() без вказівки імені бази даних, буде використано це значення. Якщо цей параметр встановлений і увімкнений безпечний режим SQL, будуть дозволені з'єднання тільки з цією базою.

`ibase.default_user` string

Ім'я користувача за промовчанням.

`ibase.default_password` string

Пароль за замовчуванням.

`ibase.default_charset` string

Кодування за промовчанням.

`ibase.timestampformat` string

`ibase.dateformat` string

`ibase.timeformat` string

Ці директиви використовуються для встановлення формату дати та часу. Дані формати будуть використовуватися як для отримання результуючого набору, що містить поля відповідних типів, так і при зв'язуванні значень з параметрами запиту.