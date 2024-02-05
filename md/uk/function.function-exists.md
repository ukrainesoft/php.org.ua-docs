---
navigation:
  - function.func-num-args.md: « func\_num\_args
  - function.get-defined-functions.md: get\_defined\_functions »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: function\_exists
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# function\_exists

(PHP 4, PHP 5, PHP 7, PHP 8)

function\_exists - Повертає \*\*`true`\*\*якщо зазначена функція визначена

### Опис

```methodsynopsis
function_exists(string $function): bool
```

Перевіряє, чи є в списку певних функцій, як вбудованих (внутрішніх), так і функцій користувача, функція `function`

### Список параметрів

`function`

Ім'я функції у вигляді рядка.

### Значення, що повертаються

Повертає **`true`**, якщо `function` існує і є функцією, інакше повертається **`false`**

> **Зауваження** :
> 
> Ця функція повертає **`false`** для мовних конструкцій, таких як [include\_once](function.include-once.md) або [echo](function.echo.md)

### Приклади

**Приклад #1 Приклад використання** function\_exists()\*\*\*\*

```php
<?php
if (function_exists('imap_open')) {
    echo "Функции IMAP доступны.<br />\n";
} else {
    echo "Функции IMAP недоступны.<br />\n";
}
?>
```

### Примітки

> **Зауваження** :
> 
> Зверніть увагу, що назва функції може бути присутня, навіть якщо саму функцію неможливо використовувати через налаштування конфігурації або опції компіляції (наприклад, як для функцій [image](ref.image.md)

### Дивіться також

-   [method\_exists()](function.method-exists.md) \- Перевіряє, чи існує метод у даному класі
-   [is\_callable()](function.is-callable.md) \- Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [get\_defined\_functions()](function.get-defined-functions.md) \- Повертає масив усіх певних функцій
-   [class\_exists()](function.class-exists.md) \- Перевіряє, чи був оголошений клас
-   [extension\_loaded()](function.extension-loaded.md) \- Визначає, чи завантажений модуль
