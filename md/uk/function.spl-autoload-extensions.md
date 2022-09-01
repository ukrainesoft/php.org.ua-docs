---
navigation:
  - function.spl-autoload-call.html: « splautoloadcall
  - function.spl-autoload-functions.html: splautoloadfunctions »
  - index.html: PHP Manual
  - ref.spl.html: Функції SPL
title: splautoloadextensions
---
# splautoloadextensions

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoloadextensions — Реєстрація та виведення розширень файлів для splautoload

### Опис

```methodsynopsis
spl_autoload_extensions(?string $file_extensions = null): string
```

Ця функція може задавати розширення файлів, у яких callback-функція [autoload()](function.autoload.html) шукатиме класи та інтерфейси . [splautoload()](function.spl-autoload.md) буде викликати функцію autoload та передавати йому ці розширення. Також ця функція може виводити вже зареєстровані розширення файлів.

> **Зауваження**: Між розширеними файлами не повинно бути пробілів.

### Список параметрів

`file_extensions`

Якщо **`null`**, функція просто виведе список зареєстрованих на даний момент розширень, перерахованих через кому. Щоб змінити цей список, необхідно викликати функцію, передавши їй рядок з розширеннями, також переліченими через кому.

### Значення, що повертаються

Список перелічених через кому розширень файлів для функції [splautoload()](function.spl-autoload.md)

### список змін

| Версия | Описание |
| --- | --- |
|  | `file_extensions` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **splautoloadextensions()****

```php
<?php
spl_autoload_extensions(".php,.inc");
?>
```
