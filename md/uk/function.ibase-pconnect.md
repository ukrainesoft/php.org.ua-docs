Відкриває постійне з'єднання з базою даних InterBase

-   [« ibase\_param\_info](function.ibase-param-info.html)
    
-   [ibase\_prepare »](function.ibase-prepare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Відкриває постійне з'єднання з базою даних InterBase
    

# ibasepconnect

(PHP 5, PHP 7 < 7.4.0)

ibasepconnect — Відкриває постійне з'єднання з базою даних InterBase

### Опис

```methodsynopsis
ibase_pconnect(    string $database = ?,    string $username = ?,    string $password = ?,    string $charset = ?,    int $buffers = ?,    int $dialect = ?,    string $role = ?,    int $sync = ?): resource
```

Відкриває постійне з'єднання із базою даних InterBase.

Принцип роботи **ibasepconnect()** дуже схожий [ibase\_connect()](function.ibase-connect.html) з двома основними відмінностями.

По-перше, при підключенні функція спочатку спробує знайти (постійне) посилання, яке вже відкрито з такими самими параметрами. Якщо вона буде знайдена, замість відкриття нового з'єднання буде повернуто її ідентифікатор.

По-друге, з'єднання з сервером InterBase не буде закрито після закінчення скрипту. Натомість посилання залишиться відкритим для використання надалі ([ibase\_close()](function.ibase-close.html) не закриватиме посилання, встановлені **ibasepconnect()**). Тому цей тип посилання називається "постійним".

### Список параметрів

`database`

Аргумент `database` повинен бути допустимим шляхом до файлу бази даних на сервері, де він знаходиться. Якщо сервер не є локальним, він повинен мати префікс 'hostname:' (TCP/IP), '//hostname/' (NetBEUI) або 'hostname@' (IPX/SPX), залежно від протоколу підключення.

`username`

Ім'я користувача. Можна встановити за допомогою директиви php.ini `ibase.default_user`

`password`

Пароль для `username`. Можна встановити за допомогою директиви php.ini `ibase.default_password`

`charset`

`charset` - Набір стандартних символів для бази даних.

`buffers`

`buffers` - кількість буферів бази даних, що виділяються для кеша за сервера. Якщо значення дорівнює 0 або опущено, сервер вибирає значення за промовчанням.

`dialect`

`dialect` вибирає діалект SQL за замовчуванням для будь-якого виразу, що виконується у з'єднанні, і за замовчуванням вибирає найвищий діалект, який підтримує клієнтські бібліотеки. Працює лише з InterBase 6 і вище.

`role`

Працює лише з InterBase 5 і вище.

`sync`

### Значення, що повертаються

Повертає ідентифікатор посилання InterBase у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [ibase\_close()](function.ibase-close.html) - Закриває з'єднання з базою даних InterBase
-   [ibase\_connect()](function.ibase-connect.html) - Відкриває з'єднання з базою даних