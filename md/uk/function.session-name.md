---
navigation:
  - function.session-module-name.md: « sessionmodulename
  - function.session-regenerate-id.md: sessionregenerateid »
  - index.md: PHP Manual
  - ref.session.md: Функції для роботи із сесіями
title: sessionname
---
# sessionname

(PHP 4, PHP 5, PHP 7, PHP 8)

sessionname — Отримати або встановити ім'я поточної сесії

### Опис

```methodsynopsis
session_name(?string $name = null): string|false
```

**sessionname()** повертає ім'я поточної сесії. Якщо встановлено параметр `name` **sessionname()** оновить ім'я сесії та поверне *старе* ім'я сесії.

Якщо нове ім'я сесії (`name`) надано, **sessionname()** змінює cookie HTTP (і виводить вміст при включеній опції `session.transid`). Коли cookie HTTP надіслано, **sessionname()** викликає помилку . **sessionname()** необхідно викликати до [sessionstart()](function.session-start.md) для правильної роботи сесії

Ім'я сесії скидаються на значення за умовчанням, що зберігається в `session.name` під час запуску запиту. Таким чином, вам потрібно викликати **sessionname()** для кожного запиту (і до [sessionstart()](function.session-start.md)

### Список параметрів

`name`

Ім'я сесії посилається на ім'я сесії, яке використовується в cookie та URL (наприклад, `PHPSESSID` ). Воно має містити лише буквено-цифрові символи, і має бути коротким і зрозумілими (наприклад, для користувачів із увімкненим попередженням cookie). Якщо встановлено параметр `name` і він не дорівнює **`null`**, ім'я поточної сесії зміниться нею.

**Увага**

Ім'я сесії не може складатися тільки з цифр, принаймні одна буква має бути присутньою. Інакше щоразу генеруватиметься новий ідентифікатор.

### Значення, що повертаються

Повертає ім'я поточної сесії. Якщо встановлено параметр `name`, ім'я поточної сесії зміниться і буде повернуто *старе* або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `module` тепер може бути **`null`** |
|  | **sessionname()** перевіряє статус сесії, раніше вона перевіряла лише статус cookie. Тому стара версія **sessionname()** дозволяла викликати **sessionname()** після [sessionstart()](function.session-start.md), що могло призвести до збою PHP та неправильної поведінки. |

### Приклади

**Приклад #1 Приклад використання **sessionname()****

```php
<?php

/* устанавливает имя сессии равным WebsiteID */

$previous_name = session_name("WebsiteID");

echo "Предыдущее имя сессии: $previous_name<br />";
?>
```

### Дивіться також

-   Параметр конфігурації [session.name](session.configuration.md#ini.session.name)
