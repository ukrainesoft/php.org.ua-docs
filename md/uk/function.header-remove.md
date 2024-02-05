---
navigation:
  - function.header-register-callback.md: « header\_register\_callback
  - function.header.md: header »
  - index.md: PHP Manual
  - ref.network.md: Мережеві функції
title: header\_remove
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# header\_remove

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

header\_remove — Видалення раніше встановлених заголовків

### Опис

```methodsynopsis
header_remove(?string $name = null): void
```

Видаляє попередньо встановлений функцією [header()](function.header.md)HTTP-заголовок.

### Список параметрів

`name`

Ім'я заголовка, що видаляється. Якщо \*\*`null`\*\*видаляються всі раніше встановлені заголовки.

> **Зауваження**: Це незалежний параметр.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `name` тепер допускає значення null. |

### Приклади

**Приклад #1 Знищення певного заголовка.**

```php
<?php
header("X-Foo: Bar");
header("X-Bar: Baz");
header_remove("X-Foo");
?>
```

Висновок наведеного прикладу буде схожим на:

```
X-Bar: Baz
```

**Приклад #2 Знищення всіх встановлених раніше заголовків.**

```php
<?php
header("X-Foo: Bar");
header("X-Bar: Baz");
header_remove();
?>
```

Висновок наведеного прикладу буде схожим на:

### Примітки

**Застереження**

Ця функція видалить *Усе* заголовки, встановлені за допомогою PHP, включаючи cookies, сесію та заголовки `X-Powered-By`

> **Зауваження** :
> 
> Доступ до заголовків та їх висновок здійснюватиметься лише у випадку, якщо у SAPI є їх підтримка.

### Дивіться також

-   [header()](function.header.md) \- Надсилає необроблений (сирий) HTTP-заголовок
-   [headers\_sent()](function.headers-sent.md) \- Перевіряє, чи були надіслані заголовки
