---
navigation:
  - function.ini-alter.md: « ini\_alter
  - function.ini-get.md: ini\_get »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: ini\_get\_all
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ini\_get\_all

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

ini\_get\_all — Отримує всі налаштування конфігурації

### Опис

```methodsynopsis
ini_get_all(?string $extension = null, bool $details = true): array|false
```

Повертає всі зареєстровані конфігураційні установки.

### Список параметрів

`extension`

Необов'язкове ім'я модуля. Якщо не \*\*`null`\*\*и не строка (string)`core`, функція повертає лише параметри.

`details`

Виводити детальні відомості про налаштування або лише поточні значення. За замовчуванням **`true`** (Виводити детальні відомості).

### Значення, що повертаються

Повертає асоціативний масив з іменами директив як ключі. Повертає **`false`** і викликає помилку рівня **`E_WARNING`**, якщо `extension` не існує.

Якщо `details`равен\*\*`true`\*\*(по умолчанию), в массиве будут содержаться`global_value`(значение настройки php.ini),`local_value`(например, заданное с помощью[ini\_set()](function.ini-set.md)или .htaccess) и`access`(уровень доступа).

Якщо `details`равен\*\*`false`\*\*, значенням масиву буде відповідне поточне налаштування.

Смотрите соответствующий[розділ керівництва](configuration.changes.modes.md), в якому наводиться опис рівнів доступу

> **Зауваження** :
> 
> Директива може мати кілька рівнів доступу, у цьому випадку `access` міститиме відповідну бітову маску.

### Приклади

**Приклад #1 Приклади використання **ini\_get\_all()****

```php
<?php
print_r(ini_get_all("pcre"));
print_r(ini_get_all());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [pcre.backtrack_limit] => Array
        (
            [global_value] => 100000
            [local_value] => 100000
            [access] => 7
        )

    [pcre.recursion_limit] => Array
        (
            [global_value] => 100000
            [local_value] => 100000
            [access] => 7
        )

)
Array
(
    [allow_call_time_pass_reference] => Array
        (
            [global_value] => 0
            [local_value] => 0
            [access] => 6
        )

    [allow_url_fopen] => Array
        (
            [global_value] => 1
            [local_value] => 1
            [access] => 4
        )

    ...

)
```

**Пример #2 Отключение`details`**

```php
<?php
print_r(ini_get_all("pcre", false)); // Добавлено в PHP 5.3.0
print_r(ini_get_all(null, false)); // Добавлено в PHP 5.3.0
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [pcre.backtrack_limit] => 100000
    [pcre.recursion_limit] => 100000
)
Array
(
    [allow_call_time_pass_reference] => 0
    [allow_url_fopen] => 1
    ...
)
```

### Примітки

> **Зауваження** :
> 
> **ini\_get\_all()** ігнорує опції типу "масив", такі як pdo.dsn.\*

### Дивіться також

-   [Як змінити налаштування конфігурації](configuration.changes.md)
-   [ini\_get()](function.ini-get.md) \- Отримує значення налаштування конфігурації
-   [ini\_restore()](function.ini-restore.md) \- Відновлює налаштування конфігурації.
-   [ini\_set()](function.ini-set.md) \- Встановлює налаштування конфігурації
-   [get\_loaded\_extensions()](function.get-loaded-extensions.md) \- Повертає масив імен усіх скомпілованих та завантажених модулів
-   [phpinfo()](function.phpinfo.md) \- Виводить інформацію про поточну конфігурацію PHP
-   [ReflectionExtension::getINIEntries()](reflectionextension.getinientries.md) \- Отримання ini-налаштувань модуля
