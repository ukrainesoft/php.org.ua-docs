---
navigation:
  - function.ibase-param-info.md: « ibase\_param\_info
  - function.ibase-prepare.md: ibase\_prepare »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_pconnect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_pconnect

(PHP 5, PHP 7 < 7.4.0)

ibase\_pconnect — Відкриває постійне з'єднання з базою даних InterBase

### Опис

```methodsynopsis
ibase_pconnect(    string $database = ?,    string $username = ?,    string $password = ?,    string $charset = ?,    int $buffers = ?,    int $dialect = ?,    string $role = ?,    int $sync = ?): resource
```

Відкриває постійне з'єднання із базою даних InterBase.

Принцип роботи \*\*ibase\_pconnect()\*\*очень похож на[ibase\_connect()](function.ibase-connect.md) з двома основними відмінностями.

По-перше, при підключенні функція спочатку спробує знайти (постійне) посилання, яке вже відкрито з такими самими параметрами. Якщо вона буде знайдена, замість відкриття нового з'єднання буде повернуто її ідентифікатор.

По-друге, з'єднання з сервером InterBase не буде закрито після закінчення скрипту. Натомість посилання залишиться відкритим для використання надалі ([ibase\_close()](function.ibase-close.md) не закриватиме посилання, встановлені **ibase\_pconnect()**). Тому цей тип посилання називається "постійним".

### Список параметрів

`database`

Аргумент`database` повинен бути допустимим шляхом до файлу бази даних на сервері, на якому він знаходиться. Якщо сервер не є локальним, він повинен мати префікс 'hostname:' (TCP/IP), '//hostname/' (NetBEUI) або 'hostname@' (IPX/SPX), залежно від протоколу підключення.

`username`

Ім'я користувача. Можна встановити за допомогою директиви php.ini `ibase.default_user`

`password`

Пароль для`username`. Можна встановити за допомогою директиви php.ini `ibase.default_password`

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

Повертає ідентифікатор посилання InterBase у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [ibase\_close()](function.ibase-close.md) \- Закриває з'єднання з базою даних InterBase
-   [ibase\_connect()](function.ibase-connect.md) \- Відкриває з'єднання з базою даних
