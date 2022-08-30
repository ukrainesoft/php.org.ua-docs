Повертає true, якщо вказана функція визначена

-   [« funcnumargs](function.func-num-args.html)
    
-   [getdefinedfunctions »](function.get-defined-functions.html)
    
-   [PHP Manual](index.html)
    
-   [Функции управления функциями](ref.funchand.html)
    
-   Повертає true, якщо вказана функція визначена
    

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
> Ця функція повертає **`false`** для мовних конструкцій, таких як [includeonce](function.include-once.html) або [echo](function.echo.html)

### Приклади

**Приклад #1 Приклад використання **functionexists()****

```php
<?php
if (function_exists('imap_open')) {
    echo "Функции IMAP доступны.<br />\n";
} else {
    echo "Функции IMAP недоступны.<br />\n";
}
?>
```

### Примітки

> **Зауваження**
> 
> Зверніть увагу, що назва функції може бути присутня, навіть якщо саму функцію неможливо використовувати через налаштування конфігурації або опції компіляції (наприклад, як для функцій [image](ref.image.html)

### Дивіться також

-   [methodexists()](function.method-exists.html) - Перевіряє, чи існує метод у даному класі
-   [ісcallable()](function.is-callable.html) - Перевіряє, що значення може бути викликане як функція у поточній області видимості
-   [getdefinedfunctions()](function.get-defined-functions.html) - Повертає масив усіх певних функцій
-   [classexists()](function.class-exists.html) - Перевіряє, чи був оголошений клас
-   [extensionloaded()](function.extension-loaded.html) - Визначає, чи завантажений модуль