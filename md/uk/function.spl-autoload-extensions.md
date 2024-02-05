---
navigation:
  - function.spl-autoload-call.md: « spl\_autoload\_call
  - function.spl-autoload-functions.md: spl\_autoload\_functions »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: spl\_autoload\_extensions
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# spl\_autoload\_extensions

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

spl\_autoload\_extensions — Реєстрація та виведення розширень файлів для spl\_autoload

### Опис

```methodsynopsis
spl_autoload_extensions(?string $file_extensions = null): string
```

Ця функція може задавати розширення файлів, у яких callback-функція [\_\_autoload()](function.autoload.md) шукатиме класи та інтерфейси . [spl\_autoload()](function.spl-autoload.md) буде викликати функцію \_\_autoload та передавати йому ці розширення. Також ця функція може виводити вже зареєстровані розширення файлів.

> **Зауваження**: Між розширеними файлами не повинно бути пробілів.

### Список параметрів

`file_extensions`

Якщо **`null`**, функція просто виведе список зареєстрованих на даний момент розширень, перерахованих через кому. Щоб змінити цей список, необхідно викликати функцію, передавши їй рядок з розширеннями, також переліченими через кому.

### Значення, що повертаються

Список перелічених через кому розширень файлів для функції [spl\_autoload()](function.spl-autoload.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `file_extensions` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання** spl\_autoload\_extensions()\*\*\*\*

```php
<?php
spl_autoload_extensions(".php,.inc");
?>
```
