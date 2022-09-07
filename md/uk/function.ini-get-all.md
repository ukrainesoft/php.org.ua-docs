---
navigation:
  - function.ini-alter.md: « inialter
  - function.ini-get.md: iniget »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: inigetall
---
# inigetall

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

inigetall — Отримує всі налаштування конфігурації

### Опис

```methodsynopsis
ini_get_all(?string $extension = null, bool $details = true): array|false
```

Повертає всі зареєстровані конфігураційні установки.

### Список параметрів

`extension`

Необов'язкове ім'я модуля. Якщо не **`null`** і не рядок (string) `core`, функція повертає лише параметри.

`details`

Виводити детальні відомості про налаштування або лише поточні значення. За замовчуванням **`true`** (Виводити детальні відомості).

### Значення, що повертаються

Повертає асоціативний масив з іменами директив як ключі. Повертає **`false`** і викликає помилку рівня **`E_WARNING`**, якщо `extension` не існує.

Якщо `details` дорівнює **`true`** (за замовчуванням), у масиві будуть утримуватися `global_value` (значення налаштування php.ini), `local_value` (наприклад, задане за допомогою [iniset()](function.ini-set.md) або .htaccess) та `access` (рівень доступу).

Якщо `details` дорівнює **`false`**, значенням масиву буде відповідне поточне налаштування.

Дивіться відповідний [раздел руководства](configuration.changes.modes.md), в якому наводиться опис рівнів доступу

> **Зауваження**
> 
> Директива може мати кілька рівнів доступу, у цьому випадку `access` міститиме відповідну бітову маску.

### Приклади

**Приклад #1 Приклади використання **inigetall()****

```php
<?php
print_r(ini_get_all("pcre"));
print_r(ini_get_all());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #2 Відключення `details`**

```php
<?php
print_r(ini_get_all("pcre", false)); // Добавлено в PHP 5.3.0
print_r(ini_get_all(null, false)); // Добавлено в PHP 5.3.0
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

> **Зауваження**
> 
> **inigetall()** ігнорує опції типу "масив", такі як pdo.dsn.

### Дивіться також

-   [Як змінити налаштування конфігурації](configuration.changes.md)
-   [iniget()](function.ini-get.md) - Отримує значення налаштування конфігурації
-   [inirestore()](function.ini-restore.md) - Відновлює налаштування конфігурації.
-   [iniset()](function.ini-set.md) - Встановлює налаштування конфігурації
-   [getloadedextensions()](function.get-loaded-extensions.md) - Повертає масив імен усіх скомпілованих та завантажених модулів
-   [phpinfo()](function.phpinfo.md) - Виводить інформацію про поточну конфігурацію PHP
-   [ReflectionExtension::getINIEntries()](reflectionextension.getinientries.md) - Отримання ini-налаштувань модуля
