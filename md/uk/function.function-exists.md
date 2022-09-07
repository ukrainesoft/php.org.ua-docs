---
navigation:
  - function.func-num-args.md: « funcnumargs
  - function.get-defined-functions.md: getdefinedfunctions »
  - index.md: PHP Manual
  - ref.funchand.md: Функции управления функциями
title: functionexists
---
# functionexists

(PHP 4, PHP 5, PHP 7, PHP 8)

functionexists - Повертає \*\*`true`\*\*якщо зазначена функція визначена

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

> **Зауваження**
> 
> Ця функція повертає **`false`** для мовних конструкцій, таких як [includeonce](function.include-once.md) або [echo](function.echo.md)

### Приклади

**Приклад #1 Приклад використання **functionexists()****

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

> **Зауваження**
> 
> Зверніть увагу, що назва функції може бути присутня, навіть якщо саму функцію неможливо використовувати через налаштування конфігурації або опції компіляції (наприклад, як для функцій [image](ref.image.md)

### Дивіться також

-   [methodexists()](function.method-exists.md) - Перевіряє, чи існує метод у даному класі
-   [ісcallable()](function.is-callable.md) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [getdefinedfunctions()](function.get-defined-functions.md) - Повертає масив усіх певних функцій
-   [classexists()](function.class-exists.md) - Перевіряє, чи був оголошений клас
-   [extensionloaded()](function.extension-loaded.md) - Визначає, чи завантажений модуль
