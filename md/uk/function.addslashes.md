---
navigation:
  - function.addcslashes.md: « addcslashes
  - function.bin2hex.md: bin2hex »
  - index.md: PHP Manual
  - ref.strings.md: Функції для роботи з рядками
title: addslashes
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# addslashes

(PHP 4, PHP 5, PHP 7, PHP 8)

addslashes — Екранує рядок за допомогою слішів

### Опис

```methodsynopsis
addslashes(string $string): string
```

Повертає рядок зі зворотним слішем перед символами, які потрібно екранувати. Екрануються такі символи:

-   одинарна лапка (`'`) .
-   подвійна лапка (`"`) .
-   зворотний сліш (`\`) .
-   NUL (байт\*\*`null`\*\*) .

Невеликий приклад використання функції **addslashes()** для екранування перелічених вище символів:

```php
<?php
$str = "O'Reilly?";
eval("echo '" . addslashes($str) . "';");
?>
```

Иногда функцию**addslashes()** некоректно намагаються використати для запобігання [SQL-ін'єкцій](security.database.sql-injection.md). Не робіть так. Замість цього використовуйте підготовлені запити або функції екранування відповідних модулів роботи з базами даних.

### Список параметрів

`string`

Рядок, що екранується.

### Значення, що повертаються

Повертає рядок, що екранується.

### Приклади

**Приклад #1 Приклад використання** addslashes()\*\*\*\*

```php
<?php
$str = "Ваше имя O'Reilly?";

// выводит: Ваше имя O\'Reilly?
echo addslashes($str);
?>
```

### Дивіться також

-   [stripcslashes()](function.stripcslashes.md) \- Видаляє екранування символів, зроблене функцією addcslashes
-   [stripslashes()](function.stripslashes.md) \- Видаляє екранування символів
-   [addcslashes()](function.addcslashes.md) \- Екранує рядок слішами у стилі мови C
-   [htmlspecialchars()](function.mdspecialchars.md) \- Перетворює спеціальні символи в HTML-сутності
-   [quotemeta()](function.quotemeta.md) \- Екранує спеціальні символи
-   [get\_magic\_quotes\_gpc()](function.get-magic-quotes-gpc.md) \- Отримання поточного значення конфігурації конфігурації magic\_quotes\_gpc
